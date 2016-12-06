---
title: js字符串处理问题（一）
date: 2016-06-22 14:51:44
tags:
---
# JS中的常见字符串处理
最近参加了一些大公司的前端面试，所以特来总结一些常见题目以及答题的个人思路

	

## 1.输入字符串检测字符数量

主要是靠遍历字符串并创建一个新的对象来装载每一个字符，对每一个字符进行键值对赋值。

	
```javascript

var str = "dadasjadajdadan.dasddgjkl";
var join = {};
for(var i = 0;i < str.length;i++)
{
	if(!join[str.charAt(i)]){
	join[str.charAt(i)] = 1;}
	else {
		join[str.charAt(i)]++
	}
	}
	var max = 0;
	var maxStr = "";
	for(var item in join){
		if(join[item] > max){
			max = join[item];
			maxStr = item;
	}
	}
	console.log("the max str is " + maxStr +" " + 	"the 	number is " + max);

```
	
然后遍历对象属性，获得value值最大的属性，同时打印属性名称。

---

## 2.字符串子串查询
暂时可以使用indexof(string,position)

```

var string = 'erictangerictang';
var result = string.indexOf('tang');
console.log(result);//4
```
	
