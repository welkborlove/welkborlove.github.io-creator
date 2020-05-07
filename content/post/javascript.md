---
title: "js"
date: 2020-05-01T14:01:36+08:00
draft: false
---

 # javascript的总结
  * js是布兰登在1995年5月仅花了10天的时间把原型设计出来 最初命名为Mocha,网景公司为了让这门语言搭上java的热度改为javascript命名 这也是成为大众这门语言的诸多误解.
  * javasceipt的基本特点如下
  * 是一种解析型脚本语言(代码不进行预諞译)
  * 主要用来HTML页面添加交互行为
  * 可以直接嵌入HTML页面,但写错单独js文件有利于解构和行为的分离
  * javascript常用来完成以下任务
  * 嵌入动态文本于HTML页面
  * 对浏览器事件作出响应
  * 读写HTML元素
  * 在数据被提交到服务器之前验证数据
  * 检测访客的浏览器信息
  * 控制cookies，包括创建和修改等
  * 特性
  * 不同于服务器端脚本语言，例如PHP与ASP，JavaScript主要被作为客户端脚本语言在用户的浏览器上运行，不需要服务器的支持。所以在早期程序员比较青睐于JavaScript以减少对服务器的负担，而与此同时也带来另一个问题：安全性。而随着服务器变得强大，现在的程序员更喜欢运行于服务端的脚本以保证安全，但JavaScript仍然以其跨平台、容易上手等优势大行其道。同时，有些特殊功能（如AJAX）必须依赖JavaScript在客户端进行支持。随着引擎如V8和框架如Node.js的发展，及其事件驱动及异步IO等特性，JavaScript逐渐被用来编写服务器端程序。且在近几年中，Node.js的出世，让JavaScript也具有了一定的服务器功能，且在某些方面比PHP的效果更为显著。

 ## Javascript的10个设计缺陷

  1.  不适合开发大型程序
  * Javascript没有名称空间（namespace），很难模块化；没有如何将代码分布在多个文件的规范；允许同名函数的重复定义，后面的定义可以覆盖前面的定义，很不利于模块化加载
  2.  非常小的标准库
  * Javascript提供的标准函数库非常小，只能完成一些基本操作，很多功能都不具备。
  3.  null和undefined
  * null属于对象（object）的一种，意思是该对象为空；undefined则是一种数据类型，表示未定义

```typeof null; // object```
```typeof undefined; // undefined```

两者非常容易混淆，但是含义完全不同。

```var foo;```
```alert(foo == null); // true```
```alert(foo == undefined); // true```
```alert(foo === null); // false```
```alert(foo === undefined); // true```

在编程实践中，null几乎没用，根本不应该设计它。

4. 全局变量难以控制
* Javascript的全局变量，在所有模块中都是可见的；任何一个函数内部都可以生成全局变量，这大大加剧了程序的复杂性
5. 自动插入行尾分号
* Javascript的所有语句，都必须以分号结尾。但是，如果你忘记加分号，解释器并不报错，而是为你自动加上分号。有时候，这会导致一些难以发现的错误。
6. 加号运算符
 * +号作为运算符，有两个含义，可以表示数字与数字的和，也可以表示字符与字符的连接。

  ```alert(1+10); // 11```

  ```alert("1"+"10"); // 110```

  如果一个操作项是字符，另一个操作项是数字，则数字自动转化为字符。

  ```alert(1+"10"); // 110```

  ```alert("10"+1); // 101```

  这样的设计，不必要地加剧了运算的复杂性，完全可以另行设置一个字符连接的运算符。

7. NaN  NaN是一种数字，表示超出了解释器的极限。它有一些很奇怪的特性：

```NaN === NaN; //false```

```NaN !== NaN; //true```

```alert( 1 + NaN ); // NaN1```

与其设计NaN，不如解释器直接报错，反而有利于简化程序。

8. 数组和对象的区分
* 由于Javascript的数组也属于对象（object），所以要区分一个对象到底是不是数组，相当麻烦。Douglas Crockford的代码是这样的：
9. == 和 ===
* ==用来判断两个值是否相等。当两个值类型不同时，会发生自动转换，得到的结果非常不符合直觉。
* 因此，推荐任何时候都使用"==="（精确判断）比较符。
10. 基本类型的包装对象
* Javascript有三种基本数据类型：字符串、数字和布尔值。它们都有相应的建构函数，可以生成字符串对象、数字对象和布尔值对象。
* 与基本数据类型对应的对象类型，作用很小，造成的混淆却很大。
11.  既然Javascript有缺陷，数量还不少，那么它是不是一种很糟糕的语言？有没有前途？
回答是Javascript并不算糟糕，相反它的编程能力很强大，前途很光明。