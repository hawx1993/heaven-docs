---
title: Alert - 警告提示
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Alert - 警告提示

警告提示，展现需要关注的信息。

## 何时使用

- 当某个页面需要向用户显示警告的信息时。
- 非浮层的静态展现形式，始终展现，不会自动消失，用户可以点击关闭。

### 操作

<code src="./demos/action.tsx" />

### 顶部公告

<code src="./demos/banner.tsx" />

### 基本

<code src="./demos/basic.tsx" />

### 可关闭的警告提示

<code src="./demos/closable.tsx" />

### 自定义关闭

<code src="./demos/close-text.tsx" />

<code src="./demos/custom-icon.tsx" />

### 含有辅助性文字介绍

<code src="./demos/description.tsx" />

### React 错误处理

<code src="./demos/error-boundary.tsx" />

<code src="./demos/icon.tsx" />

### 轮播的公告

<code src="./demos/loop-banner.tsx" />

### 平滑地卸载

<code src="./demos/smooth-closed.tsx" />

### 四种样式

<code src="./demos/style.tsx" />

## API

| 参数        | 说明                                                                 | 类型                    | 默认值                                    | 版本  |
| ----------- | -------------------------------------------------------------------- | ----------------------- | ----------------------------------------- | ----- |
| action      | 自定义操作项                                                         | ReactNode               | -                                         | 4.9.0 |
| afterClose  | 关闭动画结束后触发的回调函数                                         | () => void              | -                                         |       |
| banner      | 是否用作顶部公告                                                     | boolean                 | false                                     |       |
| closable    | 默认不显示关闭按钮                                                   | boolean                 | -                                         |       |
| closeText   | 自定义关闭按钮                                                       | ReactNode               | -                                         |       |
| description | 警告提示的辅助性文字介绍                                             | ReactNode               | -                                         |       |
| icon        | 自定义图标，`showIcon` 为 true 时有效                                | ReactNode               | -                                         |       |
| message     | 警告提示内容                                                         | ReactNode               | -                                         |       |
| showIcon    | 是否显示辅助图标                                                     | boolean                 | false，`banner` 模式下默认值为 true       |       |
| type        | 指定警告提示的样式，有四种选择 `success`、`info`、`warning`、`error` | string                  | `info`，`banner` 模式下默认值为 `warning` |       |
| onClose     | 关闭时触发的回调函数                                                 | (e: MouseEvent) => void | -                                         |       |

### Alert.ErrorBoundary

| 参数        | 说明                                         | 类型      | 默认值            | 版本 |
| ----------- | -------------------------------------------- | --------- | ----------------- | ---- |
| description | 自定义错误内容，如果未指定会展示报错堆栈     | ReactNode | {{ error stack }} |      |
| message     | 自定义错误标题，如果未指定会展示原生报错信息 | ReactNode | {{ error }}       |      |
