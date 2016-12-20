---
layout: post
title: "Install jekyll on centOS6.5"
categories: jekyll
tags: jekyll RubyGems
date: 2016-12-20 14:30:02 +0800
excerpt: 建立github+markdown+jekyll的过程以及踩的一些坑。
---
* content
{:toc}





最近我决定弄一个博客记录一些东西，并决定使用github+markdown+jekyll 。这一套东西的好处在于:
1. 我只需要写markdown文件就可以更新blog。
2. 我非常喜欢git和github，所以把blog放在github我会比较开心。
3. jekyll是少数几个我找到的将markdown转换成静态网页的开源软件，并可以用在linux（centos6.5）上运行。
4. 而且jekyll功能很齐备，配合一些插件即可完成包括评论分类在内的blog的功能。

想要在本地搭建这套blog系统，首先需要在本地安装jekyll。要安装jekyll，首先需要安装Ruby环境与node.js环境。
通过[node.js](https://nodejs.org/en/)可以下载安装node.js。我装的是7.2.1版本。
然后是[ruby](https://ruby-china.org/wiki/ruby-mirror)。我下载的是2.3.1版本。

之后，可以通过[gem](http://guides.rubygems.org/what-is-a-gem/)指令下载jekyll。但在这之前，受到某个不可描述的影响，国内要上[gem的默认源](http://rubygems.org/)比较困难。所以在用gem下载jekyll之前，我们需要替换gem的源。

```
gem sources -a http://gems.ruby-china.org
gem sources --remove http://rubygems.org/
gem sources -l
```
确认只有我们新添加的source之后，就可以下载安装jekyll了。

```
$ gem install jekyll bundler
$ jekyll -v
jekyll 3.3.1
```
至此，本地jekyll环境就搭建好了。

在这之后，你可以通过jekyll新建网站，添加主题等。我选择的是github上一个人提供的[主题](https://github.com/Gaohaoyang/gaohaoyang.github.io)。之后只要在_post写入文章就可以了。

