---
layout: post
title: "UIColor使用十六进制的宏"
category: objective-c
tags: [ios, objective-c]
---
{% include JB/setup %}
一个宏,使用起来比较方便，来源[Cocoa-Matic](http://cocoamatic.blogspot.com/2010/07/uicolor-macro-with-hex-values.html)
{% highlight objc %}
#define UIColorFromRGB(rgbValue) [UIColor colorWithRed:((float)((rgbValue & 0xFF0000) >> 16))/255.0 green:((float)((rgbValue & 0xFF00) >> 8))/255.0 blue:((float)(rgbValue & 0xFF))/255.0 alpha:1.0]
//how to use
UIColor *color=UIColorFromRGB(0xDDEEFF);
{% endhighlight %}
