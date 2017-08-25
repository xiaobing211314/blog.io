---	  
layout: post  
title: 	浏览器内核简介   
date:  2017-08-25   
categories: blog  	 
tags: [浏览器]    	
description: 浏览器内核的极度简单介绍.  	
---    
   
   
### 浏览器内核
浏览器最重要或者说核心的部分是“Rendering Engine”，可大概译为“渲染引擎”，不过我们一般习惯将之称为“浏览器内核”。负责对网页语法的解释并渲染（显示）网页。 所以，通常所谓的浏览器内核也就是浏览器所采用的渲染引擎，渲染引擎决定了浏览器如何显示网页的内容以及页面的格式信息。不同的浏览器内核对网页编写语法的解释也有不同，因此同一网页在不同的内核的浏览器里的渲染（显示）效果也可能不同。    

### 内核分类

#### Trident   

Trident(IE内核)：该内核程序在1997年的IE4中首次被采用，是微软在Mosaic代码的基础之上修改而来的，并沿用到IE11，也被普遍称作”IE内核”。

#### Gecko

Gecko(Firefox内核)：Netscape6开始采用的内核，后来的Mozilla FireFox(火狐浏览器) 也采用了该内核，Gecko的特点是代码完全公开，因此，其可开发程度很高，全世界的程序员都可以为其编写代码，增加功能。  

#### Presto

Presto(Opera前内核) (已废弃)： Opera12.17及更早版本曾经采用的内核，现已停止开发并废弃，该内核在2003年的Opera7中首次被使用，该款引擎的特点就是**渲染速度的优化达到了极致**，然而代价是牺牲了网页的兼容性。

#### Webkit

Webkit(Safari内核,Chrome内核原型,开源):它是苹果公司自己的内核，也是苹果的Safari浏览器使用的内核。

#### Blink   

Blink是一个由Google和Opera Software开发的浏览器排版引擎，Google计划将这个渲染引擎作为Chromium计划的一部分，并且在2013年4月的时候公布了这一消息。这一渲染引擎是开源引擎WebKit中WebCore组件的一个分支，并且在Chrome（28及往后版本）、Opera（15及往后版本）和Yandex浏览器中使用。   
      
详情参见[浏览器内核](https://wapbaike.baidu.com/item/%E6%B5%8F%E8%A7%88%E5%99%A8%E5%86%85%E6%A0%B8/10602413?fr=aladdin)  [内核小知识](http://www.iplaysoft.com/browsers-engine.html)



