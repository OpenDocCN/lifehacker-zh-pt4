# 如何在您的电脑上虚拟化 Android，以便您可以在购买之前进行尝试

> 原文:[https://life hacker . com/how-to-virtualize-an-Android-device-so-you-can-try-befo-1609054771](https://lifehacker.com/how-to-virtualize-an-android-device-so-you-can-try-befo-1609054771)

你大概知道可以在虚拟机 中 [运行桌面操作系统进行测试。你可以对 Android 做同样的事情，这是在你买手机之前测试手机的好方法。下面是如何设置它。](https://lifehacker.com/the-power-users-guide-to-better-virtual-machines-in-vir-1569943402)

Watch

### **为什么要虚拟化 Android？**

你的第一个问题可能是:为什么要这么做？就像虚拟化桌面操作系统一样，出于一些原因，您可能希望在虚拟机中进行尝试。如果你第一次考虑购买安卓手机或平板电脑，设置虚拟设备是提前掌握操作系统的好方法。开发者可以使用虚拟机来尝试想法，它也给普通用户提供了尝试应用程序的机会，而不必担心影响重要的手机。它可以被看作是一个测试平台，在这里你可以尝试所有你想测试的软件。

有各种各样的虚拟化工具可以用来运行 Android，但迄今为止最令人印象深刻的是 [Genymotion](http://www.genymotion.com/) 。这款免费工具基于 VirtualBox(我们最喜欢的用于 Windows 的 [虚拟化工具)，它运行特定的设备，而不仅仅是普通的 Android 安装。例如，如果你想买一部 Nexus 7，你可以提前下载一个虚拟版本并在你的电脑上运行。](https://lifehacker.com/the-best-virtualization-app-for-windows-5861847)

### **如何设置 Genymotion**

Genymotion 非常容易安装和设置。只需遵循以下步骤:

1.  访问 [Genymotion 网站](http://www.genymotion.com/) ，点击获取 Genymotion 链接，然后下载该软件的免费版本。在这里，您还可以创建一个 Genymotion 帐户，稍后您会用到它。
2.  在您的计算机上安装 Genymotion。请注意，这将中断您的网络访问，因此在安装之前，请确保您没有运行任何大的下载。
3.  安装完成后，启动 Genymotion。它将检测到您没有设置任何虚拟设备。单击“是”创建一个。
4.  点击连接按钮，输入您的 Genymotion 用户名和密码，您将看到一个现成设备列表供您选择。

如果 117MB 的 Genymotion 下载看起来有点大，那是因为它包含了一个捆绑版本的 VirtualBox。如果你已经安装了 Genymotion，你可以下载一个 VirtualBox 免费版本，但是完整的软件包是一个不错的选择，因为它确保你需要的一切都可以获得，而不需要访问其他网站。

如果你查看 Genymotion 的设备列表，你会看到普通的手机和平板电脑，以及三星 Galaxy S5 等特定型号和 Nexus 7 等平板电脑。您可以浏览整个列表，或者使用下拉菜单根据 Android 版本和设备型号进行过滤。要选择设备:

1.  从列表中选择一个设备，然后单击下一步。
2.  为虚拟设备输入一个有意义的名称，然后单击下一步。
3.  下载完成后(大约 200MB ),单击“完成”。然后，只需从列表中选择您选择的设备，然后单击播放。

设备初始化时会有短暂的延迟，然后你会看到一个熟悉的 Android 启动屏幕。窗口右侧的一系列按钮提供切换和控制，包括屏幕旋转选项，您不必一直在纵向模式下工作。

### **安装谷歌 Play 商店和谷歌应用**

你可能会立即注意到的一件事是，Google Play 和其他谷歌应用程序不包括在内。谢天谢地，安装它们很容易:

1.  抓取 [ARM 翻译安装程序](http://goo.gl/tfjjMt) 和你正在使用的 Android 版本的 Google Apps 捆绑包:[Google Apps for Android 4.4](https://docs.google.com/file/d/12OyLsSAGPeOdmAnsZ2aH6q0K73itj1alJedDMuQA9CABUhXePuqhbwst7OKG/edit?usp=sharing)，[Google Apps for Android 4.3](https://goo.im/gapps/gapps-jb-20130813-signed.zip/)，[Google Apps for Android 4.2](https://goo.im/gapps/gapps-jb-20130812-signed.zip/)，或者[Google Apps for Android 4.1](https://goo.im/gapps/gapps-jb-20121011-signed.zip/)。
2.  下载完成后，将 ARM 翻译 ZIP 文件拖放到 Android 窗口上——无需解压缩。Genymotion 将提供使用存档来刷新虚拟设备，因此单击 OK 继续。
3.  当刷新过程完成时，单击确定，然后重新启动设备。
4.  现在，将 Google Apps ZIP 文件拖放到虚拟设备窗口，然后单击 OK 开始文件传输。
5.  重启设备，然后你就可以使用 Google Play 和其他谷歌应用了。

或者，你可以安装一个第三方商店，如 [亚马逊应用商店](http://www.amazon.com/getappstore?asc_campaign=InlineText&asc_refurl=https://lifehacker.com/how-to-virtualize-an-android-device-so-you-can-try-befo-1609054771&asc_source=&tag=kinjalifehackerlink-20) 。为此，您需要允许安装第三方应用程序。转至“设置”，单击“安全”标题，然后选中“未知来源”框。启动内置的网络浏览器，下载亚马逊应用商店。然后，您可以浏览可用的应用程序，并安装任何您感兴趣的应用程序。

没有什么可以阻止你设置多个虚拟 Android 机器，所以你可以在每个机器上尝试不同的东西，或者运行不同版本的 Android。无论你是一个正在寻找新的操作系统使用方法的经验丰富的 Android 用户，还是你想第一次尝试，Genymotion 都是一个伟大的免费选择。

*标题照片制作使用* [*微软*](http://commons.wikimedia.org/wiki/File:Windows_8_Start_screen_UI.png) *。*