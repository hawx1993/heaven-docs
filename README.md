# 快速介绍

本项目采用 lerna 多包架构方案，将 heaven 基础组件库，template 模板库，以及 pbc 业务组件库结合在一起，方便开发与文档维护。

# 基础使用

## 安装依赖

`yarn install`

### 安装依赖到指定 packages

例如，在@perfma/heaven 中安装 antd

```bash
$ yarn workspace @perfma/heaven add antd
```

or

```bash
$ lerna add antd --scope=@perfma/heaven
```

### 安装依赖到 pbc 组件

例如，安装 lodash 到@perfma/pbc-filter-layout 组件：

```bash
$ lerna add lodash@4.0.1 --scope=@perfma/pbc-filter-layout
```

### 安装所有包的公共依赖

仅 devDeps 的依赖需要安装到根目录依赖中：

```bash
$ yarn  add lodash -D -W
```

### 添加内部模块的依赖

目前仅`heaven-template` 可以依赖 heaven 基础组件和 pbc 业务组件库，heaven-template 不可被任一方依赖。

```bash
$ lerna add @perfma/heaven --scope @perfma/heaven-template
```

## 清空内容

### 清空所有 node_modules

```bash
$ yarn run clean:all
```

### 清空 umi 缓存

```bash
$ yarn run clean:cache
```

## 开发与发布

### 启动在线文档

本地开发环境启动包含基础组件文档，pbc 组件文档和模板库文档：

`yarn start`

### 单独启动 heaven 文档

```
$ yarn start:heaven
```

### 单独启动 pbc 文档

```
$ yarn start:pbc
```

### 单独启动 template 文档

```
$ yarn start:template
```

### 打包 文档

打包包括 pbc 组件文档，基础组件文档和模板库文档

`yarn run build:doc`

### 发布 heaven 包

`yarn run release:heaven`

### 发布 heaven beta 版

```bash
$ yarn run release-alpha:heaven
```

### 发布 heaven-pbc 包

lerna 可自动发布改动过代码的 pbc 组件，无需指明指定的 pbc 组件

```bash
$ yarn run release:pbc
```

## 代码提交

### 使用 commit 命令提交代码

- `yarn run commit` or `yarn run commit:all`

- 选择提交类型
- 依次输入变更范围、变更描述、详情描述、是否有 break change

## 模板生成

可选择生成 pbc 组件或模板库代码模板:

```bash
$ yarn run generate
```

<img src="./docs/imgs/10.png" />

## 相关规范

> code review

- heaven 基础组件库相关 code review at @初七
- heaven-pbc 组件库相关 code review @吹雪
- heaven-template 模板库 code review @白寒

当以上人员无响应时，可 @尼禄 进行 code review

- heaven 基础组件文件夹用小写命名，遵循 antd 命名一致，发布 npm 包请联系 @初七
- heaven-pbc 发布 npm 包，执行 npm run release:pbc，cr 通过后，可自行发包
- heaven-template cr 和设计走查通过后，请联系 @白寒 上传代码到 oss 仓库

## heaven 色板

heaven 组件目前已支持导出色板：

```less
@import '@perfma/heaven/es/style/palette.less';
```

[👉 色板详情点击](./design/color)

#### heaven

- heaven 组件颜色请使用 `style/palette.less` 文件的变量，若颜色在色板找不到，请和设计师沟通解决，不要自己定义变量

> package 引用规范

- heaven-template 可以引用 heaven-pbc 和 heaven 组件，反之则不行
- heaven 基础组件可被任意组件引用，反之，heaven 基础组件不能引用 pbc 组件和模板库

## 开发流程

<img src="./docs/imgs/process.png" />
