
## 陕西本初网络科技有限公司前端测试题

<br>

<p align="center">
公司使用了大量SPA单页web应用技术，需要对vue2 webpack  npm 有较为深入的了解。
</p>

### 页面无刷新效果

<p align="center">

[![Build Status](https://travis-ci.org/jeneser/douban.svg?branch=master)](https://travis-ci.org/jeneser/douban) [![David](https://img.shields.io/david/expressjs/express.svg?style=flat-square)](https://github.com/jeneser/douban) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/aa2dd7f4191546258edf6e55464d1962)](https://www.codacy.com/app/jeneser/douban?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=jeneser/douban&amp;utm_campaign=Badge_Grade) [![Powered](https://img.shields.io/badge/Powered%20by-vue2%2B-brightgreen.svg)](https://github.com/vuejs/vue) [![Percentage of issues still open](http://isitmaintained.com/badge/open/jeneser/douban.svg)](http://isitmaintained.com/project/jeneser/douban "Percentage of issues still open") [![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/jeneser/douban.svg)](http://isitmaintained.com/project/jeneser/douban "Average time to resolve an issue") [![PR](https://img.shields.io/badge/PR-welcome-brightgreen.svg)](https://github.com/jeneser/douban/pulls) [![license](https://img.shields.io/badge/license-MIT-brightgreen.svg)](https://github.com/jeneser/douban/blob/master/LICENSE)

</p>
<br>

<p align="center">
    <img src="https://raw.githubusercontent.com/jeneser/jeneser.github.io/master/assets/images/douban/douban_home.gif" >
    <img src="https://raw.githubusercontent.com/jeneser/jeneser.github.io/master/assets/images/douban/douban_movie.gif" >
    <br>
     <img src="https://raw.githubusercontent.com/jeneser/jeneser.github.io/master/assets/images/douban/douban_login.gif" >
    <img src="https://raw.githubusercontent.com/jeneser/jeneser.github.io/master/assets/images/douban/douban_search.gif" >
    <br><br>
    <strong>......</strong>
    <br>
	 <strong><a href="https://jeneser.github.io/douban/">Live Demo</a></strong>
</p>


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## 测试题目 （约20分钟完成）

1. 创建一个新的路由 `ibenchu`
2. 使用该接口填充数据，数据需要正常展示出来，对样式没有要求 [大陆票房](https://apicloud.mob.com/boxoffice/day/query?key=1eae6b9688738&area=CN)
3. 在该项目的首页（豆瓣）加上跳转到这个页面的方式（不得使用A标签）



## 相关技术

- [Vuex](https://vuex.vuejs.org) : Centralized State Management for Vue.js
- [Vue-router](http://router.vuejs.org/) : The official router for Vue.js
- ~~[vue-resource](https://github.com/pagekit/vue-resource) : The HTTP client for Vue.js~~
- [Superagent](https://github.com/visionmedia/superagent) : Ajax with less suck - (and node.js HTTP client to match)
- [vue-infinite-loading](https://github.com/PeachScript/vue-infinite-loading) : An infinite scroll plugin for Vue.js 1.0 & Vue.js 2.0.
- [normalize.css](https://github.com/necolas/normalize.css) :  A collection of HTML element and attribute style-normalizations
- [vue-scroll-behavior](https://www.npmjs.com/package/vue-scroll-behavior) :  Completely customize the scroll behavior on route navigation

## API

Douban Api V2
- Basic URI : `https://api.douban.com/V2/`
- Online activities
  - Activities list : `/event/list?loc=108288&count=&start=`
  - Single activitie info : `/event/id`
- Movie
  - In theaters : `/movie/in_theaters?count=`
  - Coming soon : `/movie/coming_soon?count=`
  - Top 250 : `/movie/top250?count=`
  - Single movie info : `/movie/subject/id`
- Book
  - Search some books : `/book/search?q=&count=`
  - Single book info : `/book/id`
- Search
  - Search books : `/book/search?q=`
  - Search movie : `/movie/search?q=`
  - Search music : `/music/search?q=`

Mock Douban Backend
- User Basic URI : `https://douban.herokuapp.com/user/`
- Register
  - Path: `/user`
  - method: `POST`
- Login
  - Path: `/user/:id`
  - method: `GET`

For detailed explanation, checkout the [Douban Api V2](https://developers.douban.com/wiki/?title=api_v2) and [Douban Backend](https://github.com/jeneser/douban-backend)

## 目录
```
.
├── build
│   ├── build.js
│   ├── check-versions.js
│   ├── dev-client.js
│   ├── dev-server.js
│   ├── utils.js
│   ├── vue-loader.conf.js
│   ├── webpack.base.conf.js
│   ├── webpack.dev.conf.js
│   └── webpack.prod.conf.js
├── config
│   ├── dev.env.js
│   ├── index.js
│   └── prod.env.js
├── index.html
├── LICENSE
├── package.json
├── README.md
├── src
│   ├── App.vue
│   ├── assets
│   │   ├── avatar.png
│   │   ├── book_zw.jpg
│   │   ├── camera.svg
│   │   ├── douban-app-logo.png
│   │   ├── pen.svg
│   │   ├── promotion_bg.jpg
│   │   └── user_normal.jpg
│   ├── components
│   │   ├── Banner.vue
│   │   ├── Card.vue
│   │   ├── DownloadApp.vue
│   │   ├── Group.vue
│   │   ├── HeaderBar.vue
│   │   ├── List.vue
│   │   ├── Rating.vue
│   │   ├── Scroller.vue
│   │   ├── Marking.vue
│   │   ├── SubNav.vue
│   │   ├── Tags.vue
│   │   ├── Types.vue
│   │   └── UserBar.vue
│   ├── main.js
│   ├── router
│   │   └── index.js
│   ├── store
│   │   ├── index.js
│   │   └── modules
│   │       ├── activities.js
│   │       ├── book.js
│   │       ├── group.js
│   │       ├── movie.js
│   │       ├── search.js
│   │       ├── subject.js
│   │       └── user.js
│   └── views
│       ├── BookView.vue
│       ├── DetailView.vue
│       ├── GroupView.vue
│       ├── HomeView.vue
│       ├── LoginView.vue
│       ├── MovieView.vue
│       ├── PagesView.vue
│       ├── RegisterView.vue
│       ├── SearchView.vue
│       ├── StatusView.vue
│       ├── SubjectView.vue
│       └── TalionView.vue
└── static
    └── logo.png
```

