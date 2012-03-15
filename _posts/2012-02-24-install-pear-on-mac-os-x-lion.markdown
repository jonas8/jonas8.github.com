---
layout: post
title: "Mac os x lion 上安装PEAR"
date: 2012-02-24 01:20
comments: true
categories: PHP
tags: [php, pear]
tagline: 
---
Mac Os X Lion 上安装PEAR,执行以下命令
{% highlight bash linenos %}
sudo php /usr/lib/php/install-pear-nozlib.phar
sudo pear config-set php_ini /private/etc/php.ini
sudo pecl config-set php_ini /private/etc/php.ini
sudo pear upgrade-all 
{% endhighlight %}


