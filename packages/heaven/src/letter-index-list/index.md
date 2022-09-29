---
title: LetterIndexList - 字母索引列表
group:
  path: /
nav:
  title: 组件
  path: /components
---

## LetterIndexList - 字母索引列表

类通讯录导航

## 何时使用

需要按名称快捷导航时

### 基本用法

<code src="./demo.tsx"></code>

## API

| 属性         | 说明                 | 类型                                                                                 | 默认值 |
| ------------ | -------------------- | ------------------------------------------------------------------------------------ | ------ |
| dataSource   | 源数组               | [LetterGroup](#lettergroup)`[]`                                                      | `无`   |
| selectable   | 元素是否可选择       | `boolean`                                                                            | `true` |
| initialValue | 选择模式下，初始选项 | `any`                                                                                | `无`   |
| height       | 容器高度             | `string \| number`                                                                   | `400`  |
| width        | 容器宽度             | `string \| number`                                                                   | `194`  |
| onChange     | 元素点击事件         | `({ selected, item, }: { selected: any; item: LetterGroupItem; }) => void`           | `无`   |
| itemRender   | 元素自定义渲染函数   | `(item: LetterGroupItem) => ReactElement<any, string \| JSXElementConstructor<any>>` | `无`   |

### LetterGroup

```ts
export type LetterGroup = {
  letter: string;
  children: { id: any; name: any }[];
};
```
