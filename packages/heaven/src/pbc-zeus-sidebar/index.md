---
title: pbc-zeus-sidebar
group:
  path: /
nav:
  title: pbc组件
  path: /heaven-pbc
---

## pbc-zeus-sidebar

> Demo:

<code src="./demo/index.tsx"></code>

### Usage

```js
import ZeusSidebar from '@perfma/pbc-zeus-sidebar';

function App() {
  return <ZeusSidebar header={{ title: '', logoUrl: '', afterLoginUrl: '' }} />;
}
```

## API

### ZeusSidebar

| 参数      | 说明                                                           | 类型          | 默认值 | 
| - | - | - | - |
| header | object | {} | {afterLoginUrl: '',title:'', logoUrl:''}|
|items | [] | ItemType[]| antd menu items|
|enableCollapsed | boolean| false | 是否折叠侧边栏
|secondaryItems | []| ItemType[] | 底部企业管理 menuItems，无需传入 icon
|showMoreIcon| boolean| false | 是否展示底部`more` icon
|MenuProps| MenuProps| MenuProps | antd MenuProps
|skeletonOption| object | {enable: false, rows: 6} | 是否开启加载骨架屏
