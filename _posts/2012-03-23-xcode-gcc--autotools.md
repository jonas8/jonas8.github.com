---
layout: post
title: "xcode gcc和autotools的问题"
category: xcode
tags: [xcode, gcc, autotools]
---
{% include JB/setup %}

xcode在最近的版本更新中有很多变化，4.2版本彻底抛弃了gcc工具链，xcode 4.3又把autotools干掉了。固然llvm,cmake很先进，但是很多开源软件还不能用llvm编译，比如ruby 1.9.2以及ruby中的很多数据库驱动，没了autotools也是件很头痛的事，比如php的一些扩展没法编译。要保留这些工具如果你有之前的版本的安装文件（可以从[imzdl](http://imzdl.com/)下载）可以从xcode 4.1 -> xcode 4.2 -> xcode 4.3的顺序安装，安装之前不要uninstall之前的版本，到4.3的时候会有个选项删除之前的版本，但只会删除之前的/Develop目录，不会删除之前的command line tools,这样gcc autotools就都保存下来了。在4.3中Preferences - Downloads - Components里下载command line toos更新llvm工具链。

另外也可以自己手动安装:

**gcc**

1. github上有个[osx-gcc-installer](https://github.com/kennethreitz/osx-gcc-installer)
2. 也可以选择[hpc mac osx](http://hpc.sourceforge.net/index.php) 上的资源，包含有binary package,目前版本是gcc-4.7,比apple官方的新很多。

**autotools**

如果安装的有homebrew可以直接
{% highlight bash %}
brew install autoconf automake
{% endhighlight %}

