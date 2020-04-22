# Webpack介绍和实战
---
## Webpack介绍
### 1. 什么是webpack？
- webpack是一个**模块**打包器
- 在webpack看来，所有资源文件（js/json/css/img/less……）都会作为模块处理
- 它将根据模块的依赖关系进行静态分析，生成对应的静态资源

### 2. 理解loader
- webpack本身只能加载js/json模块，如果要加载其他类型的文件（模块），就需要使用对应的loader进行转换/加载
- loader本身也是运行在nodejs中的JavaScript模块
- loader本身是一个函数，接受源文件作为参数，返回转换的结果
- loader一般以xxx-loader的方式命名，xx代表了这个loader要做的转换功能，比如json-loader
### 3. 配置文件
webpack.config.js是一个node模块，返回一个json格式的配置信息对象
### 4. 插件
- 插件可以完成一些loader不能完成的功能
- 一般是在webpack的配置信息plugins选项中指定
- CleanWebpackPlugin: 自动清楚指定文件夹资源
- HtmlWebpackPlugin：自动生成HTML文件
- UglifyJSPlugin：压缩js文件
