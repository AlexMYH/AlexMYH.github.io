---
layout: post
title:  "android studio中fill_parent,wrap_content,match_parent区别及相关笔记"
date:   2018-03-31
desc: "NOHING"
keywords: "AlexMYH"
categories: [Java]
tags: [android]
icon: icon-html
---


## **1:三个属性都用来适应视图的水平或垂直大小，一个以视图的内容或尺寸为基础的布局比精确地指定视图范围更加方便。**

### 1）fill_parent       
   设置一个构件的布局为fill_parent将强制性地使构件扩展，以填充布局单元内尽可能多的空间。    
这跟Windows控件的dockstyle属性大体一致。设置一个顶部布局或控件为fill_parent将强制性让它布满整个屏幕。

### 2） wrap_content

   设置一个视图的尺寸为wrap_content将强制性地使视图扩展以显示全部内容。以TextView和ImageView控件为例，    
设置为wrap_content将完整显示其内部的文本和图像。布局元素将根据内容更改大小。设置一个视图的尺寸为wrap_content大体等同于设置Windows控件的Autosize属性为True。

### 3）match_parent
   Android2.2中match_parent和fill_parent是一个意思 .两个参数意思一样，match_parent更贴切，     
于是从2.2开始两个词都可以用。那么如果考虑低版本的使用情况你就需要用fill_parent了


## **2:Activity的几种状态：**
*Active/Runing 一个新 Activity 启动入栈后，它在屏幕最前端，处于栈的最顶端，此时它处于可见并可和用户交互的激活状态。       

*Paused当Activity被另一个透明或者Dialog样式的Activity覆盖时的状态。此时它依然与窗口管理器保持连接，系统继续维      
护其内部状态，所以它仍然可见，但它已经失去了焦点故不可与用户交互。 

*Stoped 当 Activity 被另外一个 Activity 覆盖、失去焦点并不可见时处于 Stoped 状态。 

*Killed Activity 被系统杀死回收或者没有被启动时处于 Killed 状态。

*protected void onStart() 该方法在 onCreate() 方法之后被调用，或者在 Activity 从 Stop 状态转换为 Active 状态时被调用，
一般执行了onStart()后就执行onResume()。 

*protected void onResume() 在 Activity 从 Pause 状态转换到 Active 状态时被调用。


```
onCreate()	这是第一个回调，在活动第一次创建是调用
onStart()	这个回调在活动为用户可见时被调用
onResume()	这个回调在应用程序与用户开始可交互的时候调用
onPause()	被暂停的活动无法接受用户输入，不能执行任何代码。当当前活动将要被暂停，上一个活动将要被恢复是调用
onStop()	当活动不在可见时调用
onDestroy()	当活动被系统销毁之前调用
onRestart()	当活动被停止以后重新打开时调用
```

## **3:若MAIN动作和 LAUNCHER类别没有在活动中声明，应用程序的图标将不会出现在主屏幕的应用列表中。**
```
<intent-filter>
             <action android:name="android.intent.action.MAIN" />
             <category android:name="android.intent.category.LAUNCHER"/>
          </intent-filter>  
```

















