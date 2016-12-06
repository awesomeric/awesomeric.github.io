---
title: 关于我自己的
date: 2016-11-12 23:50:16
---
```
function Myself(name,age,contact){

	this.name = name;
	this.age = age;
	this.contact = contact;
}
Myself.prototype.method = function(){
	console.log('hello,this is my simple introduction');
}

var me = mew Myself('EricTang',22,'bravesuperking@gmail.com');
```