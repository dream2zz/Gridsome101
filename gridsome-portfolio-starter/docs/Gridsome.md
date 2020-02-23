---
title: 1 Gridsome
excerpt: Gridsome是一个现代的网站开发框架，用于创建可以部署在任何地方的快速，安全的网站。
---

- [1. 简介](#1-%e7%ae%80%e4%bb%8b)
- [2. 原理](#2-%e5%8e%9f%e7%90%86)
- [3. 快速入门](#3-%e5%bf%ab%e9%80%9f%e5%85%a5%e9%97%a8)
  - [3.1. 先决条件](#31-%e5%85%88%e5%86%b3%e6%9d%a1%e4%bb%b6)
  - [3.2. 安装Gridsome CLI工具](#32-%e5%ae%89%e8%a3%85gridsome-cli%e5%b7%a5%e5%85%b7)
  - [3.3. 创建一个Gridsome项目](#33-%e5%88%9b%e5%bb%ba%e4%b8%80%e4%b8%aagridsome%e9%a1%b9%e7%9b%ae)


# 1. 简介

Gridsome是一个开源超4K+基于Vue.js超快速创建现代化网站的工具栈，用于创建可在任何地方部署的快速安全的网站。

它使开发人员可以轻松构建现代JAMstack网站。

Gridsome捆绑了一些难以错过的功能，这使它成为最受欢迎的静态站点生成器之一。其中一些功能包括：

* 基于Vue.js - 最简单，最易用的前端框架。
* 通过热加载进行本地开发 - 在开发过程中实时查看更改。
* 基于文件的页面路由 - src/pages中的任何Name.vue文件都是静态路由。
* 动态路由 - src/pages中的任何[param].vue文件都是动态路由。
* 静态文件生成 - 安全，快速地部署到任何CDN或静态Web主机。
* 数据来源 - 从任何Headless CMS，API或Markdown文件中添加数据。
* GraphQL数据层 - 具有集中式数据层的简单数据管理。
* 自动代码拆分 - 将超高性能构建到每个页面中。
* 自动优化的代码 - 开箱即用的代码分割和资产优化。
* 自动页面预取 - 页面在后台加载以便快速浏览。
* 渐进式图像支持 - 自动调整大小，优化和延迟加载图像。
* 插件生态系统 - 查找适合任何工作的插件。

# 2. 原理

Gridsome是一个现代的网站开发框架，用于创建可以部署在任何地方的快速，安全的网站。生成静态HTML文件以创建SEO友好的标记，一旦将其加载到浏览器中，该标记就会合并到由Vue.js驱动的SPA中。

源插件从本地文件或外部API获取内容，并将数据存储在本地数据库中。统一的GraphQL数据层使您可以仅从数据库中提取所需的数据，并在Vue.js组件中使用它们。数据在构建时生成并存储为静态JSON。

首先只加载关键的HTML，CSS和JavaScript。接下来的页面会被预取，这样用户就可以在不重新加载页面的情况下快速点击，即使离线时也是如此。

Gridsome会自动优化前端以加载和快速执行blazing。你可以得到代码分割，图像优化，延迟加载，几乎完美的灯塔得分开箱即用。

Gridsome站点通常不连接到任何数据库，并且可以完全托管在全局CDN上。它可以处理数千到数百万次点击，并且不需要昂贵的服务器成本。

Gridsome使用超快速静态站点生成器，JavaScript和API的强大功能来创建令人惊叹的动态Web体验。

Gridsome站点在转换成一个完全由Vue.js支持的SPA之前作为静态HTML加载。这使得搜索引擎能够抓取内容并给出更好的搜索引擎优化排名，并且仍然拥有Vue.js的所有功能。

![](https://user-gold-cdn.xitu.io/2020/2/14/1704450d6d88b0b4?w=1024&h=443&f=png&s=29836)

# 3. 快速入门

## 3.1. 先决条件

您应该具有有关HTML，CSS，Vue.js以及如何使用Terminal的基本知识。了解GraphQL的工作原理是有好处的，但不是必需的。

Gridsome需要Node.js（v8.3 +）。

## 3.2. 安装Gridsome CLI工具

```
npm install --global @gridsome/cli
```

## 3.3. 创建一个Gridsome项目

```
gridsome create my-gridsome-site #创建一个新项目
cd my-gridsome-site #进入文件夹
gridsome develop #在以下位置启动本地开发服务器 http://localhost:8080
```
如果我们尝试更改此布局页面上的任何内容，那么我们将看到它会自动更改屏幕上的内容。这是我们之前谈到的Gridsome Hot Reloading功能的结果。

