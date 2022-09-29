---
title: Spin - 加载中
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Spin - 加载中

用于页面和区块的加载中状态。

## 何时使用

- 被动等待提示：页面局部处于等待异步数据或正在渲染过程时，合适的加载动效会有效缓解用户的焦虑。
- <font color="#346fff">V2.0：主动执行类：新增圆圈指示符类，用于比如点击执行等待相关</font>

### 基本用法

<code src="./demos/basic.tsx" />

### 自定义指示符

<code src="./demos/custom-indicator.tsx" />

### 延迟

<code src="./demos/delayAndDebounce.tsx" />

### 容器

<code src="./demos/inside.tsx" />

### 卡片加载中

<code src="./demos/nested.tsx" />

### 各种大小

<code src="./demos/size.tsx" />

### 自定义描述文案

<code src="./demos/tip.tsx" />

## 扩展

### 圆圈指示符（主动执行类）

<code src="./demos/circle.tsx" />

## API

| 参数             | 说明                                         | 类型                                                           | 默认值    | 版本         |
| ---------------- | -------------------------------------------- | -------------------------------------------------------------- | --------- | ------------ |
| delay            | 延迟显示加载效果的时间（防止闪烁）           | number (毫秒)                                                  | -         |              |
| indicator        | 加载指示符                                   | ReactNode                                                      | -         |              |
| size             | 组件大小，可选值为 `small` `default` `large` | string                                                         | `default` |              |
| spinning         | 是否为加载中状态                             | boolean                                                        | true      |              |
| tip              | 当作为包裹元素时，可以自定义描述文案         | string                                                         | -         |              |
| wrapperClassName | 包装器的类属性                               | string                                                         | -         |              |
| circle           | 转为主动执行类（圆圈指示符）                 | 类型为`boolean` 或 {icon:`boolean`,text:`string` 或 `boolean`} | false     | `@heaven2.0` |

### 静态方法

- `Spin.setDefaultIndicator(indicator: ReactNode)`

  你可以自定义全局默认 Spin 的元素。
