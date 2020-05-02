---
title: "开博大吉"
date: 2020-04-27T14:01:36+08:00
draft: false
---


# a标签的用法
  a 标签有四个属性
 * a标签里面写上href 输入要跳转网页的地址 点击地址来访问网页 href的取值 网站https://baidu.com http://baidu.com //baidu.com  路径/a/b/c 以及a/b/c index.html 以及./index.html  伪协议 javascript:代码;  mailto:邮箱  tel:手机号  id hred=#xxx
 * a标签里面写上target 的作用是指定那个窗口打开网页  target的取值内置名字_blank _top _parent _self   程序员的命名  window的name  iframe 的name   iframe标签内嵌窗口很少用 只有老系统在用
 *  a标签里面写上download 理论上可以下载 但是现在不行 问题不是所有的浏览器都支持 尤其是手机  
 *  a标签里面写上rel=noopener 

## img标签 图片
 *  作用 发出get 请求,展示一张图片
 *  属性 all/height/width/src
 *  事件  onload/onerror
 *  相应式 max-width:100%
 *  可替换的元素请看MDN
 
### 常用的表章节的标签有哪些
* h1~h6 是标题标签
* section 是章 节的意思
* article 一片文章的意思
* main 主要的意思
* aside 旁边的意思
#### table 标签 表格
* 相关的标签有table thead tbody tfoot tr td th
* 相关的样式 table-layout  border-collapse borber-spacing
  ##### form 标签 表格
  * 作用发出get或post请求
  * 属性 action/autocomp
  * 事件 onsubmit
  
   ###### input 标签
   * 作用 让用户输入内容
   * 属性 type: button/checkbox/email/file/hidden/numberpassword/radio/search/submit/tel/textmaxlength/pattern/value/placeholder
   * 事件 onchange /onfocus/onblur
   * 其他的输入标签 select+option textarea labei  注意事项一般不监听input的click 事件 form 里面的input要有name  form里面放一个type=submit才能触发submit事件