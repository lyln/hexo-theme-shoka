# Hexo Theme Shoka

## Usage

1. Clone this repository

``` bash
# cd your-blog
git clone https://github.com/amehime/hexo-theme-shoka.git ./themes/shoka
```

2. Make changes to the root `_config.yml`
  - update `theme` fragment as `shoka`.
  - add the following fragments
  ```
  logo: Yume Shoka
  email: you@example.com
  category_map:
  ```

3. Install the necessary plugins
  - [hexo-renderer-multi-markdown-it](https://www.npmjs.com/package/hexo-renderer-multi-markdown-it)
  - [hexo-autoprefixer](https://www.npmjs.com/package/hexo-autoprefixer)
  - [hexo-algoliasearch](https://www.npmjs.com/package/hexo-algoliasearch)
  - [hexo-symbols-count-time](https://www.npmjs.com/package/hexo-symbols-count-time)
  - [hexo-feed](https://www.npmjs.com/package/hexo-feed)

4. Make changes to the theme `_config.yml`


## 模版修改
插件安装
```
npm un hexo-renderer-marked --save
npm i hexo-renderer-multi-markdown-it --save

npm install hexo-autoprefixer --save
npm install hexo-symbols-count-time

npm install hexo-feed --save-dev
```


## Hexo 主题 Shoka 食用说明

安装依赖插件
```
npm un hexo-renderer-marked --save
npm i hexo-renderer-multi-markdown-it --save

```


首页显示模式

模版_config.yml
```
index:
  mode: category #or category
```

站点_config.yml
```
category_dir: /

#permalink: :year/:month/:day/:title/
permalink: :title/

同时配置对应的分类

category_map:
  产品设计: pm-note

```

md文件存放位置
```
source/_posts/pm-note

cover.jpg
xx.md 直接放置到分离文件夹下

文章设置分类

---
title: 界面设计
date: 2020-08-11 
categories:
  - ["产品设计"]
tags:
---

```


### 问题解决

```
TypeError: Cannot read property 'querySelector' of null
app.js
这段先注释掉
  // TOC item animation navigate.
  // link.addEventListener('click', clickScroll);
  // anchor.querySelector('a.anchor').addEventListener('click', clickScroll);
  // return anchor;

```
