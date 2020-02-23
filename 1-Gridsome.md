Gridsome
===

- [Gridsome](#gridsome)
- [1. 简介](#1-%e7%ae%80%e4%bb%8b)
- [2. 原理](#2-%e5%8e%9f%e7%90%86)
- [3. 快速入门](#3-%e5%bf%ab%e9%80%9f%e5%85%a5%e9%97%a8)
  - [3.1. 先决条件](#31-%e5%85%88%e5%86%b3%e6%9d%a1%e4%bb%b6)
  - [3.2. 安装Gridsome CLI工具](#32-%e5%ae%89%e8%a3%85gridsome-cli%e5%b7%a5%e5%85%b7)
  - [3.3. 创建一个Gridsome项目](#33-%e5%88%9b%e5%bb%ba%e4%b8%80%e4%b8%aagridsome%e9%a1%b9%e7%9b%ae)
- [4. 目录结构](#4-%e7%9b%ae%e5%bd%95%e7%bb%93%e6%9e%84)
  - [4.1. root 目录](#41-root-%e7%9b%ae%e5%bd%95)
  - [4.2. /src 目录](#42-src-%e7%9b%ae%e5%bd%95)
  - [4.3. /static 目录](#43-static-%e7%9b%ae%e5%bd%95)
  - [4.4. 其他目录](#44-%e5%85%b6%e4%bb%96%e7%9b%ae%e5%bd%95)
- [5. 项目配置](#5-%e9%a1%b9%e7%9b%ae%e9%85%8d%e7%bd%ae)
- [6. 页面](#6-%e9%a1%b5%e9%9d%a2)
  - [6.1. 基于文件的页面](#61-%e5%9f%ba%e4%ba%8e%e6%96%87%e4%bb%b6%e7%9a%84%e9%a1%b5%e9%9d%a2)
  - [6.2. 编程方式创建页面](#62-%e7%bc%96%e7%a8%8b%e6%96%b9%e5%bc%8f%e5%88%9b%e5%bb%ba%e9%a1%b5%e9%9d%a2)
  - [6.3. 动态路由](#63-%e5%8a%a8%e6%80%81%e8%b7%af%e7%94%b1)
  - [6.4. 页面元信息](#64-%e9%a1%b5%e9%9d%a2%e5%85%83%e4%bf%a1%e6%81%af)
  - [6.5. 自定义404页面](#65-%e8%87%aa%e5%ae%9a%e4%b9%89404%e9%a1%b5%e9%9d%a2)
- [7. 集合](#7-%e9%9b%86%e5%90%88)
  - [7.1. 添加集合](#71-%e6%b7%bb%e5%8a%a0%e9%9b%86%e5%90%88)
  - [7.2. 使用Source plugins添加集合](#72-%e4%bd%bf%e7%94%a8source-plugins%e6%b7%bb%e5%8a%a0%e9%9b%86%e5%90%88)
  - [7.3. 使用Data Store API添加集合](#73-%e4%bd%bf%e7%94%a8data-store-api%e6%b7%bb%e5%8a%a0%e9%9b%86%e5%90%88)
  - [7.4. 在GraphQL中的集合](#74-%e5%9c%a8graphql%e4%b8%ad%e7%9a%84%e9%9b%86%e5%90%88)
    - [7.4.1. 自动生成Schema](#741-%e8%87%aa%e5%8a%a8%e7%94%9f%e6%88%90schema)
    - [7.4.2. 探索可用的类型和字段](#742-%e6%8e%a2%e7%b4%a2%e5%8f%af%e7%94%a8%e7%9a%84%e7%b1%bb%e5%9e%8b%e5%92%8c%e5%ad%97%e6%ae%b5)
- [8. 模板](#8-%e6%a8%a1%e6%9d%bf)
  - [8.1. 安装模板](#81-%e5%ae%89%e8%a3%85%e6%a8%a1%e6%9d%bf)
  - [8.2. 将数据添加到模板](#82-%e5%b0%86%e6%95%b0%e6%8d%ae%e6%b7%bb%e5%8a%a0%e5%88%b0%e6%a8%a1%e6%9d%bf)


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

```
git clone https://github.com/drehimself/gridsome-portfolio-starter
npm config set sharp_dist_base_url https://npm.taobao.org/mirrors/sharp-libvips/v8.8.1/
npm i --registry=https://registry.npm.taobao.org

```



# 4. 目录结构

基本的Gridsome项目的结构如下：
```
.
├── package.json
├── gridsome.config.js
├── gridsome.server.js
├── static/
└── src/
    ├── main.js
    ├── index.html
    ├── App.vue
    ├── layouts/
    │   └── Default.vue
    ├── pages/
    │   ├── Index.vue
    │   └── Blog.vue
    └── templates/
        └── BlogPost.vue
```

## 4.1. root 目录

* `package.json` 包含有关项目中安装了哪些插件的信息。

* `gridsome.config.js` 该文件包含已安装插件的配置和选项。

* `gridsome.server.js` 该文件是可选的，用于挂接到Gridsome服务器的各个部分。该文件必须导出可以访问API的函数。

## 4.2. /src 目录

* `Main.js` 在此处导入全局样式和脚本。该文件还具有可以访问Client API的导出功能。该文件是安装Vue插件，注册组件和指令等的地方。

* `Layouts目录` 如果要共享页面或模板的一个或多个布局，请在此目录中创建组件。

* `Pages目录` 该目录中的所有组件均成为您网站的页面。每个页面将根据其.vue文件的位置获得其路径。 `src/pages/Index.vue`将成为您网站的主页，而`src/pages/AboutUs.vue`将成为`example.com/about-us`。

* `Templates目录` 如果要将外部数据源（例如来自WordPress博客的帖子）导入到项目中，则每个帖子都会在此目录中寻找其模板的组件。组件文件的名称必须与GraphQL模式中的节点类型匹配。

* `自定义index.html` 有时，您将需要覆盖Gridsome用于生成页面的基本HTML模板。Gridsome使这变得非常容易。您要做的就是在src目录中创建一个新的index.html文件。

* `自定义App.vue` 该App.vue文件是包装所有页面和模板的主要组件。您可以通过App.vue在src目录中拥有自己的文件来覆盖默认文件。如果要在所有页面之间共享布局，则覆盖默认值很有用。

了解有关覆盖App.vue的更多信息

## 4.3. /static 目录
此目录中的文件将dist在构建期间直接复制到。例如，/ static / robots.txt将位于https://yoursite.com/robots.txt

* Aliases 在Gridsome中，您可以使用别名~或@链接到文件/src夹内的文件。例如，您可以使用以下命令导入Vue组件`import Card from '~/components/Card'`

## 4.4. 其他目录

* `Assets` 全局样式，图像，字体和图标通常添加到src/assets目录中。

* `Shared or global components` 您可以在多个页面或模板中使用的组件可以存储在src/components目录中。

* `Data files` 您可以将诸如.json或.yaml想要导入到组件中的数据文件存储在src/data目录中。


# 5. 项目配置

Gridsome需要gridsome.config.js才能工作。插件配置和项目设置都是在这个文件当中。基本配置文件如下所示：
```
module.exports = {
  siteName: 'Gridsome',
  siteUrl: 'https://www.gridsome.org',
  plugins: []
}
```

* siteName 为您的项目设置一个名称。该名称通常在标题标签中使用

* siteDescription 为您的项目设置描述

* siteUrl 通常用于设置站点的域的根目录

* host 运行时主机

* port 运行时端口

* outputDir 当运行`gridsome build`时，将在其中生成生产构建文件的目录

* pathPrefix Gridsome假定您的项目是从域的根目录提供的。如果您的项目将托管在名为`/my-app`的子目录中，请更改此选项`my-app`

* titleTemplate 默认 `%s - <siteName>`，用于设置标题的模板。在页面中设置的元信息，会替换这个%s占位符

* plugins 通过将插件添加到plugins数组来激活插件
```
module.exports = {
  plugins: [
    {
      use: '@gridsome/source-filesystem',
      options: {
        path: 'blog/**/*.md',
        route: '/blog/:year/:month/:day/:slug',
        typeName: 'Post'
      }
    }
  ]
}
```

* templates 定义集合的路由和模板

* metadata 将全局元数据添加到GraphQL schema

* icon 默认情况下会使用位于`src/favicon.png`作为favicon和touchicon。但也可以定义其他路径或大小，图标应为正方形，最小16个像素
```
module.exports = {
  icon: './src/my-icon.png'
}
```
* configureWebpack 如果该选项是一个对象，它将与内部配置合并。
```
module.exports = {
  configureWebpack: {
    // merged with the internal config
  }
}
```
如果该选项是一个函数，它将获得内部配置作为其第一个参数。您可以修改参数或返回一个新的配置对象，该对象将覆盖内部webpack配置。
```
const merge = require('webpack-merge')

module.exports = {
  configureWebpack(config) {
    return merge({ /* custom config */ }, config)
  }
}
```

* chainWebpack 该函数将接收由webpack-chain提供支持的ChainableConfig实例

* runtimeCompiler 在运行时包括Vue模板编译器

* configureServer 配置开发服务器

* permalinks.trailingSlash 启用此选项后，具有动态路由的页面将不包含斜杠，并且服务器上必须具有额外的重写规则才能正常工作。此外，的静态路径<g-link>不会自动包含尾部斜杠，而应包含在路径中：
```
<g-link to="/about-us/">About us</g-link>
```
* permalinks.slugify 使用自定义的Slugify方法。默认slugifyer是`@sindresorhus/slugify`。
```
module.exports = {
  permalinks: {
    slugify: {
      use: 'another-slugify-library',
      options: {}
    }
  }
}
```
* css.split 将CSS分成多个块。默认情况下禁用拆分。拆分CSS可能会导致奇怪的行为

* css.loaderOptions 将选项传递给与CSS相关的加载程序。例如：
```
module.exports = {
  css: {
    loaderOptions: {
      scss: {
        // options here will be passed to sass-loader
      },
      less: {
        // options here will be passed to less-loader
      }
    }
  }
}
```

# 6. 页面

页面负责在URL上显示您的数据。

每个页面将静态生成，并具有自己的index.html带有标记的文件。

在Gridsome中创建页面有两个选择：

1. 使用file system  - 用单文件组件创建页面。
2. 使用Pages API  - 用编程方式创建页面。

## 6.1. 基于文件的页面

`src/page`s目录中的单文件组件将自动转换成它的URL。

文件位置用于生成URL，以下是一些基本示例：

* `src/pages/Index.vue` 变成 `/`（首页）
* `src/pages/AboutUs.vue` 变成 `/about-us`
* `src/pages/about/Vision.vue` 变成 `/about/vision`
* `src/pages/blog/Index.vue` 变成 `/blog`

一个简单的页面组件可能看起来像这样：
```html
<template>
  <div>
    <h1>Hello, world!</h1>
  </div>
</template>
```
`src/pages`中的页面通常用于固定网址，例如`/about`；或用于列出博客文章，例如`/blog`。

## 6.2. 编程方式创建页面

可以使用`gridsome.server.js`中的`createPages`钩子，以编程方式创建页面。

如果您想从外部API手动创建页面而不使用GraphQL数据层，这很有用。
```
module.exports = function (api) {
  api.createPages(({ createPage }) => {
    createPage({
      path: '/my-page',
      component: './src/templates/MyPage.vue'
    })
  })
}
```

## 6.3. 动态路由

页面可以具有动态路由。对于仅需要客户端路由的页面，动态路由很有用。

例如，用户页面根据URL中的片段，从外部API获取信息。

## 6.4. 页面元信息

Gridsome使用vue-meta处理有关页面的元信息。
```html
<template>
  <div>
    <h1>Hello, world!</h1>
  </div>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!',
    meta: [
      { name: 'author', content: 'John Doe' }
    ]
  }
}
</script>
```

## 6.5. 自定义404页面

创建一个`src/pages/404.vue`组件，即可自定义404页面。


# 7. 集合

集合是一组节点，每个节点都包含带有自定义数据的字段。如果您要在网站上放置博客文章，标签，产品等，则集合很有用。

## 7.1. 添加集合

集合可以通过`Source plugins`添加，也可以使用`Data Store API`自己完成。

集合在development和build期间存储在本地内存数据存储中。

节点可以来自本地文件（Markdown，JSON，YAML等）或任何外部的API。

![](https://gridsome.org/assets/static/node-pages.0eae6d2.8581c59dbb258143a7ffcebb617ec5dc.png)

## 7.2. 使用Source plugins添加集合

将集合添加到Gridsome的最简单方法是使用`Source plugins`。

本示例从WordPress网站创建集合。`Source plugins`的`typeName`选项通常用于集合名称添加前缀。
```js
// gridsome.config.js
module.exports = {
  plugins: [
    {
      use: '@gridsome/source-wordpress',
      options: {
        baseUrl: 'YOUR_WEBSITE_URL',
        typeName: 'WordPress',
      }
    }
  ]
}
```
您可以在 `https://gridsome.org/plugins` 上浏览源插件。

## 7.3. 使用Data Store API添加集合

您可以从任何外部API手动添加集合。

本示例创建一个名为Post的集合，该集合从API获取内容，并将结果作为节点添加到该集合。
```js
// gridsome.server.js
const axios = require('axios')

module.exports = function (api) {
  api.loadSource(async actions => {
    const collection = actions.addCollection('Post')

    const { data } = await axios.get('https://api.example.com/posts')

    for (const item of data) {
      collection.addNode({
        id: item.id,
        title: item.title,
        content: item.content
      })
    }
  })
}
```


## 7.4. 在GraphQL中的集合

每个集合将向 `GraphQL Schema` 添加两个根字段，这些根字段用于检索页面中的节点。

字段名称是根据集合名称自动生成的。如果为集合命名Post，则在 Schema 中将具有以下可用字段：

* post 通过单个id获取节点。
* allPost 获取节点列表。（可以排序和过滤。）

### 7.4.1. 自动生成Schema

Schema中的每个集合类型都将具有基于启动时发现的数据自动生成的字段。

这对于简单的项目非常有用，但由于内容已从外部源中删除，因此通常会导致错误，例如缺少字段。您可以使用Schema API定义自己的架构，该架构在数据更改时将保留。

集合的自定义架构类型必须实现该Node接口。

### 7.4.2. 探索可用的类型和字段

您可以通过在GraphQL资源管理器中打开Schema选项卡来浏览可用字段。


# 8. 模板

模板用于为集合中的节点创建单个页面。节点需要相应的页面才能显示在其自己的URL上。

## 8.1. 安装模板

以下示例显示了如何为名为Post的集合设置路由和模板。

如果没有明确指定的话，位于`src/templates/{Collection}.vue`将默认用作模板。
```js
// gridsome.config.js
module.exports = {
  templates: {
    Post: '/blog/:year/:month/:title',
  }
}
```

指定自定义组件的路径：
```js
// gridsome.config.js
module.exports = {
  templates: {
    Post: [
      {
        path: '/blog/:year/:month/:title',
        component: './src/other/location/Post.vue'
      }
    ]
  }
}
```

为一个集合设置多个模板：
```js
// gridsome.config.js
module.exports = {
  templates: {
    Product: [
      {
        path: '/product/:slug',
        component: './src/templates/Product.vue'
      },
      {
        name: 'reviews',
        path: '/product/:slug/reviews',
        component: './src/templates/ProductReviews.vue'
      }
    ]
  }
}
```

> **slugify**  
> GitHub:https://github.com/sindresorhus/slugify  
> 对于URLs、文件名和IDs很实用的Js处理类。它正确处理德语变音符号，越南语，阿拉伯语，俄语，罗马尼亚语，土耳其语等。  
> 安装  
> `npm install @sindresorhus/slugify`  
> 用法  
> `const slugify = require('@sindresorhus/slugify'); `
> `slugify('I ♥ Dogs');`  
> `//=> 'i-love-dogs'`  
> `slugify('  Déjà Vu!  ');`  
> `//=> 'deja-vu'`  
> `slugify('fooBar 123 $#%');`  
> `//=> 'foo-bar-123'`  

模板路径可以是在 `GraphQL schema` 中带有一个path字段。使用to参数获取集合的其他模板的路径。
```js
query ($id: ID!) {
  product(id: $id) {
    path               # path to the default template
    path(to:"reviews") # path to the reviews template
  }
}
```

可用的模板选项：

* path - 定义动态路由，并使用任何节点字段作为参数。
* component - 指定要用作每个页面模板的组件。
* name - 为模板指定名称，以获取GraphQL中的路径。

默认情况下，路径参数为slugified（分段值），但是可以通过添加_raw后缀来使用原始值，例如:title_raw。通过使用双下划线（__）分隔属性或索引来访问深层对象或数组中的值。date字段有一组语法 :year，:month和:day。

* :id 决心 node.id
* :value解析为node.value（分段值）
* :value_raw解析为node.value（原始值）
* :object__value 决心 node.object.value
* :array__3__id 决心 node.array[3].id

path选项也可以是一个函数，该函数接收节点作为第一个参数并返回路径。
```js
// gridsome.config.js
module.exports = {
  templates: {
    Post: [
      {
        path: (node) => {
          return `/product/${node.slug}/reviews`
        }
      }
    ]
  }
}
```
每个节点都会在 GraphQL schema 中获得一个包含path字段的，生成的URL。

## 8.2. 将数据添加到模板

根据templates配置生成的页面将在该块中将节点id用作查询变量page-query。使用$id变量获取当前页面的节点：

<template>
  <div>
  	<h1 v-html="$page.post.title" />
  	<div v-html="$page.post.content" />
  </div>
</template>

<page-query>
query ($id: ID!) {
  post(id: $id) {
    title
    content
  }
}
</page-query>
其他节点字段也可用作查询变量。通过使用双下划线（__）分隔属性或索引来访问深层对象或数组中的值。

$id 决心 node.id
$value 决心 node.value
$object__value 决心 node.object.value
$array__3__id 决心 node.array[3].id
＃节点字段作为元信息
该metaInfo选项必须是一个函数才能访问查询结果：

<script>
export default {
  metaInfo() {
    return {
      title: this.$page.post.title
    }
  }
}
</script>