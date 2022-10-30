# GravityBox 在一个可定制的包中添加了大量对 Android 的调整

> 原文：<https://lifehacker.com/gravitybox-adds-a-ton-of-tweaks-to-android-in-one-custo-1502250290>

Android ( [根源](https://lifehacker.com/everything-you-need-to-know-about-rooting-your-android-5789397) ): [闪烁 rom](http://lifehacker.com/five-best-android-roms-5915093)是定制你的 Android 体验的一个很好的方式，但是如果你不想 [处理 ROMming 过程](http://lifehacker.com/this-database-of-android-roms-helps-you-choose-the-best-1449794780) ，GravityBox 对普通 Android 进行了大量的调整。

Watch

GravityBox 实际上是[exposed](http://forum.xda-developers.com/showthread.php?t=1574401)的一个模块，这个令人敬畏的框架 [让你基本上创建你自己的定制 ROM](https://lifehacker.com/how-to-create-your-own-customized-version-of-android-wi-1440101209) ，只包含你想要的特性——并且不需要 ROM 刷新。因此，您需要根化并安装 Xposed 框架才能工作，但是它非常容易设置。更多信息，请查看我们关于 x exposed 的指南。

可以把 GravityBox 看作是 Xposed 框架的“启动包”。GravityBox 没有逐一安装你想要的每个功能，而是包含了大量最流行的 Android 调整，你可以根据自己的需要启用或禁用这些调整。它包括(但不限于):

*   CyanogenMod 饼图控件
*   自定义状态栏的快速设置(以及 Android 最初没有的新磁贴)
*   其他锁屏功能
*   用状态栏控制亮度
*   更改状态栏中图标的颜色和样式
*   没有通知时自动切换到快速设置
*   向关机菜单添加更多项目
*   使用音量键跳过曲目
*   在某些手机的硬件按键上添加新的操作
*   可扩展体积面板
*   取消通知和铃声音量的链接
*   电话应用程序的拨号器调整
*   自定义通知抽屉样式
*   更多

请注意，GravityBox 不能在现有的定制 rom 上工作，如 CyanogenMod 甚至三星的 touch wiz——你需要运行普通的 Android(或非常接近它的东西)才能让 GravityBox 工作。查看 XDA 开发者的 GravityBox 线程( [这个用于糖豆](http://forum.xda-developers.com/showthread.php?t=2316070) 和 [这个用于 KitKat](http://forum.xda-developers.com/showthread.php?t=2554049) )了解更多信息。

要安装 GravityBox，只需 [按照我们的说明安装曝光的](https://lifehacker.com/how-to-create-your-own-customized-version-of-android-wi-1440101209) (如果你还没有)，然后:

1.  在开始之前，从你的手机的恢复模式做一个 Nandroid 备份，以防出现任何问题。
2.  从 XDA 线程下载并运行重力盒 APK。或者，您可以在 Xposed 应用程序的下载部分找到它。同样，确保你下载了适合你的 Android 版本的正确版本——有一个用于糖豆 的 [和一个用于 KitKat](http://forum.xda-developers.com/showthread.php?t=2316070) 的 [。](http://forum.xda-developers.com/showthread.php?t=2554049)
3.  转到 Xposed 的“模块”部分，GravityBox 应该会出现。选中该框以启用它。(如果不起作用，你可能需要先重启手机，然后再尝试勾选复选框。)
4.  检查完重力盒后，重启你的手机。
5.  再次打开 Xposed 应用程序，在模块部分点击 GravityBox 的条目。这将打开 GravityBox 的设置，你可以开始调整你的心的内容。

默认情况下，GravityBox 没有启用任何额外的功能，因此您可以从头开始构建您的自定义 Android 版本。

像往常一样，像这样的调整，一定要在开始之前在 XDA Developers 阅读整篇文章，并在开始之前做好备份。我一直在我的 Nexus 4 上测试 GravityBox，到目前为止它非常棒。点击下面的链接查看。

[【重力盒】Android 4.1/4.2/4.3](http://forum.xda-developers.com/showthread.php?t=2316070) 的调整盒| XDA 开发者论坛

[【重力盒】-安卓 4.4](http://forum.xda-developers.com/showthread.php?t=2554049) 的调整盒| XDA 开发者论坛