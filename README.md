# Mac and macOS Development Relevant Resource Collection
Mac与macOS开发相关技术文集

<br />

## 技术网站

1. [Mac如何恢复出厂设置](http://zhinan.sogou.com/guide/detail/?id=1610048493)
1. [macOS上安装MySQL](https://discussions.apple.com/docs/DOC-3082)
1. [Mac中如何设置三指拖拽 macOS Lion 如何单指双击拖拽](http://www.anystandards.com/archives/49079.html)
1. [揭秘苹果耗时半年修复的OS X漏洞](http://geek.csdn.net/news/detail/30401)
1. [黑Mach-O，符号动态绑定](https://github.com/facebook/fishhook)
1. [Alternative of CADisplayLink for macOS](https://stackoverflow.com/questions/14158743/alternative-of-cadisplaylink-for-mac-os-x)
1. [macOS开发 -- 通过访问Camera，实时获取图片](https://blog.csdn.net/heroguo_jp/article/details/79500654)
1. [NSImage 存储为jpg或png文件的方法](https://blog.csdn.net/yuanya/article/details/25510515)
1.  [macOS 开发：NSScrollView 学习笔记](https://segmentfault.com/a/1190000012069895)
1. [macOS中如何获取当前运行程序的路径](https://www.cnblogs.com/zenny-chen/p/3290653.html)
1. [在macOS上安装Homebrew](https://brew.sh)（用brew更新软件包：`brew upgrade <package>`）
1. 在macOS上安装命令行编译工具的简单命令：`xcode-select --install`
1. [MLClassifier increase maxIterations in CreateML](https://forums.developer.apple.com/thread/104668)
1. [Xcode内存泄漏问题调试解决](https://my.oschina.net/u/2483082/blog/755130)
1. [Mac中的Automator小机器人可以为你做些什么](https://www.toutiao.com/i6484230280306491918/)
1. [uninstalling Unity3D on Mac](https://forum.unity.com/threads/uninstalling-unity-on-mac.395154/)

<br />

## Apple自己开源的代码
1. [https://opensource.apple.com](https://opensource.apple.com)
1. [https://github.com/apple/darwin-xnu](https://github.com/apple/darwin-xnu)
1. [Blocks runtime](https://opensource.apple.com/source/clang/clang-800.0.42.1/src/projects/compiler-rt/lib/BlocksRuntime/)
1. [Foreign Function Interfaces](https://opensource.apple.com/source/libffi/libffi-18.1/)
1. [libdispatch](https://opensource.apple.com/source/libdispatch/libdispatch-913.30.4/)
1. [Objective-C 4.0](https://opensource.apple.com/source/objc4/objc4-723/)
1. [libpthread](https://opensource.apple.com/source/libpthread/libpthread-301.30.1/)
1. [Core Foundation](https://opensource.apple.com/source/CF/CF-1153.18/)

<br />

## 如何在最近几个版本的macOS中访问网路与读写文件

点击Xcode工程文件，然后点击**Capabilities**菜单栏，勾选上**App Sandbox**下面的Network的两个选项，如下图所示。

![1.png](https://github.com/zenny-chen/Mac-and-macOS-Development-Relevant-Resource-Collection/blob/master/1.png)

<br />

如果要让自己的App能读写用户文件系统，那么需要在**App Sandbox**下面的**File Access**下面的文件类型中都使用***read/write***访问权限，如下图所示。

![2.png](https://github.com/zenny-chen/Mac-and-macOS-Development-Relevant-Resource-Collection/blob/master/2.png)

<br />

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

<br />

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

<br />

## macOS下日常使用的以及Xcode与iOS模拟器下的常用快捷键

1. 打印：shift+option+k
1. 在Finder中跳转到任一目录：cmd+shift+G
1. Safari与Xcode中直接放大/缩小字体：cmd与 **=** 一起按 / cmd与 **-** 一起按
1. 将选中的文字段落向右/向左缩进一个tab：cmd+] / cmd+[
1. 对选中的代码添加注释屏蔽/取消注释屏蔽：cmd+/  在含有注释的情况下则取消注释屏蔽
1. Xcode中关闭当前编辑的文件：control+command+w
1. 模拟器中模拟点击Home键：cmd+shift+H

<br />

## macOS 10.15 Catalina下允许使用控制台应用

在macOS Catanlina下，由于系统对应用的安全性做了更严格的限制，因此对于非Mac App Store上下载的应用默认是无法打开的，除非有专门的签名，然后让用户授权允许打开。这么一来，对于很多编译用的第三方控制台应用就犯难了。不过Apple也是考虑到了这一点，因此我们可以从偏好设置中的安全性选项里把我们信任的应用开启允许不满足安全性策略。下面来教大家详细设置方式。

首先，我们打开“**系统偏好设置**”，然后点击“**安全性与隐私**”，如下图所示。

![3.png](https://github.com/zenny-chen/Mac-and-macOS-Development-Relevant-Resource-Collection/blob/master/3.png)

然后，我们滑动左侧栏，找到“**开发者工具**”，随后点击左下角的锁状🔒按钮以允许编辑该选项。最后，我们勾选上中间栏的“**终端**”即大功告成，如下图所示。

![4.png](https://github.com/zenny-chen/Mac-and-macOS-Development-Relevant-Resource-Collection/blob/master/4.png)

设置完之后，如果此时您开着控制台应用，则系统会默认将它重启，重启完之后，设置就生效了。

<br />

## macOS下删除Unity3D（其他App也可参考）

- /Applications/Unity
- ~/Library/Unity
- ~/Library/Application Support/Unity
- /Library/Application Support/Unity (License file is here...prolly best to leave it alone, or return your license first before deleting)
- /Library/Application Support/PACE Anti-Piracy
- ~/Library/Caches/com.unity3d.*
- ~/Library/Logs/Unity
- ~/Library/Preferences/Unity
- ~/Library/Preferences/com.unity3d.*
- ~/Library/Preferences/com.OverTheEdge.BugReporter.plist
- ~/Library/Preferences/dk.Otee.*


