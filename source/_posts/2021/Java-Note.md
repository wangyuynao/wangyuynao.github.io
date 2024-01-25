---
title: Java笔记
top: false
cover: false
toc: true
mathjax: true
date: 2021-02-21 11:02:33
tags:
- Java
categories:
- Java学习笔记
---

# Java学习笔记一

<!--more-->

## Java主类结构

Java语言是面向对象的程序设计语言，Java程序的基本组成单元是类，类体中又包括属性与方法两部分。每个应用程序都必须包含一个main()方法，含有main()方法的类称为主类。

### 包声明

一个Java应用程序是由若干个类组成的，package为包的关键字。

### 声明成员变量和局部变量

通常将类的属性称为类的全局变量（成员变量），将方法中的属性称为局部变量。全局变量声明在类体中，局部变量声明在方法体中。

### 编写主方法

main()方法为类体中的主方法，该方法从“{”开始，至"}"结束。public、static和void分别是main()方法的权限修饰符、静态修饰符、和返回值修饰符，Java程序中的main()方法必须声明为public static void。main()方法是程序开始执行的位置。

### 导入API类库

在Java语言中可以通过import关键字导入相关的类。

## Java基本数据类型

在Java中有8种基本数据类型来存储数值、字符和布尔值，

![基本数据类型](./java-Note/基本数据类型.png)

* 布尔类型又称逻辑类型，通过关键字boolean来定义布尔类型变量，只有true和false两个值，分别代表布尔逻辑中的“真”和“假”。布尔值不能与整数类型进行转换。布尔类型通常被用在流程控制中作为判断条件。

## 变量与常量

* 常量：其值不能被改变的量称为常量
* 变量：其值能被改变的量称为变量

### 标识符和关键字

* 标识符：标识符可以简单地理解为一个名字，用来标识类名、变量名、方法名、数组名、文件名的有效字符序列。Java语言规定标识符由任意顺序的字母、下划线(_)、美元符号($)和数字组成，并且第一个字符不能是数字。**标识符不能是Java中的保留关键字、标识符区分大小写。**
* 关键字：关键字是Java语言中已经被赋予特定意义的一些单词，不可以把这些字作为标识符来使用。



|    int    |  public  |    this    |   finally    |  boolean   | abstract  |
| :-------: | :------: | :--------: | :----------: | :--------: | :-------: |
| continue  |  float   |    long    |    short     |   throw    |  throws   |
|  return   |  break   |    for     |    static    |    new     | interface |
|    if     |   goto   |  default   |     byte     |     do     |   case    |
| strictfp  | package  |   super    |     void     |    try     |  switch   |
|   else    |  catch   | implements |   private    |   final    |   class   |
|  extends  | volatile |   while    | synchronized | instanceof |   char    |
| protected |  import  | transient  |   dafault    |   double   |           |

