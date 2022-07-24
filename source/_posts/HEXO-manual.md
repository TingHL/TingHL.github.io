---
title: HEXO 自建博客备份GitHub
date: 2021-08-08 20:55:34
categories:
- hexo
description: hexo 搭建博客过程中备份到GitHub上，以备更换电脑时环境丢失
---

# HEXO博客备份

由于自己换了电脑，忘记博客备份，只能重新搭建。为防止以后发生同样的情况，特将相关笔记记录一下。

## **参考链接**

- https://mupceet.com/2019/09/backup-hexo-blog/

## **步骤**

### **初次备份**

按照以下步骤，详情可以看一下参考链接

```shell
$cd blog
$git init

$git submodule https://github.com/theme-next/hexo-theme-next.git themes/next

$git add .
$git commit -m "init blog backup"

# 为了便于记忆 将main分支重命名为hexo分支 对应github.io中的备份分支hexo
$git branch -m master hexo
$git remote add origin https://github.com/XXX/XXX.github.io.git
$git push -u origin hexo:hexo
```

### **初次备份后**

- **博客网页部署**按照`hexo g,  hexo s,   hexo d`等命令进行生成，浏览，部署

  ```shell
  hexo g
  hexo s
  hexo d
  ```

  

- **博客源代码备份** `hexo`分支按照日常使用的`git`命令，推送到`github`的`hexo`分支上

  ```shell
  git add xxx
  git commit -m "backup"
  git push origin hexo:hexo
  ```

  
