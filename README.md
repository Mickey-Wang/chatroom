# 多人多房间聊天室


> 这是一个使用Socket.IO和Angular JS快速搭建的，基于node技术栈实现的多人多房间聊天室。来自于 [technode-tutorial](https://github.com/island205/technode-tutorial/tree/master)的项目学习。 

本项目分为四个独立部分，从最简单的聊天室实现到最终的架构优化与发布，由浅入深，分别独立讲解，各部分有对应的充分详细的教程文本（四个.md文件）。下面是对该项目简明的概述说明，使你更快的总览了解本项目。

## 目录结构与使用说明
1. chapter01：最简单的聊天室
    - 在technode目录中先运行npm install
    - npm全局安装bower，npm install -g bower
    - 根据.bowerrc安装依赖的前端类库，bower install
    - static目录为客户端代码啊，static/components目录为前端类库仓库
    - app.js为服务端入口文件
    - 运行node app.js即可在多客户端访问localhost:3000进行聊天
2. 

## 开发过程中的难点或知识盲点
- socket.io出现就是为了磨平浏览器的差异，为开发者提供一个统一的接口，在不支持WebSocket的浏览器中，socket.io可以降级为其他通信方式来实现实时通信。  
其中在客户端引入socket.io为客户端提供的类库socket.io.js。这个文件是由socket.io输出的，我们无须把这个文件添加到static目录中。如此引入`<script type="text/javascript" src="/socket.io/socket.io.js"></script>`
- 