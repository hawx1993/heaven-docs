---
title: Empty - 空状态
group:
  path: /
nav:
  title: 组件
  path: /components
---

## Empty - 空状态

空状态时的展示占位图。

## 何时使用

- 当目前没有数据时，用于显式的用户提示（<font color="#346fff">可切换系统自带的 12 种空场景 </font>）。
- 初始化场景时的引导创建流程。
- <font color="#346fff">V2.0:自定义 Description，可设置 title,remark,addon，自动生成符合标准设计的空场景方案</font>

### 基本

<code src="./demos/basic.tsx" />

## 扩展

### 标题

<code src="./demos/title.tsx" />

### 图片大小

<code src="./demos/size.tsx" />

### 全局化配置

<code src="./demos/config-provider.tsx" />

### 自定义

<code src="./demos/customize.tsx" />

### 无描述

<code src="./demos/description.tsx" />

### 选择图片

<code src="./demos/simple.tsx" />

## 内置图片

<code src="./demos/preset.tsx" />

## API

```
<Empty>
  <Button>创建</Button>
</Empty>
```

| 参数        | 说明                                           | 类型                               | 默认值                          | 版本         |
| ----------- | ---------------------------------------------- | ---------------------------------- | ------------------------------- | ------------ |
| description | 自定义描述内容                                 | ReactNode                          | -                               |              |
| image       | 设置显示图片，为 string 时表示自定义图片地址。 | ReactNode                          | `Empty.PRESENTED_IMAGE_DEFAULT` |              |
| imageStyle  | 图片样式                                       | CSSProperties                      | -                               |              |
| size        | 图片尺寸                                       | `normal`,`small`, `middle`,`large` | `normal`                        | `heaven@0.5` |
| title       | 空信息标题                                     | String / ReactNode                 | -                               | 2.0          |
| remark      | 空信息备注                                     | String / ReactNode                 | -                               | 2.0          |
| addon       | 空信息插件如：加一个 Button                    | String / ReactNode                 | -                               | 2.0          |
