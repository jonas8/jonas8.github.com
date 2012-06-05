---
layout: post
title: "mac os x上创建Windows 8可启动U盘"
category: others
tags: [mac,windows 8]
---
{% include JB/setup %}
需要u盘支持系统启动。
{% highlight bash %}
hdiutil convert -format UDRW -o ./win8.img ./Windows8-ReleasePreview-64bit-ChineseSimplified.iso # 以win8 release preview iso为例
diskutil list #get the current list of devices,e.g. /dev/disk1
diskutil unmountDisk /dev/disk1
sudo dd if=./win8.img.dmg of=/dev/rdisk1 bs=1m 
diskutil eject /dev/disk1
{% endhighlight %}

