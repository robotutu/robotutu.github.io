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

菜鸡零基础建博客指南（上）

最近突然心血来潮，想做个网(博)站(客)。虽然现在建成了也没什么可写的，但是整个过程中也是收获颇多。希望这个指南可以帮到和我一样几乎 **零基础** 但又想 **建博客** 的朋友。😁

指南将分为上、下两部分。上篇有整个过程中用到的工具及操作流程；下篇则是真实遇到的问题以及一些个人理解。

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

#### 2. 创建 Github 仓库
![如图](/article_pic/zero-to-blog-1.png)
唔...好像是叫仓库...在 Repository name 输入框中输入`urUsername.github.io`，可以理解为项目名或者仓库名，也是默认的博客域名。urUsername 就是你的用户名，其他的不用填，点击 Create repository 按钮，创建成功后可以在 Your repositories 中随时在线查看。

找不到入口的话猛击下方按钮
<div markdown="0"><a href="https://github.com/new" class="btn btn-success" target="blank">+ Repository</a></div>

### 3. 在本地把 Github 用起来
网上 Github 的[基础使用教程](http://www.runoob.com/w3cnote/git-guide.html){:target="blank"}有很多，在此不做赘述。大致意思是，把上一步创建的仓库同步到本地，在本地进行修改，然后 commit 修改的地方，再同步到线上仓库。这些操作可以用命令行也可以用图形界面的客户端：命令行中从线上同步到本地貌似叫 clone 和 pull，从本地同步到线上叫 push；图形界面中这两种都是 sync。

### 4. 下载 jekyll 博客模板
![如图](/article_pic/zero-to-blog-2.png)
打开 [JekyllThemes](http://jekyllthemes.org/){:target="blank"}，从 demo 里挑一个喜欢的模板，下载并解压。然后把所有文件复制到上一步从线上同步到本地文件夹中（如果你操作无误，文件夹名称应该是博客域名：*<u>urUsername.github.io</u>*）。

### 5. 安装所需环境

- Ruby
<br>[下载 Ruby](https://www.ruby-lang.org/zh_cn/downloads/){:target="blank"}
- gem
<br>[下载 gem 包](https://ruby.taobao.org/){:target="blank"}
- jekyll
<br>命令行操作，提示没有权限的话，在指令前加上`sudo`。
<br>`gem install jekyll`
<br>`gem install kramdown`
<br>`gem install pygments.rb`
<br>`gem install liquid`
<br>`gem bundle`

### 6. 本地启动博客
用命令行 `cd` 指令进入到 *<u>urUsername.github.io</u>* 文件夹，然后用 `jekyll serve`，如果提示错误少什么东西，直接复制名字安装就可以，如果还是不行，那么使用 `bundle exec jekyll serve`启动，这是个暂时无法解决的问题，在指南下篇会提到。

用浏览器打开本地地址：*<u>http://127.0.0.1:4000/</u>*，如果一切顺利，将会看到与模板 demo 一样的页面。此时我们可以对博客进行编辑、自定义了。

### 7. 同步线上仓库
参考 Github [基础使用教程](http://www.runoob.com/w3cnote/git-guide.html){:target="blank"}，将本地文件夹同步至线上仓库。同步成功后约 1-3 分钟，你的博客 *<u>urUsername.github.io</u>* 便可以正常访问了！(首次同步可能时间略长，但一般不会超过10分钟)

其实现在博客已经建成了，那么如何换成自己想要的域名呢？看下一步！

### 8. 购买、绑定域名
- 去 [GoDaddy](https://www.godaddy.com/){:target="blank"} 注册账号，选购你中意的域名。购买时会提示附加产品，网络 dns 保护什么的，作为菜鸡觉得暂时用不到，并没有买。另外要说的是网上很多 GoDaddy 买域名教程都说可以支付宝，但是从 2015 年年中左右好像取消了这个支付渠道，所以只能用信用卡了。
- 登录 GoDaddy 账号，进入 Manage My Domains (域名管理)，找到想要绑定到博客的域名，进入 Manage DNS 选项。将 A (Host) 和 CName (Alias) 下的所有条目删除。然后分别添加如下图：
![如图](/article_pic/zero-to-blog-3.png)
- 在本地博客文件夹根目录下创建 CNAME 文件(无后缀，urUsername.github.io/CNAME)，文件里写你上你的域名，比如我的 CNAME 文件内写的是：robotu.co。
将修改同步至线上仓库(也可以直接网页打开 github 仓库，进行文件添加和编辑)。

完成这些，等待十几分钟至几个小时就大功告成了(DNS 相关修改可能会时间较长，但最长不会超过24小时)！
*p.s. 全程操作为 Mac OSX，理论上 Windows 也可以，但是 Mac 预装了一些环境，会简单很多，Windows嘛...你懂的。*
---

### 结语
第一次搞个人网(博)站(客)，从不会打开命令行，到创建成功，并用 Markdown 写了篇算是有点小内容的博客，可谓费了九牛二虎之力，同时也收获颇丰。

希望写的东西能对别人有些帮助，其实自己还没理解透彻，所以有的地方写的不是很清楚，之后会修正更新。下一篇将具体说说整个过程中我遇到的一些 **蠢** 问题。😁
