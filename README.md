# 本主题完全模仿自`Jerry Qu`的[博客](https://imququ.com/)

# 本主题完全模仿自`Jerry Qu`的[博客](https://imququ.com/)

# 本主题完全模仿自`Jerry Qu`的[博客](https://imququ.com/)

---

# hexo-theme-veni

请将主题目录下`other`文件夹内所有文件夹复制到博客根目录`/source`下，根目录的`_config.yml` 可参考主题目录下的`_config.root.example.yml`进行修改

需要`hexo-generator-feed hexo-renderer-sass`这两个模块。

另外nodejs版本需要14以上。

## 根目录 _config.yml 配置
```
title: 博客名称，同时也是页面title
subtitle: 博客子标题，位于页面左侧导航昵称下面
author: 作者名称
lauguage: 语言选项，中文默认 zh-CN
timezone: 时区，默认Asia/Shanghai
start_year: 博客建立时间，显示在footer里版权部分

代码高亮部分:
highlight 和 prismjs 二选一，两者都启用时highlight优先
相关配置请自行查阅文档，主题部分参见下方主题文件夹内的`_config.yml`

使用`prismjs`时请在代码片段开头加上语言类型，如下:

```shell
sudo apt update
```


theme: hexo-theme-veni


```

## 主题目录下 _config.yml

```
user:
    avatar: 头像链接

post:
    expired_day: 文章过期提示期限，单位为天

aside:
    bg: 左侧导航背景链接
    width: 左侧导航宽度

nav:
    index: 首页
    categories: 分类
    tags: 标签
    chaos: 混沌
    archives: 归档
    blogroll: 友链
    about: 关于
        path: 左侧导航链接
        status: 是否显示
        intro: 进入相应页面后的简介

subnav:
    左侧导航栏底部ICON配置，建议使用镂空png图片
    name:
        path: 跳转链接
        icon: 图片链接
        color: 背景颜色
        style: style字符串

archives:
    sort: 归档排序方式，可选desc(从近期到早期), asc(从早期到近期)

blogroll:
    友链配置
    list:
        - blogname: 友链博客名称
          link: 链接
          info: 博客简介
          ssl: 是否启用了https，为true时博客名称前会出现一把小绿锁

chaos:
    混沌配置
    - name: 名称
      link: 链接
      info: 简介

highlight:
prismjs:
    style: xxx
    url: xxx

如果提供了主题url，则使用提供的主题
否则将使用jsdelivr的链接，此时必须提供主题名称即style，主题名称将嵌入如下cdn链接内:

//cdn.jsdelivr.net/gh/highlightjs/cdn-release@10.3.2/build/styles/<%= theme.highlight.style %>.min.css

//cdn.jsdelivr.net/npm/prismjs@1.22.0/themes/<%= theme.prismjs.style %>.css
```