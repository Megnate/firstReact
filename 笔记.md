## 创建项目

- create-react-app 项目名称
  - 使用这种方式创建的无法选择内部的是什么（无法使用typescript）
  - 打包是 webpack
- create-react-app 项目名称 --template typescript
  - 支持typescript
  - 打包是 webpack
- npm init vite@latest 项目名称 --template react-ts
  - 支持typescript
  - 使用 vite
  - 本项目使用这种方式来构建第一个react项目
  - 选择babel，不选择 SWC（rust编写的ES6编译器，比babel快10倍）
    - 还未学习rust，所以暂时不选取这种方式进行编译

## package.json

- react-native：构建和渲染APP
- react-scripts：把webpack的打包规则及相关插件都放入node_modules目录中，使用这个来进行封装，使用这个来调用webpack进行打包处理
  - react-scripts eject：暴露webpack的配置规则，可以更改配置
- web-vitals：性能检测工具
- browserslist：基于browserslist规范，设置浏览器的兼容情况
  - postcss-loader + autoprefixer：会给CSS3设置相关的前缀
  - babel-loader：将ES6编译为ES5
  - production
    - not dead：不兼容IE
  - development（默认不兼容低版本和IE浏览器）
    - last 1 chrome version：只考虑 chrome 的最后一个版本