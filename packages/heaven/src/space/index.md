---
title: Space - 间距
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Space - 间距

设置组件之间的间距。

## 何时使用

避免组件紧贴在一起，拉开统一的空间。

- 适合行内元素的水平间距。
- 可以设置各种水平对齐方式。

### 对齐

<code src="./demos/align.tsx" />

### 基本用法

<code src="./demos/base.tsx" />

### 自定义尺寸

<code src="./demos/customize.tsx" />

<code src="./demos/debug.tsx" />

<code src="./demos/gap-in-line.tsx" />

### 间距大小

<code src="./demos/size.tsx" />

### 分隔符

<code src="./demos/split.tsx" />

### 垂直间距

<code src="./demos/vertical.tsx" />

### 自动换行

<code src="./demos/wrap.tsx" />

## API

| 参数      | 说明                                   | 类型                                     | 默认值       | 版本                  |
| --------- | -------------------------------------- | ---------------------------------------- | ------------ | --------------------- |
| align     | 对齐方式                               | `start` \| `end` \|`center` \|`baseline` | -            | 4.2.0                 |
| direction | 间距方向                               | `vertical` \| `horizontal`               | `horizontal` | 4.1.0                 |
| size      | 间距大小                               | [Size](#Size) \| [Size\[\]](#Size)       | `small`      | 4.1.0 \| Array: 4.9.0 |
| split     | 设置拆分                               | ReactNode                                | -            | 4.7.0                 |
| wrap      | 是否自动换行，仅在 `horizontal` 时有效 | boolean                                  | false        | 4.9.0                 |

### Size

`'small' | 'middle' | 'large' | number`
