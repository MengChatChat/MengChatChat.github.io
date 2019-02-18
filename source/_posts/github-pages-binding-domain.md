---
title: Github Pages绑定域名
index_img: ../post_img/github.png
tags: [工具, hexo, Github Pages]
---
Github Pages的默认域名是github的二级域名username.github.com或者username.github.io，需要绑定自己的独立域名的话也非常简单，只要以下两步：

### 一、增加CNAME

在你的git仓库创建一个CNAME文件，内容写你的域名。比如我的域名是blog.mengwj.com，在CNAME文件写入“blog.mengwj.com”就好了。

#### 1.创建一个CNAME文件

![GitHub Pages image](/post_img/github_pages_binding_domain/1-1.png)


#### 2.内容写你的域名

![GitHub Pages image](/post_img/github_pages_binding_domain/1-2.png)

#### 3.Hexo生成完毕后自动部署网站

``` bash
$ hexo generate --deploy
```

简写

``` bash
$ hexo g -d
```

![GitHub Pages image](/post_img/github_pages_binding_domain/1-3.png)

![GitHub Pages image](/post_img/github_pages_binding_domain/1-4.png)

![GitHub Pages image](/post_img/github_pages_binding_domain/1-5.png)

### 二、域名解析

#### 1.增加一条CNAME记录

增加一条CNAME记录到该xx.github.io。到你的域名注册商后台，正确解析是使用CNAME将你的域名解析到 xx.github.io，不要使用A记录解析到ip。我这里配置了子域blog。

![GitHub Pages image](/post_img/github_pages_binding_domain/3-1.png)

![GitHub Pages image](/post_img/github_pages_binding_domain/3-2.png)

![GitHub Pages image](/post_img/github_pages_binding_domain/3-3.png)

![GitHub Pages image](/post_img/github_pages_binding_domain/3-4.png)

![GitHub Pages image](/post_img/github_pages_binding_domain/3-5.png)

---

这是别人的设置，也可以参考一下，没有配置子域，而是直接使用www的。

![GitHub Pages image](/post_img/github_pages_binding_domain/3-7.png)


另外，需要注意的问题是，如果使用A记录解析到ip，则会每次发文章，都会收到github的邮件，如下：

![GitHub Pages image](/post_img/github_pages_binding_domain/3-6.png)

或者如下:

![GitHub Pages image](/post_img/github_pages_binding_domain/3-8.png)