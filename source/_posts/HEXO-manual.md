---
title: HEXO manual
date: 2021-08-08 20:55:34
tags:
- hexo
- manual
categories:
- hexo
---

# HEXO博客备份

由于自己换了电脑，忘记博客备份，只能重新搭建。为防止以后发生同样的情况，特将相关笔记记录一下。

**参考链接**

- https://mupceet.com/2019/09/backup-hexo-blog/

**步骤**

```shell
$cd blog
$git init

$git submodule https://github.com/theme-next/hexo-theme-next.git themes/next

$git add .
$git commit -m "init blog backup"

$git branch -m master hexo
$git remote add origin https://github.com/XXX/XXX.github.io.git
$git push -u origin hexo:hexo
```

