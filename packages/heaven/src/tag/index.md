---
title: Tag - 标签
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Tag - 标签

进行标记和分类的小标签。

## 何时使用

- 用于标记事物的属性和维度。
- 进行分类。

### 添加动画

<!-- <code src="./demos/animation.tsx" /> -->

### 基本

<code src="./demos/basic.tsx" />

### 可选择标签

<code src="./demos/checkable.tsx" />

### 多彩标签

<code src="./demos/colorful.tsx" />

### 可删除或操作标签

<code src="./demos/control.tsx" />

### 控制关闭状态

<code src="./demos/controlled.tsx" />

<code src="./demos/customize.tsx" />

### 图标按钮

<code src="./demos/icon.tsx" />

### 预设状态的标签

<code src="./demos/status.tsx" />

## API

### Tag

| 参数      | 说明                                                       | 类型             | 默认值    | 版本         |
| --------- | ---------------------------------------------------------- | ---------------- | --------- | ------------ |
| closable  | 标签是否可以关闭（点击默认关闭）                           | boolean          | false     |              |
| closeIcon | 自定义关闭按钮                                             | ReactNode        | -         | 4.4.0        |
| color     | 标签色                                                     | string           | -         |              |
| icon      | 设置图标                                                   | ReactNode        | -         |              |
| visible   | 是否显示标签                                               | boolean          | true      |              |
| onClose   | 关闭时的回调（可通过 `e.preventDefault()` 来阻止默认行为） | (e) => void      | -         |              |
| type      | 标签类型                                                   | `add`\|`default` | `default` | `heaven@0.5` |
| maxLength | 标签最大长度                                               | number           | -         | `heaven@0.5` |
| borderless | 设置无边框tag | string | false | ` heaven@2.0 `|

### Tag.CheckableTag

| 参数     | 说明                 | 类型              | 默认值 | 版本 |
| -------- | -------------------- | ----------------- | ------ | ------ |
| checked  | 设置标签的选中状态   | boolean           | false  | |
| onChange | 点击标签时触发的回调 | (checked) => void | -      | |
| checkedType | 选中类型 | string | `default`  | `heaven@2.0`|
