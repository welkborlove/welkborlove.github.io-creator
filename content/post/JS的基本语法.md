---
title: "JS的基本语法"
date: 2020-05-04T14:01:36+08:00
draft: false
---


# 什么是表达式和语句
 * 1+2的表达式的值为3
 * add(1,2)的表达式值为函数返回值
 * console.log表达式的值为函数本身
 * console.log(3)表达式的值为多少呢？ undefined 
  
 ## 语句
 * var a = 1 是一个语句
 * 二者的区别
 * 表达式一般都有值,语句可能有也可能没有
 * 语句一般会改变环境(声明 赋值)
 * 上面两句话并不是绝对的
 * 大小写敏感 不要写错
 * var a和var A是不同的
 * object 和Object 是不同的
 * function和Function是不同的
 * 空格 
 * 大部分的空格没有实际意义
 * var a = 1 和var a=1 没有区别
 * 加回车大部分时候也不影响
 * 只有一个地方不能加回车 那就是return后面
  ### 标识符 
   * 规则
   * 第一个字符，可以是Unicode字母或$ 或者_或者中文 后面的字符 除了上面说还可以有数字
   * 变量名是标识符
   * var_ = 1
   * var $ = 2
   * var ______=6
   * var 你好 = 'hi'
   * 
   ###  区块block
   * 把代码包在一起
   * {let a = 1  let b = 2}
   * 常常与if / fou /while 合用

  ### if 语句  如果 。。那么
  * if 语句
  * if(表达式){语句1}else{语句2}
  * {}在语句只有一句的时候可以省略， 不建议这样做
  * 变态情况
  * 表达式里可以非常变态， 如a = 1
  * 语句 1 和 2 可以非常变态 如嵌套if else  
  * a = 1 if( a === 2) console.log('a')  console.log ('a等于2')
  * 常用写法
  ```if (表达式){语句} else if (表达式){语句}else{语句}```
   * 次用语句 ```function fn(){if(表达式){return 表达式}  if (表达式){return 表达式} return 表达式 }```
   ### switch 语句  if else 升级版
   * switch (fruit){case "banana"... break;  case "apple":...break; default: ...}
   * break 大部分时候 省略break 你就完了 少不部分时候，可以利用break    
  ### 问号冒号表达式   
  * 表达式1？表达式2：表达式3
  ### while 循环 当。。。时
   * while(表达式){语句}
   * 判断表达式的真假 
   * 当表达式为真， 执行语句 执行完在判断表达式的真假 
   * 当表达式为假 执行后面的语句
   * 其他 do 。。while  
  ### 语法糖
  * for是while循环的方便写法
  * for(语句；表达式2；语句3){循环体}
  * 先执行语句1
  * 然后执行表达式2
  * 如果为真 ，执行循环体 然后执行语句3
  * 如果为假 直接退出循环 执行后面的语句
 ### break 和continue
 * 退出所有的循环 退出当前的一次循环
 ### label 语句
  ``` foo: {console.log(1) break foo; console.log('本行不会输出')}```
  * { foo: 1} 是什么呢 是一个标签 值为1