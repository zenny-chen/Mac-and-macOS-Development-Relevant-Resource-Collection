# Mac and macOS Development Relevant Resource Collection
Mac与macOS开发相关技术文集

<br />

## 技术网站

1. [Mac如何恢复出厂设置](http://zhinan.sogou.com/guide/detail/?id=1610048493)
1. [macOS上安装MySQL](https://discussions.apple.com/docs/DOC-3082)
1. [Mac中如何设置三指拖拽 macOS Lion 如何单指双击拖拽](http://www.anystandards.com/archives/49079.html)
1. [揭秘苹果耗时半年修复的OS X漏洞](http://geek.csdn.net/news/detail/30401)
1. [黑Mach-O，符号动态绑定](https://github.com/facebook/fishhook)
1. [Objective-C Runtime](https://developer.apple.com/documentation/objectivec?language=objc)
1. [Alternative of CADisplayLink for macOS](https://stackoverflow.com/questions/14158743/alternative-of-cadisplaylink-for-mac-os-x)
1. [macOS开发 -- 通过访问Camera，实时获取图片](https://blog.csdn.net/heroguo_jp/article/details/79500654)
1. [NSImage 存储为jpg或png文件的方法](https://blog.csdn.net/yuanya/article/details/25510515)
1.  [macOS 开发：NSScrollView 学习笔记](https://segmentfault.com/a/1190000012069895)
1. [详解C语言中的stdin，stdout，stderr](http://blog.csdn.net/Crazy_Tengt/article/details/72717144)
1. [C语言压缩文件和用MD5算法校验文件完整性的实例教程_C 语言](https://yq.aliyun.com/ziliao/119635)
1. [链接过程中的符号重定位_C底层](http://blog.csdn.net/darkfaker/article/details/79370796)
1. [Linux内核中的软中断、tasklet和工作队列](http://blog.csdn.net/T146lLa128XX0x/article/details/79070798)
1. [How To Install LLVM and Clang on CentOS 6](https://www.vultr.com/docs/how-to-install-llvm-and-clang-on-centos-6)
1. [在Centos-5下安装Objective-C的编译环境](http://blog.csdn.net/Robincui2011/article/details/6785987)
1. [macOS中如何获取当前运行程序的路径](https://www.cnblogs.com/zenny-chen/p/3290653.html)
1. [在macOS上安装Homebrew](https://brew.sh)（用brew更新软件包：`brew upgrade <package>`）
1. Xcode 10之后可以在Apple开发者官网下载独立的OpenGL性能剖析等工具：https://developer.apple.com/download/more/?=for%20Xcode
1. [kqueue用法简介](https://www.cnblogs.com/luminocean/p/5631336.html)
1. [使用 kqueue 在 FreeBSD 上开发高性能应用服务器](https://www.ibm.com/developerworks/cn/aix/library/1105_huangrg_kqueue/)
1. [C/C++下scanf的%匹配以及过滤字符串问题](https://www.toutiao.com/a6659550631625228808)
1. [MLClassifier increase maxIterations in CreateML](https://forums.developer.apple.com/thread/104668)

<br/>

## Apple自己开源的代码
1. [https://opensource.apple.com](https://opensource.apple.com)
1. [https://github.com/apple/darwin-xnu](https://github.com/apple/darwin-xnu)
1. [Blocks runtime](https://opensource.apple.com/source/clang/clang-800.0.42.1/src/projects/compiler-rt/lib/BlocksRuntime/)
1. [Foreign Function Interfaces](https://opensource.apple.com/source/libffi/libffi-18.1/)
1. [libdispatch](https://opensource.apple.com/source/libdispatch/libdispatch-913.30.4/)
1. [Objective-C 4.0](https://opensource.apple.com/source/objc4/objc4-723/)
1. [libpthread](https://opensource.apple.com/source/libpthread/libpthread-301.30.1/)
1. [Core Foundation](https://opensource.apple.com/source/CF/CF-1153.18/)

<br/>

## 如何在最近几个版本的macOS中访问网路与读写文件

点击Xcode工程文件，然后点击**Capabilities**菜单栏，勾选上**App Sandbox**下面的Network的两个选项，如下图所示。
![屏幕快照 2018-12-06 上午3.40.15.png](https://upload-images.jianshu.io/upload_images/8136508-59a31493d04a9c15.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

如果要让自己的App能读写用户文件系统，那么需要在**App Sandbox**下面的**File Access**下面的文件类型中都使用***read/write***访问权限，如下图所示。
![屏幕快照 2018-12-07 上午2.00.09.png](https://upload-images.jianshu.io/upload_images/8136508-b0d942d864222b34.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

<br/>

## Mac下的一些小技巧

1. macOS下显示用户主目录下的Library目录：`chflags nohidden ~/Library/`
1. macOS下的App所产生的文件一般会存放在 `~/Library/Containers/` 目录下，然后会以“com.company.appname”作为目录。App被删除后，该文件夹不会被删除，因此需要我们手工去删除。
1. 取消QQ通知声音。首先进入“系统偏好设置”，然后进入“通知”，在左边栏找到QQ，然后选中后将“播放通知的声音”给取消勾选即可。
1. [如何解决macOS文本编辑等应用为何会自动转换引号](https://www.zhihu.com/question/35110457)
1. [教您如何远程访问您的Macbook](https://www.toutiao.com/a6636314785552007688)
1. 在macOS上安装ICCUC库：`brew install icu4c`。
1. 在macOS上安装swig库：`brew install swig`。
1. 在macOS上安装pkg-config：`brew install pkg-config`。
1. 在macOS上安装node.js（npm）：`brew install node`。
1. macOS上安装glib：`brew install glib`。glib默认安装在`/usr/local/Cellar/glib/<版本号>`。需要包含的头文件路径有：`/usr/local/Cellar/glib/2.58.1/include/glib-2.0`，`/usr/local/Cellar/glib/2.58.1/lib/glib-2.0/include`。需要包含的库文件路径：`/usr/local/Cellar/glib/2.58.1/lib`。如果仅仅只要glib的相关函数，则只要用`-lglib-2.0`进行连接即可。
1. 在macOS上要导出某些编译时所需要的符号：`export XXX_LIBS=xxxx`
1. 在macOS上导出动态库路径：`export DYLD_LIBRARY_PATH=xxxx`
1. meson被默认安装在`~/Library/Python/3.x/bin/`目录下。
1. macOS上安装Python3与Python3-Pip：首先安装HomeBrew，然后：
```bash
brew install python3
curl https://bootstrap.pypa.io/get-pip.py | python3

# 如果还想再安装Python 2.7.x的pip，则可以使用以下命令
sudo easy_install pip

# 如果在当前环境下同时有Python 3的pip，也有Python 2.7的pip，
# 那么使用 pip 默认表示Python 2.7下的；使用 pip3 则表示Python 3下的
```

<br/>

### macOS上安装MySQL

首先：`brew install mysql`
然后控制台会提示：
We've installed your MySQL database without a root password. To secure it run:
    mysql_secure_installation

MySQL is configured to only allow connections from localhost by default

To connect run:
    mysql -uroot

To have launchd start mysql now and restart at login:
  brew services start mysql
Or, if you don't want/need a background service you can just run:
  mysql.server start

<br/>

## macOS下日常使用的以及Xcode与iOS模拟器下的常用快捷键

1. 打印：shift+option+k
1. 在Finder中跳转到任一目录：cmd+shift+G
1. Safari与Xcode中直接放大/缩小字体：cmd与 **=** 一起按 / cmd与 **-** 一起按
1. 将选中的文字段落向右/向左缩进一个tab：cmd+] / cmd+[
1. 对选中的代码添加注释屏蔽/取消注释屏蔽：cmd+/  在含有注释的情况下则取消注释屏蔽
1. Xcode中关闭当前编辑的文件：control+command+w
1. 模拟器中模拟点击Home键：cmd+shift+H

