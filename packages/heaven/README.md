# @perfma/heaven

An UI Framework base [Ant Design V4](https://ant.design/components/overview-cn/) for React.

## 开始使用

- 安装

  ```bash
  npm i  @perfma/heaven
  ```

- 已经支持按需加载样式（使用 babel-import-plugin）, 请剔除之前 prefixCls 和 @antd-prefix

  ```
  import { Button } from '@perfma/heaven';
  ↓  ↓  ↓  ↓
  import { Button } from '@perfma/heaven';
  import '@perfma/heaven/lib/button/style/index.less';
  import 'antd/es/button/style.less';
  ```

- babel-import-plugin 配置说明：（修改 babel.config）

  ```
  [
    'import',

    {
      libraryName: '@perfma/heaven',
      libraryDirectory: 'es',
      style: true,
      customStyleName: (name) => `@perfma/heaven/es/${name}`,
    },
  ]
  ```

- heaven less 变量替换，请在 less loader 中进行变量替换

  ```javascript
    // 加入以下配置文件，未来在工程化中会统一集成
    const vars = require('./modifyvars.js')
    // less loader 配置
    lessOptions:{
      javascriptEnabled: true,
      modifyVars : vars
    }

  ```

  ```javascript
  //modifyvars.js
  const fs = require('fs');
  const path = require('path');

  const fileHeaven = fs.readFileSync(
    path.resolve(
      __dirname,
      '..',
      'node_modules/@perfma/heaven/es/style/vars.less',
    ),
    'utf8',
  );
  const vars = {};
  fileHeaven.split('\n').forEach((line) => {
    if (line.indexOf('@import') !== 0) {
      if (line.indexOf('@') === 0) {
        line = line.split('//')[0].replace(';', '');
        const temp = line.split(':');
        const name = temp[0];
        const value = temp[1];
        vars[name] = value;
      }
    }
  });
  // vars['@ant-prefix'] = 'heaven'; // 可在此处自定义 ant-prefix，默认值 heaven

  module.exports = vars;
  ```

- 由于是按需加载，存在 less 文件多次依赖引入以及在开发环境中 src 中样式被覆盖问题，需要进行如下配置：

  - 1、工程化中 rules 配置如下：

  ```javascript
     {
        // heaven 等组件打包成common.css,第一优先级打包
        test: /\.less|css$/,
        include: /node_modules|heaven|antd/,
        use: [
          MiniCssExtractPlugin.loader,
          'css-loader',
          {
            loader: 'postcss-loader',
            options: {
              postcssOptions: {
                plugins: [['postcss-preset-env']],
              },
            },
          },
          {
            loader: 'less-loader',
            options: {
              lessOptions: {
                javascriptEnabled: true,
                modifyVars,
              },
            },
          },
        ],
      },
      {
        // 如果是生产环境则，打包CSS，否则走style-loader
        test: /\.less|css$/,
        include: /src/,
        use: [
          isProduction ? MiniCssExtractPlugin.loader : 'style-loader',
          'css-loader',
          {
            loader: 'postcss-loader',
            options: {
              postcssOptions: {
                plugins: [['postcss-preset-env']],
              },
            },
          },
          {
            loader: 'less-loader',
            options: {
              lessOptions: {
                javascriptEnabled: true,
                modifyVars,
              },
            },
          },
        ],
      },
  ```

  - 2、需要开启 common(heaven,antd)css 优先打包，即先加载组件库样式，再走业务组件样式，比如：

    ```html
    <button class="heaven-btn btn-diy">demo</button>
    会先加载heaven-btn样式，再加载btn-diy样式
    ```

    优先级配置如下：

    ```javascript
      optimization: {
        splitChunks: {
          chunks: 'all',
          minChunks: 1,
          cacheGroups: {
            // this is most important!!
            commonStyles: {
              name: 'common',
              test: (module) => {
                const name = module.nameForCondition && module.nameForCondition();
                if (
                  name &&
                  ((/node_modules\/@perfma\/heaven/.test(name) &&
                    /.(c|le)ss$/.test(name)) ||
                    (/node_modules\/antd/.test(name) && /.(c|le)ss$/.test(name)))
                ) {
                  return true;
                }

                return false;
              },
              chunks: 'all',
              type: 'css/mini-extract',
              enforce: true,
              priority: 999, // 最高优先级
            },
            styles: {
                name: 'biz', // 可以重命名，可以是xsea/testma
                type: 'css/mini-extract',
                chunks: 'all',
                enforce: true,
            },
          },
        },
      }
    ```

    - 3、开启去重插件，请在 webpack plugins 安装如下插件

    ```javascript
    const CssMinimizerPlugin = require('css-minimizer-webpack-plugin');
    plugins: [...new CssMinimizerPlugin()];
    ```

- 开始使用

  > 除部分组件的扩展能力外，其他使用方法与 [Ant Design](https://ant.design/components/overview-cn/) 一致。

  ```tsx
  import React from 'react';
  import { Input } from '@perfma/heaven';

  export default () => <Input placeholder="please input" limit={20} />;
  ```

## 改造组件

> 仅对样式进行了自定义修改

- [x] Alert
- [x] Badge
- [x] Breadcrumb
- [x] Button
- [x] Card
- [x] Cascader
- [x] DatePicker
- [x] Drawer
- [x] Empty
- [x] Form
- [x] InputNumber
- [x] Message
- [x] Menu
  - [x] themes, layouts
  - [ ] resize?
- [x] Modal
- [x] Notification
- [x] Pagination
- [x] Popconfirm
- [x] Popover
- [x] Progress
- [x] Select
- [ ] Skeleton
- [ ] Slider
- [ ] Spin
- [x] Switch
- [x] Transfer
- [x] Tree
- [x] TreeSelect
- [x] Tabs
- [x] Tag
- [x] TimePicker
- [ ] Timeline
- [ ] Tooltip
  - [ ] dark 模式
- [ ] Upload

## 扩展组件

> 新增组件，以及对原有组件新增功能

- [Checkbox](/components/checkbox#扩展)
- [Input](/components/input#扩展)
- [LetterIndexList](/components/letter-index-list)
- [Radio](/components/radio#扩展)
- [Table](/components/table#扩展)
- [Toast](/components/toast)
- [Tooltip.Ellipsis](/components/tooltip#ellipsis)

## 文档发布

构建文档并发布到http://heaven.perfma-inc.com

1. 完成开发后，当前分支打一个`docs/***`的 tag，比如 docs/202108202034
2. 推送 tag 到 gitlab，触发 gitlab-ci 进行发布
