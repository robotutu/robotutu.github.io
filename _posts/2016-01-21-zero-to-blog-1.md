---
layout: post
title: 菜鸡零基础建博客指南（上）
description: 艰辛历程
tags: [blog, jekyll, github, github pages]
image:
  feature: pic-zero-to-blog-1.jpg
  credit:
  creditlink:
---

# 菜鸡零基础建博客指南（上）

最近突然心血来潮，想做个网(博)站(客)。虽然现在建成了也没什么可写的，但是整个过程中也是收获颇多。希望这个指南可以帮到和我一样几乎 **零基础** 但又想 **建博客** 的朋友。😁

指南将分为上、下两部分。上篇有整个过程中用到的工具、流程以及个人理解的原理；下篇则是一些具体操作、遇到的问题以及总结。

---

### 使用的工具
- [Shadowsocks](https://portal.shadowsocks.com/aff.php?aff=4491){:target="blank"}
<br>干掉 GFW 的工具，建议全程翻墙
- [GitHub](https://github.com/){:target="blank"}
<br>分布式版本控制系统和开源代码库 *（其实不懂是什么意思，扩展：[版本控制](http://blog.jobbole.com/55304/){:target="blank"}）*，并提供了 [Github Pages](https://pages.github.com/) 服务，我们并不需要额外做什么就可以直接享受这项服务
- [Jekyll](http://jekyll.bootcss.com/){:target="blank"}
<br>将纯文本转化为静态网站和博客的工具
- [JekyllThemes](http://jekyllthemes.org/){:target="blank"}
<br>提供了很多成熟的博客模板，可以直接使用并修改
- [Atom](https://atom.io/)
<br>文本代码编辑器，也可以用别的，网上普遍评价是文件太大时会直接崩掉，不过作为菜鸡文件暂时没那么大，用起来感觉很好
- [GoDaddy](https://www.godaddy.com/){:target="blank"}
<br>购买、管理域名的地方

---

### 建博客流程

#### 1. 注册 Github 账号
Username 将出现在你默认的博客网址中： *<u>urUsername.github.io</u>*
<div markdown="0"><a href="https://github.com/join" class="btn btn-success" target="blank">Sign up</a></div>

#### 2. 新建 Github 仓库
唔...好像是叫仓库...在 Repository name 输入框中输入`urUsername.github.io`，urUsername 就是你的用户名，其他的不用填，点击 Create repository 按钮。
![如图：](/article_pic/zero-to-blog-1.png){: .image-right}

找不到入口的话猛击下方按钮
<div markdown="0"><a href="https://github.com/new" class="btn btn-success" target="blank">+ Repository</a></div>

### 3. 下载 jekyll 博客模板
打开 [JekyllThemes](http://jekyllthemes.org/){:target="blank"}，从 demo 里挑一个喜欢的模板，下载并解压。

### 4. 安装所需环境


### 5. 上传发布博客


#### 个人理解的原理
- 使用 GitHub 及 GitHub Pages 生成一个 *urgithubname.github.io* 的网站（但里面什么都没有，空空如也）。
- 使用 jekyll 在
