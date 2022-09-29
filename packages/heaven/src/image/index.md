---
title: Image - 图片
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Image - 图片

可预览的图片。

## 何时使用

- 需要展示图片时使用。
- 加载大图时显示 loading 或加载失败时容错处理。

### 基本用法

<code src="./demos/basic.tsx" />

### 容错处理

<code src="./demos/fallback.tsx" />

### 渐进加载

<code src="./demos/placeholder.tsx" />

<code src="./demos/preview-mask.tsx" />

### 多张图片预览

<code src="./demos/previewGroup.tsx" />

### 自定义预览图片

<code src="./demos/previewSrc.tsx" />

## API

| 参数        | 说明                               | 类型                                   | 默认值 | 版本                                    |
| ----------- | ---------------------------------- | -------------------------------------- | ------ | --------------------------------------- |
| alt         | 图像描述                           | string                                 | -      | 4.6.0                                   |
| fallback    | 加载失败容错地址                   | string                                 | -      | 4.6.0                                   |
| height      | 图像高度                           | string \| number                       | -      | 4.6.0                                   |
| placeholder | 加载占位, 为 `true` 时使用默认占位 | ReactNode                              | -      | 4.6.0                                   |
| preview     | 预览参数，为 `false` 时禁用        | boolean \| [previewType](#previewType) | true   | 4.6.0 [previewType](#previewType):4.7.0 |
| src         | 图片地址                           | string                                 | -      | 4.6.0                                   |
| width       | 图像宽度                           | string \| number                       | -      | 4.6.0                                   |
| onError     | 加载错误回调                       | (event: Event) => void                 | -      | 4.12.0                                  |

### previewType

```
{
  visible?: boolean;
  onVisibleChange?: (visible, prevVisible) => void;
  getContainer?: string | HTMLElement | (() => HTMLElement); // V4.8.0
  src?: string; // V4.10.0
  mask?: ReactNode; // V4.9.0
  maskClassName?: string; // V4.11.0
  current?: number; // V4.12.0 仅支持 PreviewGroup。
}
```

其他属性见 [&lt;img>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#Attributes)
