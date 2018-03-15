# support-ie8


## polyfill

在页面引入 polyfil

```html
<script src="https://cdn.polyfill.io/v2/polyfill.min.js"></script>
```

## 其他资源

- [react-ie8](https://github.com/xcatliu/react-ie8)

## 使用特定的构建工具

- :+1: 使用 `es3ify-loader`

## 使用特定版本的构建工具

- :+1: `webpack@1.13.2` https://github.com/SamHwang1990/blog/issues/6
- :+1: `karma@1.3.0` https://github.com/karma-runner/karma/issues/2556

## 构建工具兼容配置

- :information_source: React hot reload 不支持IE8，本地开发阶段要测试IE8请取消热更新.
- :information_source: `uglify@2.7.0`之后的版本 设置 `screw-ie8: false` `compress: { warnings: false, screw_ie8: false }, mangle: { screw_ie8: false }, output: { screw_ie8: false }`
- :information_source: `babel-presets-es2015` 设置 `loose: true` ，避免出现 `Object.defineProperty` *`"presets": [ ["es2015", { "loose": true }] ]`*


## 使用特定版本的第三方包

- :+1: `react@1.14.8` `react@15.*.*` 不兼容IE8
- :+1: `react-router@2.3.0` `2.3.0` 以上版本存在 `Object.defineProperty`
- :+1: `redux@3.*.*`  `redux 4` 不支持IE8 [Redux 4 breaking changes](https://github.com/reactjs/redux/issues/1342)

## 不要使用特定版本的第三方包

- :warning: `antd@2x`
- :warning: `react-redux@4.0.1~4.0.3` https://github.com/reactjs/react-redux/issues/227

## 不要使用的第三包

- :warning: `enzyme`
- :warning: `redux-saga` https://github.com/redux-saga/redux-saga/issues/313

## webpack 注意事项

```
// 不兼容IE8
import { Tabs } from "antd"
// 兼容IE8
import Tabs from "antd/lib/tabs"
```

## IE Debug

### 禁用内存保护（IE8没有）
![image](https://cloud.githubusercontent.com/assets/3949015/23246656/305ce328-f9d0-11e6-868c-eb5c53698d80.png)

![image](
https://camo.githubusercontent.com/14fe4cd48bf45038d6f2685d5ded18989472a6eb/687474703a2f2f69312e7069696d672e636f6d2f3536373537312f636430306632363833323137326337382e706e67)

### 禁用崩溃重启
![image](https://cloud.githubusercontent.com/assets/3949015/23246659/3da388ca-f9d0-11e6-9b09-e8d571cd8308.png)

### 找到调试工具

> 吐槽：有时调试工具会出现在屏幕外，导致无法找到。

![image](https://cloud.githubusercontent.com/assets/3949015/23251177/3e85c96c-f9e7-11e6-8b2c-7eb1028fe4d6.png)

### 普通刷新清除不了IE缓存

![image](https://cloud.githubusercontent.com/assets/3949015/23251406/223b18a6-f9e8-11e6-8f2e-1ff475118ad6.png)
