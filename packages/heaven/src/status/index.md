---
title: Status - 状态
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Status - 状态

用于反馈页面的状态结果。

## 何时使用

当有重要操作需告知用户处理结果，且反馈内容较为复杂时使用。

### 403

<code src="./demos/403.tsx" />

### 404

<code src="./demos/404.tsx" />

### 500

<code src="./demos/500.tsx" />

### 自定义 图片

<code src="./demos/custom-image.tsx" />



## API

| 参数     | 说明                       | 类型                                                                   | 默认值 | 版本 |
| -------- | -------------------------- | ---------------------------------------------------------------------- | ------ | - |
| extra    | 操作区                     | ReactNode                                                              | -      | @heaven2.0 |
| image    | 自定义 image               | ReactNode \| string                                                   | -      | @heaven2.0 |
| code   | 结果的状态，决定图标和颜色    |  `404` \| `403` \| `500`                                               | -      | @heaven2.0 |
| subTitle | subTitle 文字              | ReactNode                                                              | -      | @heaven2.0 |
| title    | title 文字                 | ReactNode                                                              | -      | @heaven2.0 |
