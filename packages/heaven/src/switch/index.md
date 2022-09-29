---
title: Switch - 开关
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Switch - 开关

开关选择器。

## 何时使用

- 需要表示开关状态/两种状态之间的切换时；
- 和 `checkbox` 的区别是，切换 `switch` 会直接触发状态改变，而 `checkbox` 一般用于状态标记，需要和提交操作配合。
- <font color="#346fff"> 颜色调整（V2.0）：调整显示颜色以及 disable 时颜色改为透明度 50% </font>

### 基本

<code src="./demos/basic.tsx" />

### 不可用

<code src="./demos/disabled.tsx" />

### 加载中

<code src="./demos/loading.tsx" />

### 两种大小

<code src="./demos/size.tsx" />

### 文字和图标

<code src="./demos/text.tsx" />

## API

| 参数              | 说明                                | 类型                                     | 默认值    |
| ----------------- | ----------------------------------- | ---------------------------------------- | --------- |
| autoFocus         | 组件自动获取焦点                    | boolean                                  | false     |
| checked           | 指定当前是否选中                    | boolean                                  | false     |
| checkedChildren   | 选中时的内容                        | ReactNode                                | -         |
| className         | Switch 器类名                       | string                                   | -         |
| defaultChecked    | 初始是否选中                        | boolean                                  | false     |
| disabled          | 是否禁用                            | boolean                                  | false     |
| loading           | 加载中的开关                        | boolean                                  | false     |
| size              | 开关大小，可选值：`default` `small` | string                                   | `default` |
| unCheckedChildren | 非选中时的内容                      | ReactNode                                | -         |
| onChange          | 变化时回调函数                      | function(checked: boolean, event: Event) | -         |
| onClick           | 点击时回调函数                      | function(checked: boolean, event: Event) | -         |

## 方法

| 名称    | 描述     |
| ------- | -------- |
| blur()  | 移除焦点 |
| focus() | 获取焦点 |
