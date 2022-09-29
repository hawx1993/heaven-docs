---
title: Popconfirm - 气泡确认框
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Popconfirm - 气泡确认框

点击元素，弹出气泡式的确认框。

## 何时使用

目标元素的操作需要用户进一步的确认时，在目标元素附近弹出浮层提示，询问用户。

和 `confirm` 弹出的全屏居中模态对话框相比，交互形式更轻量。

### 异步关闭

<code src="./demos/async.tsx" />

### 基本

<code src="./demos/basic.tsx" />

### 带内容的确认框

<code src="./demos/content.tsx" />

### 条件触发

<code src="./demos/dynamic-trigger.tsx" />

### 自定义 Icon 图标

<code src="./demos/icon.tsx" />

### 国际化

<code src="./demos/locale.tsx" />

### 位置

<code src="./demos/placement.tsx" />

## API

| 参数              | 说明                                   | 类型                                   | 默认值                   |
| ----------------- | -------------------------------------- | -------------------------------------- | ------------------------ |
| cancelButtonProps | cancel 按钮 props                      | [ButtonProps](/components/button/#API) | -                        |
| cancelText        | 取消按钮文字                           | string                                 | `取消`                   |
| disabled          | 阻止点击 Popconfirm 子元素时弹出确认框 | boolean                                | false                    |
| icon              | 自定义弹出气泡 Icon 图标               | ReactNode                              | &lt;ExclamationCircle /> |
| okButtonProps     | ok 按钮 props                          | [ButtonProps](/components/button/#API) | -                        |
| okText            | 确认按钮文字                           | string                                 | `确定`                   |
| okType            | 确认按钮类型                           | string                                 | `primary`                |
| title             | 确认框的描述                           | ReactNode \| () => ReactNode           | -                        |
| onCancel          | 点击取消的回调                         | function(e)                            | -                        |
| onConfirm         | 点击确认的回调                         | function(e)                            | -                        |

更多属性请参考 [Tooltip](/components/tooltip/#API)。

## 注意

请确保 `Popconfirm` 的子元素能接受 `onMouseEnter`、`onMouseLeave`、`onFocus`、`onClick` 事件。