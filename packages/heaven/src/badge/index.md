---
title: Badge - 徽标数
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Badge - 徽标数

图标右上角的圆形徽标数字。

## 何时使用

一般出现在通知图标或头像的右上角，用于显示需要处理的消息条数，通过醒目视觉形式吸引用户处理。

- <font color="#346fff"> 方形（V2.0）：一般用于单字母文本 </font>

### 基本

<code src="./demos/basic.tsx" />

### 动态

<code src="./demos/change.tsx" />

### 多彩徽标

<code src="./demos/colorful.tsx" />

### 讨嫌的小红点

<code src="./demos/dot.tsx" />

### 可点击

<code src="./demos/link.tsx" />

### 独立使用

<code src="./demos/no-wrapper.tsx" />

### 自定义位置偏移

<code src="./demos/offset.tsx" />

### 封顶数字

<code src="./demos/overflow.tsx" />

### 缎带

<code src="./demos/ribbbon.tsx" />

<code src="./demos/ribbon-debug.tsx" />

### 大小

<code src="./demos/size.tsx" />

### 状态点

<code src="./demos/status.tsx" />

<code src="./demos/title.tsx" />

## 扩展

### 方形

<code src="./demos/square.tsx" />

## API

### Badge

| 参数          | 说明                                                                     | 类型                                                           | 默认值 | 版本  |
| ------------- | ------------------------------------------------------------------------ | -------------------------------------------------------------- | ------ | ----- |
| color         | 自定义小圆点的颜色                                                       | string                                                         | -      |       |
| count         | 展示的数字，大于 overflowCount 时显示为 `${overflowCount}+`，为 0 时隐藏 | ReactNode                                                      | -      |       |
| dot           | 不展示数字，只有一个小红点                                               | boolean                                                        | false  |       |
| offset        | 设置状态点的位置偏移                                                     | \[number, number]                                              | -      |       |
| overflowCount | 展示封顶的数字值                                                         | number                                                         | 99     |       |
| showZero      | 当数值为 0 时，是否展示 Badge                                            | boolean                                                        | false  |       |
| size          | 在设置了 `count` 的前提下有效，设置小圆点的大小                          | `default` \| `small`                                           | -      | 4.6.0 |
| status        | 设置 Badge 为状态点                                                      | `success` \| `processing` \| `default` \| `error` \| `warning` | -      |       |
| text          | 在设置了 `status` 的前提下有效，设置状态点的文本                         | ReactNode                                                      | -      |       |
| title         | 设置鼠标放在状态点上时显示的文字                                         | string                                                         | -      |       |
| square        | 使用小方点                                                               | boolean                                                        | false  | 2.0   |

### Badge.Ribbon (4.5.0+)

| 参数      | 说明                                                      | 类型             | 默认值 | 版本 |
| --------- | --------------------------------------------------------- | ---------------- | ------ | ---- |
| color     | 自定义缎带的颜色                                          | string           | -      |      |
| placement | 缎带的位置，`start` 和 `end` 随文字方向（RTL 或 LTR）变动 | `start` \| `end` | `end`  |      |
| text      | 缎带中填入的内容                                          | ReactNode        | -      |      |
