# 每个 OS X 命令行用户都应该知道的八个终端实用程序

> 原文：<https://lifehacker.com/eight-terminal-utilities-every-os-x-command-line-user-s-1593793109>

OS X 终端打开了一个强大的 UNIX 实用程序和脚本的世界。如果您正在从 Linux 迁移，您会发现许多熟悉的命令以您期望的方式工作。但是高级用户通常不知道 OS X 自带了一些在其他操作系统上找不到的基于文本的工具。



了解这些 Mac 专用程序可以让你在 [命令行](https://lifehacker.com/a-command-line-primer-for-beginners-5633909) 上更有效率，帮助你在 UNIX 和 Mac 之间架起一座桥梁。

***本帖最初出现在米切尔·科恩的博客上，***[***mitchchn . me***](http://www.mitchchn.me/)***。***

## 1.O **笔**

`open`打开文件、目录和应用程序。很刺激，对吧？但是作为一个**命令行双击，它确实很方便。**例如，键入:

```
$ open /Applications/Safari.app/ 
```

…将启动 Safari，就像您在 Finder 中连按它的图标一样。回想一下，OS X 应用不是真正的可执行文件，而是扩展名为*的特殊目录(包)。app* 。`open`是从命令行启动这些程序的唯一方法。它还可以启动其他真正捆绑在一起的文件，比如 Pages 文档。)

如果你将`open`指向一个文件，它将试图加载这个文件及其相关的 GUI 应用程序。`open screenshot.png`将在预览中打开该图像。您可以设置`-a`标志来自行选择应用程序，或者使用`-e`在“文本编辑”中打开文件进行编辑。

在一个目录上运行`open`将会直接把你带到 Finder 窗口中的那个目录。这对于通过键入`open .`调出当前目录特别有用

请记住，Finder 和终端之间的集成是双向的——如果您将文件从 Finder 拖到终端窗口中，它的完整路径会粘贴到命令行中。

## 2.P**b 复制**和 P**b 粘贴**

这两个命令允许您从命令行复制和粘贴文本。当然，您也可以只使用鼠标——但是`pbcopy`和`pbpaste`的真正威力来自于它们是 UNIX 命令这一事实，这意味着它们受益于管道、重定向以及与其他命令一起位于脚本中的能力。打字:

```
$ ls ~ | pbcopy 
```

…会将您主目录中的文件列表复制到 OS X 剪贴板。您可以轻松捕获文件的内容:

```
$ pbcopy < blogpost.txt 
```

..或者做些更疯狂的事。这个被破解的脚本将抓取最新的谷歌涂鸦的链接，并将其复制到你的剪贴板上。

```
$ curl http://www.google.com/doodles#oodles/archive | grep -A5 'latest-doodle on' | grep 'img src' | sed s/.*'<img src="\/\/'/''/ | sed s/'" alt=".*'/''/ | pbcopy
```

将`pbcopy`与管道一起使用是一种很好的方式来捕获命令的输出，而不必向上滚动并仔细选择它。这使得共享诊断信息变得容易。`pbcopy`和`pbpaste`也可以用来自动化或加速某些类型的任务。例如，如果您想要将电子邮件主题行保存到任务列表，您可以从 Mail.app 复制主题并运行:

```
$ pbpaste >> tasklist.txt 
```

## 3.**dfdf**

许多 Linux 超级用户尝试过使用`locate`在 Mac 上搜索文件，然后很快发现它不起作用。总是有古老的 UNIX `find`命令，但是 OS X 有它自己的杀手级搜索工具:Spotlight。那么为什么不从命令行利用它的强大功能呢？

这正是`mdfind`所做的。聚光灯能找到的东西，`mdfind`也能找到。这包括搜索内部文件和元数据的能力。

自带一些便利功能，让它从它的蓝色大兄弟中脱颖而出。例如，`-onlyin`标志可以将搜索限制到单个目录:

```
$ mdfind -onlyin ~/Documents essay 
```

`mdfind`数据库应该在后台保持最新，但是您也可以使用`mdutil`对它(以及 Spotlight)进行故障诊断。如果 Spotlight 不能正常工作，`mdutil -E`将删除索引并从头开始重建。您也可以使用`mdutil -i off`完全关闭索引。

## 4.屏幕截图

让您拍摄许多不同类型的截图。它类似于 **Grab.app** 和键盘快捷键 cmd + shift + 3 和 cmd + shift + 4，除了它更灵活。以下是使用`screencapture`的几种不同方式:

捕获屏幕内容，包括光标，并将生成的图像(名为“image.png”)附加到新邮件中:

```
$ screencapture -C -M image.png 
```

使用鼠标选择一个窗口，然后在没有窗口投影的情况下捕捉其内容，并将图像拷贝到剪贴板:

```
$ screencapture -c -W 
```

延迟 10 秒后捕捉屏幕，然后在预览中打开新图像:

```
$ screencapture -T 10 -P image.png 
```

用鼠标选择屏幕的一部分，捕捉其内容，并将图像保存为 pdf 格式:

```
$ screencapture -s -t pdf image.pdf 
```

要查看更多选项，请键入`screencapture --help`

## 5.l〔t0〕aunchtl〔t1〕

`launchctl`让你与 OS X 初始化脚本系统`launchd`交互。使用启动守护程序和启动代理，您可以控制在启动计算机时启动的服务。您甚至可以设置脚本在后台定期或定时运行，类似于 Linux 上的 cron 作业。

例如，如果您想让 Apache web 服务器在您打开 Mac 时自动启动，只需键入:

```
$ sudo launchctl load -w /System/Library/LaunchDaemons/org.apache.httpd.plist 
```

运行`launchctl list`将显示当前加载了哪些启动脚本。`sudo launchctl unload [path/to/script]`将停止并卸载正在运行的脚本，添加`-w`标志将从您的引导序列中永久删除这些脚本。我喜欢在所有自动更新“助手”= " " created = " " by = " " adobe = " " apps = " "和="" microsoft="" office。< ="" p="" >

启动脚本存储在以下位置:

> ~/库/启动代理
> 
> /库/启动代理
> 
> /Library/launch 守护进程
> 
> /系统/库/启动代理
> 
> /系统/库/启动守护进程

要了解启动代理或守护进程的内容，有一篇由 [保罗·安斯利](http://paul.annesley.cc/2012/09/mac-os-x-launchd-is-cool/) 撰写的博客文章，带你了解文件格式。如果你想学习如何编写自己的`launchd`脚本，苹果在他们的 [开发者网站](https://developer.apple.com/library/mac/documentation/MacOSX/Conceptual/BPSystemStartup/Chapters/CreatingLaunchdJobs.html) 上提供了一些有用的文档。如果你想完全避免使用 [命令行](https://lifehacker.com/become-a-command-line-ninja-with-these-time-saving-shor-5743814) ，还有奇妙的 [Lingon](http://www.peterborgapps.com/lingon/) 应用。

## 6.S **ay**

这是一个有趣的例子:`say`将文本转换为语音，使用 OS X 用于 [画外音](http://www.apple.com/accessibility/osx/voiceover/) 的相同 TTS 引擎。没有任何选项，`say`将简单地 [大声说出您给出的任何文本](https://www.youtube.com/watch?v=G0FtgZNOD44) :

```
$ say "Never trust a computer you can't lift." 
```

您还可以使用`say`来朗读带有`-f`标志的文本文件的内容，并且可以存储带有`-o`标志的结果音频剪辑:

```
$ say -f mynovel.txt -o myaudiobook.aiff 
```

在脚本中，`say`命令可以代替控制台日志记录或警告声音。例如，您可以设置一个自动机或 [Hazel](http://www.noodlesoft.com/hazel.php) 脚本来进行批处理文件，然后用`say`来宣布任务完成。

但是最令人愉快的使用`say`是相当险恶的:如果你有`ssh`访问朋友或同事的 Mac，你可以悄悄地登录他们的机器，并通过命令行困扰他们。给他们一个惊喜。

可以设置语音(和语言！)供`say`使用，方法是在“系统偏好设置”的**听写&语音**面板中更改默认设置。

## 7\. D **iskutil**

`diskutil`是 OS X 自带的**磁盘工具**应用的命令行界面。它可以做它的图形表亲能做的一切，但它也有一些额外的功能——比如用零或随机数据填充磁盘。只需输入`diskutil list`来查看连接到您机器的磁盘和可移动介质的路径名，然后将命令指向您想要操作的卷。小心:`diskutil`如果使用不当会永久破坏数据。

## 8.B **rew**

好吧——从技术上讲，这不是一个本地命令。但是没有 OS X 动力的用户应该是没有 [家酿](http://brew.sh) 的。该网站称之为“OS X 缺失的包装经理”，这再正确不过了。如果你曾经在 Linux 中使用过`apt-get`,你会觉得在自制软件中如鱼得水。(事实上，Homebrew 更类似于 FreeBSD 的 Ports 系统，而不是 Linux 的 apt。它使用混合的源代码/二进制系统:如果某个特定的包没有可用的二进制文件，它将简单地下载源代码 tarball 并编译它——这在当今的多核 MAC 上不成问题。)

让您轻松访问开源社区中成千上万的免费实用程序和库。例如，`brew install imagemagick`将为你设置 [ImageMagick](http://www.imagemagick.org) ，这是一个强大的实用程序，它可以让 [做任何事情](https://lifehacker.com/how-to-make-your-own-bulk-app-installer-for-os-x-1586252163) ，从制作动画 gif 到在几十种不同类型之间转换图像。`brew install node`将向您介绍 [NodeJS](http://nodejs.org) ，这是一款开发和运行服务器端 JavaScript 应用的热门新工具。

你也可以玩自制软件:`brew install archey`会给你带来 **Archey** ，这是一个很酷的小脚本，在彩色的苹果标志旁边显示你的 Mac 的规格。家酿中的选择是巨大的——因为创建 [公式](https://github.com/Homebrew/homebrew/wiki/Formula-Cookbook) 非常容易，所以新的软件包一直在增加。

archey——我的命令行将所有男孩带到院子里。

但是家酿啤酒最棒的部分是什么？它将所有文件保存在一个目录中:`/usr/local/`。这意味着你可以安装新版本的系统软件，如`python`和`mysql`，而不会干扰内置的同等软件。如果你想卸载你的自制软件，可以使用 [卸载脚本](https://gist.github.com/mxcl/1173223) 轻松卸载。

为了更好地体验 [**终端. app**](https://lifehacker.com/the-best-terminal-emulator-for-mac-os-x-5857046) ，这里列出了 OS X 10.9 小牛 中所有可用的 [控制台命令。](http://ss64.com/osx/)

感谢读者的反馈，我在后续的帖子中又写了一些命令: [(还有八百多个)](http://www.mitchchn.me/2014/and-eight-hundred-more/) 。

[八个终端实用程序每个 OS X 命令行用户都应该知道](http://www.mitchchn.me/2014/os-x-terminal/) | Mitchchn.me

* * *

米切尔·科恩(Mitchell Cohen)是一位来自多伦多的作家和技术爱好者。他在自己的博客[<small>*mitchchn . me*</small>](http://mitchchn.me/)<small>*中写道咖啡、代码、新闻、语言、失眠和巨型蜘蛛。可以在*</small>[<small>*@ mitch CHN*</small>](http://twitter.com/mitchchn)<small>*关注他的推特。*</small>

<small>*想看看你在 Lifehacker 上的作品？邮箱*</small> [<small>*安迪*</small>](mailto:andy@lifehacker.com) <small>*。*T15】</small>