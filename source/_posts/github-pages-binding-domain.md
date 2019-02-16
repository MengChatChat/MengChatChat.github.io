---
title: Github Pages绑定域名
index_img: ../post_img/github.png
tags: [工具, hexo, Github Pages]
---
Github Pages的默认域名是github的二级域名username.github.com或者username.github.io，需要绑定自己的独立域名的话也非常简单，只要以下两步：

### 一、增加CNAME

在你的git仓库创建一个CNAME文件，内容写你的域名。比如我的域名是blog.mengwj.com，在CNAME文件写入“blog.mengwj.com”就好了。

#### 1.创建一个CNAME文件
<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/1-1.png)
</div>

#### 2.内容写你的域名
<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/1-2.png)
</div>

#### 3.Hexo生成完毕后自动部署网站
``` bash
$ hexo generate --deploy
```
简写
``` bash
$ hexo g -d
```

<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/1-3.png)
</div>

<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/1-4.png)
</div>

<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/1-5.png)
</div>


### 二、域名解析

#### 1.获取Github Pages域名的ip

首先获取你Github Pages域名的ip，比如你的Github pages域名为mengchatchat.github.io，执行一下命令：

``` bash
$ ping mengchatchat.github.io
```

你应该可以得到一个IP，比如IP是207.97.227.245。

<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/2-1.png)
</div>

#### 2.增加一条A记录到该IP

最后去你的域名注册商后台，增加一条A记录到该IP就好了。

<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/3-1.png)
</div>
<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/3-2.png)
</div>
<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/3-3.png)
</div>
<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/3-4.png)
</div>
<div align="center">
    ![GitHub Pages image](/post_img/github_pages_binding_domain/3-5.png)
</div>
