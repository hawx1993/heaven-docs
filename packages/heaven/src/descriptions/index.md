---
title: Descriptions - 描述列表
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Descriptions - 描述列表

成组展示多个只读字段。

## 何时使用

常见于详情页的信息展示。

### 基本

<code src="./demos/basic.tsx" />

### 带边框的

<code src="./demos/border.tsx" />

### 响应式

<code src="./demos/responsive.tsx" />

### 自定义尺寸

<code src="./demos/size.tsx" />

<code src="./demos/style.tsx" />

<code src="./demos/text.tsx" />

### 垂直带边框的

<code src="./demos/vertical-border.tsx" />

### 垂直

<code src="./demos/vertical.tsx" />

## API

### Descriptions

| 参数         | 说明                                                                                            | 类型                             | 默认值       | 版本   |
| ------------ | ----------------------------------------------------------------------------------------------- | -------------------------------- | ------------ | ------ |
| bordered     | 是否展示边框                                                                                    | boolean                          | false        |        |
| colon        | 配置 `Descriptions.Item` 的 `colon` 的默认值                                                    | boolean                          | true         |        |
| column       | 一行的 `DescriptionItems` 数量，可以写成像素值或支持响应式的对象写法 `{ xs: 8, sm: 16, md: 24}` | number                           | 3            |        |
| contentStyle | 自定义内容样式                                                                                  | CSSProperties                    | -            | 4.10.0 |
| extra        | 描述列表的操作区域，显示在右上方                                                                | ReactNode                        | -            | 4.5.0  |
| labelStyle   | 自定义标签样式                                                                                  | CSSProperties                    | -            | 4.10.0 |
| layout       | 描述布局                                                                                        | `horizontal` \| `vertical`       | `horizontal` |        |
| size         | 设置列表的大小。可以设置为 `middle` 、`small`, 或不填（只有设置 `bordered={true}` 生效）        | `default` \| `middle` \| `small` | -            |        |
| title        | 描述列表的标题，显示在最顶部                                                                    | ReactNode                        | -            |        |

### DescriptionItem

| 参数         | 说明           | 类型          | 默认值 | 版本  |
| ------------ | -------------- | ------------- | ------ | ----- |
| contentStyle | 自定义内容样式 | CSSProperties | -      | 4.9.0 |
| label        | 内容的描述     | ReactNode     | -      |       |
| labelStyle   | 自定义标签样式 | CSSProperties | -      | 4.9.0 |
| span         | 包含列的数量   | number        | 1      |       |

> span 是 Description.Item 的数量。 span={2} 会占用两个 DescriptionItem 的宽度。当同时配置 `style` 和 `labelStyle`（或 `contentStyle`）时，两者会同时作用。样式冲突时，后者会覆盖前者。
