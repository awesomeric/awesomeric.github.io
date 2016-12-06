---
title: 阿里前端面试题总结（一）
date: 2016-08-15 10:44:23
tags: JS面试
---
# 数组问题
博主前不久参加了阿里的内推，面试里面包含了一套笔试题，个人觉得难度还是比较简单，面试官也没有仔细的查看我的答案估计只是一个简单的评估。不过博主觉得还是可以和各位前端新同学一起分享一下自己的思路，起到抛砖引玉的作用。


### 题目
这是一道大题，包含三道小题，都是很基础的东西，所以就按照自己的想法写下思路。

###### 1.不使用loop生成1－100的数组


博主这里用了一句话的方法来完成这道题

```
var arr = Array.apply(null,Array(100)).map((index,value)=>value);
arr.shift();
arr.push(100);

```


###### 2.乱序排序该数组

这个比较简单直接给方法

```javascript
arr.sort(randomSort);

function randomSort(){
return Math.random()>.5?-1:1;
}
```
###### 3.用优雅的方式对数组前十项求和

这个博主也不是很明白什么是最优雅的方式，简单的完成了

```

result = 0;
for(value of arr){
	result+=value;
		}

console.log(result);
```
