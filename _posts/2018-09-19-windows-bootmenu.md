---	
layout:	post	
title: 浅谈windows多系统及其启动菜单     
date: 18-09-19	
categories: blog
tags: [系统]   
description:  浅谈windows多系统及其启动菜单
---		
### 浅谈windows多系统及其启动菜单

    前几天看群里讨论VHD，就试着搞一搞多系统。uefi的10下装7系统，装好系统，修复引导后显示的是传统的启动菜单（黑底白字），咱还是喜欢metro的启动菜单，本来也就命令的事儿奈何折腾了一天才搞定，记录一下留作以后看。

**首先先给出具体命令**

> 传统启动菜单  
>
> - 单系统：`bcdedit/set{default}bootmenupolicy legacy`
> - 多系统：`bcdedit/set{current}bootmenupolicy legacy`                    
>
> Metro启动菜单
>
> - 单系统：`bcdedit/set{defaultybootmenupolicy standard`
> - 多系统：`bcdedit/set{current}bootmenupolicy standard`    
>

**我发生的问题**

​	本来按照上面的命令可以解决，但我就是不行，原因及我的折腾如下：

1. 我先装的X86的8.1系统直接修复的引导，导致引导炸了，10和8.1都无法进入系统，好吧我自己作大死，瞎几把安装X86的，之后进pe后修复10引导，安装64位7旗舰，修复引导，无论如何设置都是传统启动菜单。
2. 发现即使在传统菜单上我用了几次easybcd后多了好几个无效的启动项，r教授让我格式esp分区修复引导，做完后多余的启动菜单解决了，不过还是无法出来metro模式的。😭马上要绝望了。
3. 解决方法（建议格式化esp,重新修复）是进入vhd里的7系统后修复10的引导，，，（我早试过了，，不过是之前esp分区坏掉的情况下坏掉的，所以我也是白痴了）。这个原因是修复7引导的时候会覆盖，而7没有metro模式所以导致丢失了。

*PS：安装uefi的7的时候需要关闭安全打开CSM，但是某些BIOS里面无CSM，具体设置是BIOS mode设置为legacy support，再找Boot priority设置为uefi first.* 