---
sidebar: auto
---

# 基础篇
## 第一天

### 浏览器内核 

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

### 浏览器兼容性

* W3C发布的规范，是开发者不断尝试总结出来的
* 各类厂商的浏览器，不平行，或者不按标准来

---



**Alert ()** 

* 在浏览器里弹出一个框，（提供一个确定按钮，点击确定弹框消失

* 输出内容转换成字符串因为调用了 **toString** 这个方法 **结果都是字符串**

  ```js
  alert({name='liubei'}) //=>  "[object Object]"
  ```

  ```js  
  alert([12,12]) //=> "12,12"
  ```
