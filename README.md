# support-ie8

- 使用 `webpack@1.13.2` https://github.com/SamHwang1990/blog/issues/6
- 使用 `karma@1.3.0` https://github.com/karma-runner/karma/issues/2556
- [react-ie8](https://github.com/xcatliu/react-ie8)
- [uglify2](https://github.com/mishoo/UglifyJS2)@2.7.0+ `screw-ie8` 需要设置为 `false`，这是个不兼容的修改，但是 Uglify2 作者并没有更版本
- 不要使用 [enzyme](https://github.com/airbnb/enzyme)


## IE Debug

### 禁用内存保护（IE8没有）
![image](https://cloud.githubusercontent.com/assets/3949015/23246656/305ce328-f9d0-11e6-868c-eb5c53698d80.png)

### 禁用崩溃重启
![image](https://cloud.githubusercontent.com/assets/3949015/23246659/3da388ca-f9d0-11e6-9b09-e8d571cd8308.png)

## 找到调试工具

![image](https://cloud.githubusercontent.com/assets/3949015/23251177/3e85c96c-f9e7-11e6-8b2c-7eb1028fe4d6.png)

