[TOC]

# 前端学习



## 【基础】

### HTML

- 网页结构
- HTML标签
- **HTML5**新增标签和属性
  - 表单
  - canvas画布
  - 媒体
- 标签语义化，SEO
- 页面加载的流程和原理

### CSS

- CSS语法
- 盒模型（W3C标准盒模型和IE盒模型）
- CSS选择器
- CSS定位
- CSS布局、浮动
- **CSS3**新特性
  - CSS3选择器
  - 边框
  - 背景
  - 阴影
  - 过渡和动画
  - 弹性布局

### JavaScript

- 基本语法
- 变量和数据类型
- 函数
- 对象
- 面向对象编程
- 原型链、闭包
- JSON
- Ajax
- DOM和BOM
- ES5、6、7

### JQuery

- jQuery语法
- jQuery选择器
- jQuery对象
- DOM操作
- 事件
- 动画和网页特效

------



## 【进阶】

### SVG

### 图表可视化

- Echarts
- Highcharts
- webGL
  - D3.js
  - three.js
- ThingJS

### CSS3

- 布局
  - Flexbox 弹性布局
  - Grids网格布局
- 变换 过渡 动画
  - transform
  - transition
  - animation
- 响应式开发
  - rem
  - 百分比
  - 媒体查询
  - Flexbox 弹性布局
- 开发框架
  - Bootstrap
  - Foundation
  - Materialize
  - Semantic UI
- 预处理器
  - Sass
  - Less
  - Stylus
  - Postcss

### JavaScript

- Object 对象
  - 常用方法
  - 创建、修改、清空
- Array 数组
  - 常用方法
  - 创建、修改、清空
- Regexp 正则表达式
  - 基本规则
  - 常用正则
- ES6、7
  - let / const 声明（块级作用域）
  - destructuring 解构
  - backtick strings 字符串模板
  - class
  - promise
  - async / await
  - spread 扩展参数
  - rest 剩余参数
  - fat arrows 箭头函数 =>
  - getters / setters
  - module 模块g
  - generator / for of
- TypeScript
  - 强类型语言
  - 接口
  - 泛型
  - 枚举
  - 类型推论
  - 高级类型
  - 模块
  - 命名空间
  - 装饰器
  - 
- 异步编程
  - callback
  - promise
  - generator
  - async / await
  - RxJS（针对异步数据流的编程）
- 数据结构和算法
- 设计模式

### 函数式编程

- 三大编程范式（面向过程编程 / 面向对象编程 / 函数式编程）
- 函数是第一等公民
- 强调将计算过程分解成可复用的函数
- 只有[纯的](https://zh.wikipedia.org/wiki/纯函数)、没有[副作用](https://zh.wikipedia.org/wiki/函数副作用)的函数，才是合格的函数
- 基本运算
  - compose 合成
  - curry 柯里化
    - 多参数 => 单参数
- Functor 函子
  - of方法 替代 new关键字
  - Either 函子
    - 提供默认值
    - 代替`try...catch`，使用左值表示错误
  - ap 函子
    - ap方法
    - 对于那些多参数的函数，就可以从多个容器之中取值，实现函子的链式操作
  - Monad 函子
    - 总是返回一个单层的函子，有个`flatMap`(chain)方法，与`map`方法作用相同，唯一的区别是如果生成了一个嵌套函子，它会取出后者内部的值，保证返回的永远是一个单层的容器，不会出现嵌套的情况。
    - 实现 I/O （输入输出）操作
- 应用
  - react框架
  - promise
  - 通过柯里化的方式声明函数
    - 可以缓存中间值
    - 可以中断函数的运算

### 源码阅读

- jQuery 
- vue 
- webpack

### 手写系列

- 手写 jQuery

- 手写 vue

- 手写 react

- 手写 angular

  

- 手写 call

- 手写 apply

- 手写 bind

- 手写 promise

- 手写 async / await

- 手写 缓动框架

------



## 【流行框架】

### vue

- vuex
- vue-router
- axios
- vue-cli

### react

- flux
- redux
- mobx

### angular

### BootStrap

- 栅格系统和排版
- 表格、表单、按钮、图片、模态框、弹出框、下拉菜单、导航、分页、标签等等

------



## 【前端工作流】

### 工作流规范	

- ##### git-flow 

  - 示意图
    - ![](F:\github\study\frontend_前端学习.assets\git_flow.png)
  - 参考链接
    - https://nvie.com/posts/a-successful-git-branching-model/
  - 特点
    - 长期分支
      1. 主分支-master，具有多个tag，是develop分支上经过开发、测试后稳定发布的版本，用于发布
      2. 开发分支-develop，是自动构建分支，所有的feature分支的代码完成后会合并到develop
    - 短期分支（完成任务后删除）
      1. 功能分支-feature，从develop拉取，为即将发布的版本开发新功能，最终合并回develop
      2. bug修复分支-hotfix，从master拉取，以便快速修复线上问题，修复完成后合并到develop和master
      3. 测试分支-release，从develop拉取，包含所有新功能和必要的修复，并且是彻底测试过的，会合并到master和develop
  - 应用场景
    - 需要支持多个版本的软件并且相互独立
    - 多版本独立，同时后续各版本开发

- ##### github-flow

  - 示意图
    - ![](F:\github\study\frontend_前端学习.assets\github_flow.png)
  - 参考链接
    - https://guides.github.com/introduction/flow/
  - 特点
    - 只有一个master长期分支和多个feature分支
    - master分支中的代码一定是可以部署的
    - 新建的分支名称需体现此分支的作用（语义化分支名）
    - 支持快速迭代、部署，适合需求变化多端的前端**开源项目**
  - 工作流
    - master => feature branches  => pull request => master
  - 应用场景
    - 需要频繁部署、持续发布的项目

- ##### gitlab-flow

  - 示意图
    - ![](F:\github\study\frontend_前端学习.assets\gitLab_flow.png)
  - 参考链接
    - https://docs.gitlab.com/ee/topics/gitlab_flow.html
  - 特点
    - master为主分支
    - 拥有环境分支pre-production(预发分支)、production(生产分支)

  - 应用场景：
    - 需要进行预发布的项目
    - gitlab推荐的工作流方式



------



## 【模块化开发】

### 模块化开发规范

### RequireJS / SeaJS

### AMD / CMD

### 统一规范UMD

------



## 【NodeJS】

### 基本操作

### 内置模块

### 高级特性

### 常用框架

------



## 【常用工具】

### 包管理工具

- Yarn

- npm

### 构建工具

- grunt

- gulp

### 打包工具

- webpack
- rollup
- Parcel
- RequireJS / AMD
- Browserify

### 测试工具

- jest

- mocha

- Jasmine

- Enzyme

### 开发工具

- Chrome 浏览器

- vue-dev-tools（google插件）

- Typora

- VS code / Atom / WebStorm / Sublime / Notepad++

- Git / SVN / TortoiseGit（小乌龟）

- Node

- Python

- mysql数据库 navicat

- Postman

- Xftp Xshell

- 微信开发者工具 wechat_devtools

- X-mind

- PS

------



### 