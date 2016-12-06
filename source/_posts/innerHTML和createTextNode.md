---
title: innerHTML和createTextNode 
date: 2016-11-08 23:54:27
tags: DOM操作
---

平时在开发的时候常常需要操作节点，每次遇到需要注入内容的时候总是把这二者弄混淆，然后又要去查查api，所以是时候做个了结。

### 一、`createTextNode` 例如:


```javascript
var element = document.createElement("div");
element.className = "message";
var textNode = document.createTextNode("<Strong>Hello</Strong>");
element.appendChild(textNode);
document.body.appendChild(element);
```
结果: <Strong>Hello</Strong>

二、`innerHTML` 例子:
```javascript
<div > <h2 id="h2"></h2></div>
document.getElementById("h2").innerHTML = "<strong>hello</strong>";
```
结果: Hello 识别成加粗的黑体

三、区别

`innerHTML`和`createTextNode`都可以把一段内容添加到一个节点中，区别是如果这段内容中有html标签（如例子中的<strong></strong>）时表现就不同了，在createTextNode中会当作文本处理，不会被浏览器解析，但用innerHTML就会被当作HTML代码处理（如你的例子中Hello会被加粗显示）。
总的来说，**如果你确定要插入的内容中没有html标签，可以用innerHTML**，这样更简洁，**但如果不能确定（比如要插入用户输入的内容）建议用createTextNode的方式**。