# 如何在你的 Nexus 5 或 7 上安装 Android L 开发者预览版

> 原文:[https://life hacker . com/how-to-install-the-Android-l-developer-preview-on-your-1596531372](https://lifehacker.com/how-to-install-the-android-l-developer-preview-on-your-1596531372)

谷歌刚刚发布了最新版本 Android 的第一个开发者预览版。对于那些渴望获得最新最棒产品的人来说，下面是如何立即在 Nexus 5 或 Nexus 7 (2013)上安装 Android L 的方法。

Watch

首先，你需要解锁 [你的设备](https://lifehacker.com/everything-you-need-to-know-about-rooting-your-android-5789397)[ADB，并安装](http://lifehacker.com/the-easiest-way-to-install-androids-adb-and-fastboot-to-1586992378) 快速启动。然后，按照以下说明操作:

1.  点击 下载您设备的出厂图像 [。](http://developer.android.com/preview/setup-sdk.html)
2.  解压缩文件，并将其放在一个容易找到的位置。
3.  通过 USB 电缆将设备连接到计算机，并确保启用调试模式。
4.  为 ADB 打开命令行。
5.  输入`adb reboot bootloader`访问您设备的引导程序。
6.  导航到包含工厂图像的文件夹。
7.  输入`flash-all`运行安装脚本。

该脚本需要一分钟的时间来运行，您的设备可能会在启动动画上停留一段时间(在我自己的测试中，设备启动大约需要五分钟)。一旦设备启动，登录，你就可以开始了！

**警告:**在谷歌的下载页面上有提到，但还是值得重复一下: ***闪烁这个会擦除你的设备和你所有的数据*** 。开始之前，请务必做好备份。

如果你不是少数拥有 Nexus 5 或 Nexus 7 的幸运儿之一，你可以在这里 查看我们对 Android L [中所有酷东西的综述。我们还将亲自强调谷歌昨天在 I/O 大会上没有宣布的更酷的东西。Android L 将于今年秋季晚些时候正式推出。](https://lifehacker.com/updating-all-the-new-stuff-in-androids-l-release-prev-1595928268)

[Android L 预览画面](http://developer.android.com/preview/setup-sdk.html)||[系统画面闪烁指令](https://developers.google.com/android/nexus/images#instructions) | Google