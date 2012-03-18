---
layout: post
title: "Defines Presentation context is not available prior ... 警告"
category: objective-c
tags: [ios, xcode]
---
{% include JB/setup %}
在xcode 4.2中使用TabBar Controller/Navigation Controller时， 编译时候会有如下警告：
>Defines Presentation context is not available prior to xcode 4.2
解决办法： 
>Just uncheck the "Defines Context" checkbox in the attributes inspector. (Double-click on MainWindow.xib, select the navigation controller/Tab Bar Controller, then go to View->Utilities->Attributes Inspector.) That'll get rid of the warnings.