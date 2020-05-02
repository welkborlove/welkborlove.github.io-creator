---
title: "博客搭建"
date: 2020-04-25T14:01:36+08:00
draft: false
---


# 如何用 hugo 搭建个人博课

Hugo 是Go语言实现的一个博客生成器 世界上最快的博客生成器

## 安装Hugo 
*  [官网教程](https://gohugo.io/getting-started/installing)
*  Window安装方法
*  去[Hugo releases](https://github.com/gohugoio/hugo/releases) 网页下载http://hugo_xxx_windows-64bit.zip/
*  解压,把hugo.exe放到D:\Software\hugo\hugo.exe
*  把D:\Software\hugo\加到PATH
*  重启终端,运行hugo version查看版本
  ### 快速搭建出博客
*  进入[Hugo](https://gohugo.io/)官方, 点击Quick Start快速开始
*  从Step2 开始抄代码, 直到Step 7
*  得到一个public的目录,这就是我们的博客站点
*  hugo server-D 可以预览草稿
*  hugo server 可以预览草稿
*  预览网站
*  双击打开public/index.html 发现不能预览
*  因为public/index.html不能使用文件协议预览
*  请使用hugo server 预览
*  