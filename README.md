# Hexo 主题 Shoka 食用说明
[鱼干的小雨塘](https://yoogan.github.io/)

[电影小站](https://v.inshub.cn/)
1. 下载主题

``` bash
# cd your-blog
git clone https://github.com/lyln/hexo-theme-shoka.git ./themes/shoka
```

2. 修改网站 `_config.yml`
  - update `theme` fragment as `shoka`.
  - add the following fragments

修改主题显示为文件夹模式。

站点_config.yml
```
category_dir: /

#permalink: :year/:month/:day/:title/
permalink: :title/

同时配置对应的分类

category_map:
  产品设计: pm-note

```

文章设置分类
```
---
title: 界面设计
date: 2020-08-11 
categories:
  - ["产品设计"]
tags:
---
```
3. 插件安装
  - [hexo-renderer-multi-markdown-it](https://www.npmjs.com/package/hexo-renderer-multi-markdown-it)
  - [hexo-autoprefixer](https://www.npmjs.com/package/hexo-autoprefixer)
  - [hexo-algoliasearch](https://www.npmjs.com/package/hexo-algoliasearch)
  - [hexo-symbols-count-time](https://www.npmjs.com/package/hexo-symbols-count-time)
  - [hexo-feed](https://www.npmjs.com/package/hexo-feed)

```
npm un hexo-renderer-marked --save
npm i hexo-renderer-multi-markdown-it --save

npm install hexo-autoprefixer --save
npm install hexo-symbols-count-time
npm install hexo-algoliasearch

npm install hexo-feed --save-dev
```


4. 修改主题 `_config.yml`

模版_config.yml
```
index:
  mode: category #or category
```

md文件存放位置
```
source/_posts/pm-note

cover.jpg
xx.md 直接放置到分离文件夹下

```

5. 新增云撸猫
```
npm install --save hexo-helper-live2d

cnpm install live2d-widget-model-hijiki

https://huaji8.top/post/live2d-plugin-2.0/


live2d:
  enable: true
  scriptFrom: local
  pluginRootPath: live2dw/
  pluginJsPath: lib/
  pluginModelPath: assets/
  tagMode: false
  debug: false
  model:
    use: live2d-widget-model-hijiki
  display:
    position: right
    width: 150
    height: 300
  mobile:
    show: true
  react:
    opacity: 0.7

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
### 站点效果
[鱼干的小雨塘](https://yoogan.github.io/)

### 其他
需要其他帮助的欢迎一起探讨。
0成本构建自己的电影网站，[电影小站](https://v.inshub.cn/)。
![qr](https://lyln.oss-cn-beijing.aliyuncs.com/wx/qr-wx.jpg?430*430)
