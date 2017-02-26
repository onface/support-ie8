# support-ie8


## polyfill

在页面引入 polyfil 

```html
<!--[if lt IE 10]>
<script src="/polyfill-ie8.js"></script>
<![endif]-->
```

[polyfill-ie8.js](https://raw.githubusercontent.com/fast-flow/support-ie8/master/polyfill-ie8.js)

## 其他资源

- [react-ie8](https://github.com/xcatliu/react-ie8)

## 使用特定版本的构建工具

- :+1: `webpack@1.13.2` https://github.com/SamHwang1990/blog/issues/6
- :+1: `karma@1.3.0` https://github.com/karma-runner/karma/issues/2556
- :+1: `react@1.14.8` react@15.*.* 不兼容IE8

## 构建工具兼容配置

- :information_source:  `[uglify2](https://github.com/mishoo/UglifyJS2)@2.7.0`之后的版本 `screw-ie8` 需要设置为 `false`。
- :information_source:  `babel-presets-es2015` 设置 `loose:true` 可避免出现 `Object.defineProperty`   `"presets": [ ["es2015", { "loose": true }] ]`


## 使用特定版本的第三方包

- :warning: `react-router@2.3.0` `2.3.0` 以上版本存在 `Object.defineProperty`
- :warning: `redux@3.*.*`  redux 4 不支持IE8 [Redux 4 breaking changes](https://github.com/reactjs/redux/issues/1342)

## 不要使用特定版本的第三方包

- :warning: `react-redux@4.0.1~4.0.3` https://github.com/reactjs/react-redux/issues/227

## 不要使用的第三包

- :warning: [enzyme](https://github.com/airbnb/enzyme)
- :warning: `redux-saga` https://github.com/redux-saga/redux-saga/issues/313

## IE Debug

### 禁用内存保护（IE8没有）
![image](https://cloud.githubusercontent.com/assets/3949015/23246656/305ce328-f9d0-11e6-868c-eb5c53698d80.png)

### 禁用崩溃重启
![image](https://cloud.githubusercontent.com/assets/3949015/23246659/3da388ca-f9d0-11e6-9b09-e8d571cd8308.png)

### 找到调试工具

![image](https://cloud.githubusercontent.com/assets/3949015/23251177/3e85c96c-f9e7-11e6-8b2c-7eb1028fe4d6.png)

### 普通刷新清除不了IE缓存

![image](https://cloud.githubusercontent.com/assets/3949015/23251406/223b18a6-f9e8-11e6-8f2e-1ff475118ad6.png)
