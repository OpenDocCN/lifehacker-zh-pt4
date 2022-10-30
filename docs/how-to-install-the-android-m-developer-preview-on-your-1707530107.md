# 如何在您的 Nexus 5、6 或 9 上安装 Android M 开发者预览版

> 原文:[https://life hacker . com/how-to-install-the-Android-m-developer-preview-on-your-1707530107](https://lifehacker.com/how-to-install-the-android-m-developer-preview-on-your-1707530107)

今天的 [Android M 公告](https://lifehacker.com/all-the-new-features-of-android-m-1707454646) 在 [Google I/O 2015](http://lifehacker.com/all-the-important-stuff-google-announced-at-i-o-2015-1707454800?rev=1432842495224) 已经让我们相当兴奋了。如果你渴望尝试新的热点(并且你有 Nexus 5、6、9 或播放器)，下面是如何立即在你的设备上安装它的方法。

Watch

若要开始，您需要解锁您的设备。你不需要 root，但你可以在 [阅读更多关于如何解锁你的设备的内容，我们的 root 指南在这里](https://lifehacker.com/everything-you-need-to-know-about-rooting-your-android-5789397) 。你还需要在你的电脑上安装 [ADB 和 fastboot](http://lifehacker.com/the-easiest-way-to-install-androids-adb-and-fastboot-to-1586992378) ，并且至少具备 [和](http://lifehacker.com/the-most-useful-things-you-can-do-with-adb-and-fastboot-1590337225) 的模糊工作知识。然后，按照以下步骤操作:

1.  点击 下载您设备的出厂图像 [。](http://developer.android.com/preview/download.html)
2.  解压文件并保存在容易找到的地方。
3.  通过 USB 电缆将设备连接到计算机，并确保调试模式已启用。
4.  打开 ADB 命令行。
5.  输入`adb reboot bootloader`访问您设备的引导程序。(OS X 用户应补充。/在这个命令之前。)
6.  导航到包含您的工厂图像的文件夹。
7.  输入`flash-all`运行安装脚本。(OS X 用户，与步骤 5 相同的警告。)

脚本需要几分钟时间。设备在启动前通常会在启动动画上停留几分钟，所以如果你的需要一段时间*不要惊慌*。一旦设备启动，登录并享受乐趣！

**警告:这将擦除您的设备。**谷歌在其几个下载页面上提到了这一点，但以防你错过了它，闪烁这个会彻底清除你的设备和 ***清除你所有的数据*。**在继续之前，请务必进行备份，不要在您工作绝对需要的设备上尝试备份。

如果你没有足够幸运地拥有 Android M 的设备，你仍然可以在这里查看我们之前的报道。我们还将亲自去寻找谷歌没有宣布的功能。如果你发现了任何酷的东西，请在下面的评论中提出来！Android M 是一个开发者预览版，但完整版(将有一个合适的名称)应该在今年晚些时候推出，如果去年的 L 版本是任何迹象的话。

[Android M 预览图片](http://developer.android.com/preview/download.html)||[系统图片闪烁指令](https://developers.google.com/android/nexus/images#instructions) | Google