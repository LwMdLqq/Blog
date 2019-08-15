---
layout: post
title:  "filter和map的区别"
date:   2019-08-15
excerpt: ""
project: true
tag:
- jekyll 
- moon
- blog
- about
- theme
comments: true
---



## filter和map的区别

```
// filter把传入的函数以此作用于每个元素，然后根据返回值是true还是false决定保留还是丢弃该元素。简单来说就是把Array的某些元素过滤掉，然后返回剩下的元素

var arr = [1, 2, 4, 5, 6, 9, 10, 15];
var r = arr.filter(function (x) {
    return x % 2 !== 0;
});
r; // [1, 5, 9, 15]

```


```
// map方法创建一个新数组，其结果是该数组中的每个元素都调用一个提供的函数后返回的结果。简单来说map就是对原数组的加工，映射成——映射的新数组

例一：
var array1 = [1,4,9,16];
const map1 = array1.map(x => x *2);

打印结果：Array [2,8,18,32]

例二：
var array1 = [1, 4, 9, 16];
 
const map1 = array1.map(x => {
    if (x == 4) {
        return x * 2;
    }
});

console.log(map1);

打印结果：Array [undefined, 8, undefined, undefined]

// 这样写只是增加了一个条件，即x的值为4时才乘以2，之所以会出现undefined，是因为map()方法创建了一个新数组，但新数组并不是在遍历完array1后才被赋值的，而是每遍历一次就得到一个值。所以，下面这样修改后就正确了：

var array1 = [1, 4, 9, 16];
 
const map1 = array1.map(x => {
    if (x == 4) {
        return x * 2;
    }
    return x;
});
```