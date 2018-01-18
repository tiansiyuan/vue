### webpack 是什么?

如果你已经熟悉了 webpack，随时可以跳过下面的说明。如果你没有使用过 webpack，下面是一个快速介绍：

[webpack](https://webpack.github.io/) 是一个模块打包工具。它将一堆文件中的每个文件都作为一个模块，找出它们的依赖关系，将它们打包为可部署的静态资源。

![webpack](https://webpack.github.io/assets/what-is-webpack.png)

一个基本的例子，想像我们有一些 CommonJS 模块，它们不能直接在浏览器中运行，所以我们需要打包成一个文件，这样就可以通过 `<script>` 标签加载。webpack 可以遵循 `require()` 调用的依赖关系，为我们完成这些工作。

但是 webpack 可以做的不止这些。通过“loader”，我们可以配置 webpack 以任何方式去转换所有类型的文件。包括以下例子：

- 转换 ES2015，CoffeeScript 或者 TypeScript 模块为普通的 ES5 CommonJS 模块；
- 可以选择在编译之前检验你的源代码；
- 将 Jade 模版转换为纯 HTML 并且嵌入 Javascript 字符串中；
- 将 SASS 文件转换为纯 CSS，然后将其转换成 JavaScript 片段，将生成的 CSS 作为 `<style>` 标签插入页面；
- 处理 HTML 或者 CSS 中引用的图片，移动到配置的路径中，并且使用 md5 hash 重命名。

当你理解 webpack 原理后会感觉它是如此强大，它可以大大优化你的前端工作流程。它主要的缺点是配置复杂麻烦，但是使用本指南，应该可以帮助你找到 Vue.js 和 `vue-loader` 使用时的最常见问题的解决方案。