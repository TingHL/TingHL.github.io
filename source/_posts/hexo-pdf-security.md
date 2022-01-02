---
title: HEXO 博客显示PDF，并控制博客访问权限
date: 2021-12-31 22:08:46
tags: 
description: hexo 博客中插入PDF，设置密码控制访问权限
---
# HEXO博客中插入PDF 

## _config.yml文件修改
将hexo博客根目录下`_config.yml`配置文件中的`post_asset_folder`选项设置为`true`  

该选项的功能说明如下:  
`当设置post_asset_folder为true参数后，在建立文件时，Hexo会自动建立一个与文章同名的文件夹，可以把与该文章相关的所有资源都放到那个文件夹，更方便的使用资源。`

## 新建一篇文章并插入PDF
```
$ hexo new <article name>
```

在`source/_post`文件夹下，会生成`<article name>.md`和`<article name>`文件夹。将想要显示的PDF 放到`<article name>`文件夹下，并在`<article name>.md` 文章，插入如下代码：

```js
<object data="XXX.pdf"  type="application/pdf" width="100%" height="877px">
```

然后通过`hexo g `和`hexo s`查看显示效果。

# HEXO设置文章访问密码
因为有一些PDF涉及版权，或者自己有一些文章不便于面向互联网发布。可以通过设置访问密码的方式控制文章的访问权限。  

主要用到的是`hexo-blog-encrypt` ，开源项目地址链接为：https://github.com/D0n9X1n/hexo-blog-encrypt/blob/master/ReadMe.zh.md
