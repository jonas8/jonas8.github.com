---
layout: post
title: "Library Not Loaded: libmysqlclient.18.dylib"
date: 2012-03-15 14:03
comments: true
categories: ruby
tags: [ruby, rails]
excerpt: 
---
在rails中使用mysql2中出现Library not loaded: libmysqlclient.18.dylib错误，当然你得首先安装的有mysql,mysql默认的libmysqlclient.18.dylib在/usr/local/mysql/lib下，只需要

	export DYLD_LIBRARY_PATH=$DYLD_LIBRARY_PATH:/usr/local/mysql/lib/ #最好加到.bash_profile中去