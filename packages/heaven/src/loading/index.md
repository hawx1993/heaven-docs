---
title: Loading - 加载
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Loading - 加载

全局加载 loading。

## 何时使用

组件的加载样式, 支持依照子组件大小渲染, 品牌 logo

### 基本用法

<code src="./demos/loop.tsx" />

### 轻量加载

<code src="./demos/Simple.tsx" />

### Loading

| 参数    | 说明             | 类型         | 默认值 | 版本 |
| ------- | ---------------- | ------------ | ------ | ---- |
| time    | 动画运行一次时长 | number（ms） | 4000   |      |
| loading | 动画是否加载     | boolean      | true   |
| loop    | 是否循环播放     | boolean      | true   |

### Loading.Simple 0.5.x

| 参数    | 说明                                               | 类型         | 默认值    | 版本 |
| ------- | -------------------------------------------------- | ------------ | --------- | ---- |
| loading | 动画是否加载                                       | boolean      | true      |      |
| size    | 组件大小，<br />可选值为 `small` `default` `large` | string       | `default` |      |
| time    | 动画运行一次时长                                   | number（ms） | 1000      |      |
