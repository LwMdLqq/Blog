---
layout: post
title:  "undefined和null的区别"
date:   2019-02-19 10:58:13 +0800
categories: jekyll update
---

null和undefined都表示值的空缺

#### null：

* null代表空对象指针, 使用typeof运算得到object, 所以null是一个特殊的对象值
* null表示程序级的，正常的或在意料之中的值的空缺

#### undefined：
* undefined属于特殊的变量，当声明了一个变量但是未初始化时，得到的就是undefined
* undefined是表示系统级的，出乎意料的或者类似错误的值的空缺

总结：
    undefined是访问一个未初始化的变量时返回的值，而null是访问一个尚未存在的对象时所返回的值，因此可以把undefined看成是空的变量，把null看成是空的对象   
