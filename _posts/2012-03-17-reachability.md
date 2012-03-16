---
layout: post
title: "Reachability 编译警告"
category: objective-c
tags: [cocoa, ios, objective-c]
---
{% include JB/setup %}

apple官方的Reachability sample code (Version 2.2, 2010-07-20) 在xcode 4.2+编译的时候会产生一个警告:

>Declaration of 'struct sockaddr_in' will not be visible outside of this function 

解决办法:在Reachability.h加入
{% highlight objc %}
struct sockaddr_in; // netinet/in.h 有定义过也可以直接 #import <netinet/in.h>
{% endhighlight %}
