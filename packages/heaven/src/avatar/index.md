---
title: Avatar - 头像
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Avatar - 头像

用来代表用户或事物，支持图片、图标或字符展示。

## 设计师专属

安装 [Kitchen Sketch 插件 💎](https://kitchen.alipay.com)，一键填充高逼格头像和文本。

### 带徽标的头像

<code src="./demos/badge.tsx" />

### 基本

<code src="./demos/basic.tsx" />

### 自动调整字符大小

<code src="./demos/dynamic.tsx" />

<code src="./demos/fallback.tsx" />

### Avatar.Group

<code src="./demos/group.tsx" />

### 响应式尺寸

<code src="./demos/responsive.tsx" />

<code src="./demos/toggle-debug.tsx" />

### 类型

<code src="./demos/type.tsx" />

## API

### Avatar

| 参数      | 说明                                                          | 类型                                                                        | 默认值    | 版本             |
| --------- | ------------------------------------------------------------- | --------------------------------------------------------------------------- | --------- | ---------------- |
| alt       | 图像无法显示时的替代文本                                      | string                                                                      | -         |                  |
| gap       | 字符类型距离左右两侧边界单位像素                              | number                                                                      | 4         | 4.3.0            |
| icon      | 设置头像的自定义图标                                          | ReactNode                                                                   | -         |                  |
| shape     | 指定头像的形状                                                | `circle` \| `square`                                                        | `circle`  |                  |
| size      | 设置头像的大小                                                | number \| `large` \| `small` \| `default` \| { xs: number, sm: number, ...} | `default` | 4.7.0            |
| src       | 图片类头像的资源地址或者图片元素                              | string \| ReactNode                                                         | -         | ReactNode: 4.8.0 |
| srcSet    | 设置图片类头像响应式资源地址                                  | string                                                                      | -         |                  |
| draggable | 图片是否允许拖动                                              | boolean \| `'true'` \| `'false'`                                            | -         |                  |
| onError   | 图片加载失败的事件，返回 false 会关闭组件默认的 fallback 行为 | () => boolean                                                               | -         |                  |

> Tip：你可以设置 `icon` 或 `children` 作为图片加载失败的默认 fallback 行为，优先级为 `icon` > `children`

### Avatar.Group (4.5.0+)

| 参数                | 说明                 | 类型                                                                        | 默认值    | 版本  |
| ------------------- | -------------------- | --------------------------------------------------------------------------- | --------- | ----- |
| maxCount            | 显示的最大头像个数   | number                                                                      | -         |       |
| maxPopoverPlacement | 多余头像气泡弹出位置 | `top` \| `bottom`                                                           | `top`     |       |
| maxStyle            | 多余头像样式         | CSSProperties                                                               | -         |       |
| size                | 设置头像的大小       | number \| `large` \| `small` \| `default` \| { xs: number, sm: number, ...} | `default` | 4.8.0 |
