---
sidebar: auto
sidebarDepth: 4
---

# 第一天-基础篇

## 浏览器内核 

* 浏览器中 **识别代码** + **绘制页面** 的东西 叫做 **内核**

* 编写HTML.CSS.JAVASCRIPT代码 要遵循W3C规范（W3C规范制订者，有多种规范）
* 浏览器就是按照W3C规范，识别HTMl.CSS.JAVASCRIPT，并绘制出来

| 浏览器                                       | 内核     |
| -------------------------------------------- | -------- |
| Chrome 谷歌浏览器                            | webKit   |
| FireFox  火狐浏览器                          | Gecko    |
| Opera     欧朋浏览器                         | Presto   |
| IE       浏览器                              | Trident  |
| Safari   苹果浏览器+大部分国产以及手机浏览器 | WebKit   |
| Edge   浏览器                                | edgehtml |

## 浏览器兼容性

* W3C发布的规范，是开发者不断尝试总结出来的
* 各类厂商的浏览器，不平行，或者不按标准来



## 导入JS的三种方式

### 行内倒入-不要使用

* 在HTML标签的 **属性** 里通过**事件**调用js代码
* 不安全，可伪注入恶意代码

```js
<div onclick="alert('hello world')"><div>   //div标签  
```

### 内嵌倒入

* 通过 script 标签 直接将js代码写在HTML里面 

```js
<html>
<head></head>
<body>
<script> alert('hello world')</script>
</body>
</html>
```

### 外链倒入 

* 通常 倒入js标签 放到body最底部，等元素标签全都加载完再通过加载js并通过js操作元素，css放到顶部head里

```js
<script src="script.js"></script>   //写法  
```





## JS常用的输出格式

### **Alert ()** 

警告[读法 əˈlərt](https://translate.google.cn/#view=home&op=translate&sl=en&tl=zh-CN&text=confirm) 

* 类型：弹出框
* 确定按钮值：`"Ture"` 字符串

在浏览器里弹出一个框，（提供一个确定按钮，点击确定弹框消失）点击**确定**返回值为：**Ture**

输出内容转换成字符串因为调用了 **toString** 这个方法 **结果都是字符串**

```js
alert({name='liubei'}) //=>  "[object Object]"
```

```js  
alert([12,12]) //=> "12,12"
```

### Confirm()

确认[读法 kənˈfərm](https://translate.google.cn/#view=home&op=translate&sl=en&tl=zh-CN&text=confirm) 

* 类型：弹出框
* 确定按钮值：`"Ture"` 字符串
* 取消按钮值：`"Fals"` 字符串

在 Alert() 的基础上增加了 **取消** 按钮 点击**取消** 返回值为**false**

```js
confirm('hello world');
```

1. 阅读下列代码;将 confirm() 赋予给变量 hello 通过alert()接受 hello 并将 hello的值输出

2. 当用户分别点击 **确定** 和 **取消** 按钮后的 返回的值分别为 true 和 false 

3. 可根据接受的结果做不同的处理 ；  不普遍，但系统类项目用的多

```js
var hello = confirm('hello world');
alert(hello);
```



### Prompt()

提示[读法](<https://translate.google.cn/#view=home&op=translate&sl=en&tl=zh-CN&text=Prompt>) 

* 类型：弹出框
* 不输入内容确定按钮值：`空`字符串
* 输入内容确定按钮值：`"String"`字符串
* 取消按钮值：`"Null"`  字符串

在confirm()的基础上 增加输入框 

输入内容点击 **确定** 返回值为：输入的内容

```js
prompt('hello');
```



### 注意 

1. 三个常用输出方式 输出的值都为 **字符串** 
2. 真是项目几乎不用，通常提示框都是右自己封装的插件和组件实现，不用内置，因为网站样式需要精美







## 浏览器控制台

### 简介 

方便开发人员进行调试 默认浏览器为Chrome

### 调用

* Mac: Option + Command + J
* Windows: F12 或者 Control + Alt + J 



### 面板

#### Elements

* 记录了当前页面的所用HTML元素结构 和 样式 可随意调整

#### Console

调试 解决Bug 都在这里， 看各种网站养成习惯在Console里查看 职业习惯，ps可能里面有入职邀请函

   ```js
console.log(); //在控制台输出，不会转换数据类型，输出什么格式就转换什么格式
console.log({name:'张飞'}) //=> {name:'张飞'}
==
console.dir()  //比log更详细一点
console.table() //把json数据展示为一个表格
document.write('hello') // 向页面输出html内容 几乎不用
   ```



#### Source

* 所有用到的 HTML CSS JAVASCRIPT 源代码
* 参考大型网站的js 源码，用的的可 保存 下载借鉴使用

#### Network

* 每个资源加载时间 成功与否
* 性能优化用的



## JS变量与常量

### JavaScript

> ECMAScript(ES):规定了JS的一些基础核心知识 （变量，数据类型，语法规范，操作语句）
>
> 先学ES3/5 再学ES6/7

> DOM: document object model 文档对象模型，里面提供了一些属性和方法，可以让我操纵页面中的元素

### 变量与常量

> 变量：值是可以变的

> 常量：值是不可以变的

### 变量写法

var 声明变量  name变量名 =赋予 123值；堆 和 栈 （Es6 用let）

```js
var name = liubei;
```



