# node.js

## 如何系统地学习Node.js？

掌握JavaScript并不是会用jQuery做两特效，而是JavaScript语法、各种坑、原型继承、函数、this作用域、map/reduce、regex等，紧跟ES6标准，适当追踪ES7的脚步。

掌握JS精髓是知道哪些代码好，哪些是炫技的垃圾代码。

其次，掌握浏览器DOM概念、基本操作、HTTP协议、AJAX、表单等；

接下来，才是学习jQuery，因为它只是帮你更好地使用JS；

再往后，学习Node.js，就要学服务器端开发能力：

基本开发环境：Node+npm
基本模块：fs/stream/http/crypto

然后，学习Web开发基本概念：
MVC模式，链式处理，模版引擎

什么？你还在学express？JS的发展一年相当于十年，koa3都要发了，现在必须得上koa2
异步处理要跟上节奏：callback（负分）→ async库（及格）→ generator → Promise → async/await才是终极方案

有人吐槽koa中间件少，晕，随便一个express中间件10分钟改造成async函数好不好？

接下来要学如何操作数据库：
SQL基础，MySQL操作，ORM框架
Mongo之类的忽悠人可以，线上还是老实用MySQL

## 什么是前端

HTML + CSS + JavaScript

网页页面，其中包括控件布局，色调，字体，控件响应等等，都属于 前端

## 什么是后端

网站的逻辑部分，主要涉及数据库，如PHP、.net、GO、Node.js等

## 什么是 JavaScript

一门脚本语言

需嵌入到 HTML 执行

JavaScript语言实际上是两种语言风格的混合产物——（简化的）函数式编程 +（简化的）面向对象编程

## 浏览器 和 JavaScript 的关系

浏览器会把 JS 代码转换成 **计算机** 能看懂的语言(机器码/字节码)

浏览器的内核 -> JS引擎

JS引擎 将 JS代码 转换为 机器码/字节码

# 什么是 Node.js

在 V8 引擎基础上套了一层壳，通过编写 JS 代码可以实现后端能做的事情

特点：事件驱动、非阻塞的I/O等特性

优势：轻量、高效

官网：[https://nodejs.org/en/](https://nodejs.org/en/)

## 官网给出的 Node 的介绍

Node.js 是一个构建于 Chrome V8 引擎之上的 JavaScript 运行时环境

Node.js 使用 事件驱动，非阻塞 I/O 模型，这使得它非常轻量，高效。

Node.js 包管理生态，npm，是世界上最大的开源库生态系统

## 3m安装法

[nvm](https://github.com/creationix/nvm) （Node Version Manager）

解决多版本共存、切换问题

[npm](https://github.com/npm/npm)   (Node Package Manager)  

解决 Node.js 模块安装问题

[nrm](https://github.com/Pana/nrm)    (NPM Registry Manager)

解决 npm 镜像访问慢，提供测试，切换

## NVM

curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash

下载nvm, 并将路径配置到 ~/.bashrc 中

注: 如果终端是zsh，则需要配置到~/.zshrc 中(可通过 echo $0 查询)

## NVM 常用命令

nvm  --version  查看当前版本

nvm ls 查看当前已安装 node 的版本

nvm ls-remote 查看远程 node 的版本

nvm install 4.4.5 安装某版本 node

nvm use 4.4.5 使用某版本 node 

nvm alias default 4.4.5 把某版本 node 设为默认值

## NPM

安装完 Node 后自带 npm

npm -v 查询当前npm版本

npm install npm -g 通过 npm 更新 npm

npm install 模块名 

[常用 npm 模块一览](https://github.com/ruanyf/articles/blob/master/2015/2015-04-04-npm-modules.md)

## NRM

npm install -g nrm

nrm test 

nrm ls

nrm use taobao

## CommonJS

CommonJS API定义很多普通应用程序（主要指非浏览器的应用）使用的API，从而填补了这个空白。它的终极目标是提供一个类似Python，Ruby和Java标准库。这样的话，开发者可以使用CommonJS API编写应用程序，然后这些应用可以运行在不同的JavaScript解释器和不同的主机环境中

## CommonJS可以做

在兼容CommonJS的系统中，你可以使用JavaScript开发：

服务器端JavaScript应用程序
命令行工具
图形界面应用程序
混合应用程序（如，Titanium或Adobe AIR）

## CommonJS规范

模块（modules）

包（packages）

系统（system）

二进制（binary）

控制台（console）

编码（encodings）

文件系统（filesystems）

套接字（sockets)

单元测试（unit test）

## CommonJS对模块的定义

require - 用来引入依赖

export - 用来导出模块，包括标识符(identifier)和模块内容(contents)

module.exports

exports.xxx

## NodeJS和CommonJS之间的关系

CommonJS是一种规范，而Node.js是这种规范的实现

Node.js只是实现了部分CommonJS的规范