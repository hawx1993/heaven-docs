---
title: Icon - 图标
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Icon - 图标

语义化的矢量图形。

### 基本用法

<code src="./demos/basic.tsx" />

### 图标列表（彩色）

<code src="./demos/list-colored.tsx" />

### 图标列表

<code src="./demos/list.tsx" />

## API

| 参数      | 说明                                                           | 类型          | 默认值 | 版本 |
| --------- | -------------------------------------------------------------- | ------------- | ------ | ---- |
| component | 控制如何渲染图标，通常是一个渲染根标签为 `<svg>` 的 React 组件 |               | -      |      |
| rotate    | 图标旋转角度（IE9 无效）                                       | number        | -      |      |
| spin      | 是否有旋转动画                                                 | boolean       | false  |      |
| style     | 设置图标的样式，例如 `fontSize` 和 `color`                     | CSSProperties | -      |      |

`Icon` 中的 `component` 组件的接受的属性如下：

| 字段      | 说明                    | 类型             | 只读值         | 版本 |
| --------- | ----------------------- | ---------------- | -------------- | ---- |
| className | 计算后的 `svg` 类名     | string           | -              |      |
| fill      | `svg` 元素填充的颜色    | string           | `currentColor` |      |
| height    | `svg` 元素高度          | string \| number | `1em`          |      |
| style     | 计算后的 `svg` 元素样式 | CSSProperties    | -              |      |
| width     | `svg` 元素宽度          | string \| number | `1em`          |      |
