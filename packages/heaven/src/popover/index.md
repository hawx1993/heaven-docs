---
title: Popover - 气泡卡片
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Popover - 气泡卡片

点击/鼠标移入元素，弹出气泡式的卡片浮层。

## 何时使用

当目标元素有进一步的描述和相关操作时，可以收纳到卡片中，根据用户的操作行为进行展现。

和 `Tooltip` 的区别是，用户可以对浮层上的元素进行操作，因此它可以承载更复杂的内容，比如链接或按钮等。

### 箭头指向

<code src="./demos/arrow-point-at-center.tsx" />

### 基本

<code src="./demos/basic.tsx" />

### 从浮层内关闭

<code src="./demos/control.tsx" />

### 悬停点击弹出窗口

<code src="./demos/hover-with-click.tsx" />

### 位置

<code src="./demos/placement.tsx" />

### 三种触发方式

<code src="./demos/triggerType.tsx" />

## API

| 参数    | 说明     | 类型                         | 默认值 | 版本 |
| ------- | -------- | ---------------------------- | ------ | ---- |
| content | 卡片内容 | ReactNode \| () => ReactNode | -      |      |
| title   | 卡片标题 | ReactNode \| () => ReactNode | -      |      |

更多属性请参考 [Tooltip](/components/tooltip/#API)。

## 注意

请确保 `Popover` 的子元素能接受 `onMouseEnter`、`onMouseLeave`、`onFocus`、`onClick` 事件。
