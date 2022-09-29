---
title: Card - 数据展示
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Card - 数据展示

通用卡片容器。

## 何时使用

最基础的卡片容器，可承载文字、列表、图片、段落，常用于后台概览页面。

### 典型卡片

<code src="./demos/basic.tsx" />

### 无边框

<code src="./demos/border-less.tsx" />

### 更灵活的内容展示

<code src="./demos/flexible-content.tsx" />

### 网格型内嵌卡片

<code src="./demos/grid-card.tsx" />

### 栅格卡片

<code src="./demos/in-column.tsx" />

### 内部卡片

<code src="./demos/inner.tsx" />

### 预加载的卡片

<code src="./demos/loading.tsx" />

### 支持更多内容配置

<code src="./demos/meta.tsx" />

### 简洁卡片

<code src="./demos/simple.tsx" />

### 带页签的卡片

<code src="./demos/tabs.tsx" />

## 扩展

### 阴影卡片

<code src="./demos/shadow.tsx" />

## API

```
<Card title="卡片标题">卡片内容</Card>
```

### Card

| 参数                | 说明                                                | 类型                                    | 默认值       | 版本           |
| ------------------- | --------------------------------------------------- | --------------------------------------- | ------------ | -------------- |
| actions             | 卡片操作组，位置在卡片底部                          | Array&lt;ReactNode>                     | -            |                |
| activeTabKey        | 当前激活页签的 key                                  | string                                  | -            |                |
| bodyStyle           | 内容区域自定义样式                                  | CSSProperties                           | -            |                |
| bordered            | 是否有边框                                          | boolean                                 | true         |                |
| bottomLinkText      | 卡片左下方链接文案                                  | string                                  | -            |                |
| cover               | 卡片封面                                            | ReactNode                               | -            |                |
| defaultActiveTabKey | 初始化选中页签的 key，如果没有设置 activeTabKey     | string                                  | `第一个页签` |                |
| extra               | 卡片右上角的操作区域                                | ReactNode                               | -            |                |
| headStyle           | 自定义标题区域样式                                  | CSSProperties                           | -            |                |
| hoverable           | 鼠标移过时可浮起                                    | boolean                                 | false        |                |
| loading             | 当卡片内容还在加载中时，可以用 loading 展示一个占位 | boolean                                 | false        |                |
| ~~size~~            | card 的尺寸                                         | `default` \| `small`                    | `default`    | 0.5.x 删除属性 |
| tabBarExtraContent  | tab bar 上额外的元素                                | ReactNode                               | -            |                |
| tabList             | 页签标题列表                                        | Array&lt;{key: string, tab: ReactNode}> | -            |                |
| tabProps            | [Tabs](/components/tabs/#Tabs)                      | -                                       | -            |                |
| title               | 卡片标题                                            | ReactNode                               | -            |                |
| type                | 卡片类型，可设置为 `inner` 或 不设置                | string                                  | -            |                |
| onTabChange         | 页签切换的回调                                      | (key) => void                           | -            |                |
| onBottomLinkClick   | 卡片左下方链接文案点击回调                          | () => void                              | -            |                |

### Card.Grid

| 参数      | 说明                   | 类型          | 默认值 | 版本 |
| --------- | ---------------------- | ------------- | ------ | ---- |
| className | 网格容器类名           | string        | -      |      |
| hoverable | 鼠标移过时可浮起       | boolean       | true   |      |
| style     | 定义网格容器类名的样式 | CSSProperties | -      |      |

### Card.Meta

| 参数        | 说明               | 类型          | 默认值 | 版本 |
| ----------- | ------------------ | ------------- | ------ | ---- |
| avatar      | 头像/图标          | ReactNode     | -      |      |
| className   | 容器类名           | string        | -      |      |
| description | 描述内容           | ReactNode     | -      |      |
| style       | 定义容器类名的样式 | CSSProperties | -      |      |
| title       | 标题内容           | ReactNode     | -      |      |
