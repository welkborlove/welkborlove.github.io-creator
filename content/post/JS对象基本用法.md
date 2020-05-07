---
title: "开博大吉"
date: 2020-05-07T14:01:36+08:00
draft: false
---

 # JS对象
 * 七钟数据类型  number string boo symbol null undefined object 
 * 五个falsy值 null undefined 0 NaN ''(空字符串) 
 ## 对象Object
 * 对象 
 * 定义
 * 无序的数据集合
 * 键值对的集合
 * 写法
 * ``` let obj = { 'name': 'frank', 'age':18 }```
 * ```let obj = new Object({'name': 'frank'})```
 * ```console.log({'name': 'frank', 'age':18})```
 * 细节
 * 键名是字符串 不是标识符 可以包含任意字符
 * 引号可省略 省略之后就只能写标识符 
 * 就算引号省略了 键名也是字符串(重要)
 * 属性名
 * 每个key都是对象的属性名(property)
 * 属性值
 * 每一个value都是对象的属性值
 * 奇怪的属性名 所有的属性名会自动变成字符串
 * 细节 Object.keys(obj)可以得到obj的所有key
 ## 变量作属性名
 * 如何用变量做属性名
 * 之前都是用常量做属性名
 * let p1 = 'name'
 * let obj + {p1: 'frank'}这样写，属性名为'p1'
 * let obj = {[p1]:'frank'}这样写，属性名为'name'
 * 对比
 * 不加[]的属性名会自动变成字符串
 * 加了[]则会当做变量求值
 * 值如果不是字符串 则会自动变成字符串
## 
* 隐藏属性
* JS中每一个对象都有一个隐藏的属性
* 这个隐藏属性储存着共有属性组成的对象的地址
* 也就是说 隐藏属性储存着原型的地址
* 代码示例
* let obj = {}
* obj.toString()//居然不报错
* 因为obj的隐藏属性对应的对象上toString()
 ### 增删改查
 * delete obj.xxx或delete obj['xxx']
 * 即可删除obj的xxx属性
 * 请区分 属性值为undefined 和不含属性名
 * 不含属性名
 * 'xxx' in obj ===false
 * 含属性名 但是值为undefined 
 * 'xxx' in obj &&obj.xxx === undefined
 * 注意obj.xxx === undefined 
 * 不能断定'xxx'是否为obj的属性
  ### 查看所有属性
  * 查看自身所有属性
  * Object.keys(obj)
  * 查看自身+共有属性
  * console.dir(obj)
  * 或者自己依次用Object.keys打印```obj.__proto__```
  * 判断一个属性是自身的还是共有的
  * obj.hasOwnproperty('toString')
  ### 原型
  * 每个对象都有原型
  * 原型里存着对象的共有属性
  * 比如obj的原型就是一个对象
  * obj.```__proto__```存着这个对象的地址
  * 这个对象里有toString/constructor/valueOf等属性
  * 对象的原型也是对象
  * 所有对象的原型也是对象
  * obj = {}的原型即为所有对象的原型
  * 这个原型包含所有对象的共有属性 是对象的根
  * 这个原型也有原型 是null
 ### 查看属性
 * 两种方法查看属性
 * 中括号语法 obj['key']
 * 点语法 obj .key
 * 坑新人语法 obj[key]//变量 key的值一般不为'key'
 * 请优先你 让你以为key不是字符串
 * 等你确定不会弄混两种语法 再改用点语法
 * obj.name 等于obj['name']
 * obj.name不等于obj[name]
 * 这里的name是字符串 而不是变量
 * let name = 'frank' 
 * obj[name]等于obj['frank']而不是obj['name']和obj.name
  ### 修改隐藏属性
  * 不推荐使用```__proto__```
  * let obj = {name:'frank'}
  * let obj2 = {name:'jack'}
  * let common = {kind: 'human'}
  * obj.```__prtot__``` = common
  * 推荐使用Object.create
  * let obj = Object.create(common)
  * obj.name = 'frank'
  * let obj2 = Object.create(common)
  * obj2.name = 'jack'
  * 规范大概的意思是 要改就一开始就改 别后来再改
 #### 总结
 * 删
 * delete obj['name']
 * 'name' in obj//false
 * obj.hasOwnProperty('name')//false
 * 查
 * Object.keys(obj)
 * console.dir(obj)
 * obj['name']//记住这里的name是字符串
 * obj[name]//记住这里的name是变量
  ### 改
  * 改自身obj['name'] = 'jack'
  * 批量改自身Object.assign(obj,{age:18,......})
  * 改共有属性obj.```__proto__```['toString'] ='xxx'
  * 改共有属性Object.prototype['toString'] = 'xxx'
  * 改原型obj.```__prtot__``` = common
  * 改原型let obj =Object.create(common)
  * 注:所有```__prtot__```的代码都是强烈不推荐写
  * 增
  * 基本同上 有属性就改 没属性就增加