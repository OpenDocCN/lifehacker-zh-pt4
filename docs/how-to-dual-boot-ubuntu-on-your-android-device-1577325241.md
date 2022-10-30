# 如何在你的 Android 设备上双启动 Ubuntu

> 原文:[https://life hacker . com/how-to-dual-boot-Ubuntu-on-your-Android-device-1577325241](https://lifehacker.com/how-to-dual-boot-ubuntu-on-your-android-device-1577325241)

Canonical 为设备开发 Ubuntu 已经有一段时间了。不幸的是，用它来玩真的不容易。然而，如果你想尝试一下(并拥有一个最新的 Nexus 设备)，这从来没有比双重启动更容易。

Watch

最近，Canonical 宣布了对其 Ubuntu 双引导应用程序 的 [更新——允许你并行运行 Ubuntu 和 Android 这使得直接在你的设备上更新](http://developer.ubuntu.com/2014/05/announcing-ubuntu-dual-boot-with-enhanced-upgrades-and-more/)[Ubuntu for Devices](http://www.ubuntu.com/phone/features)(Ubuntu 的手机和平板电脑版本的名称)更加容易。这意味着你不仅可以在不损坏手机的情况下试用 Ubuntu，还可以看到所有甜蜜的新变化，而不必大惊小怪。听起来对修补者来说是双赢。

*免责声明:* Ubuntu for Devices 目前仍处于开发者预览阶段。因此，它可能没有足够完整的功能来作为您的日常驱动程序。这就是我们双启动的原因。自然，你应该预料到道路上会有一些颠簸。此外，Ubuntu 的应用程序使用 HTML5，但该平台上的许多“应用程序”实际上只是常规的移动网站。甚至包括一些被收录的(比如 Twitter)。在撰写本文时，一些“应用程序”会在你第一次运行它们时提示你安装一个 Android 应用程序。**不要这样。** Ubuntu 不是基于 Android 开发的，Android 应用程序也不能在上面运行。试图安装它们——甚至打开应用程序的链接——都可能会破坏东西。

### 你需要什么

要开始安装 Ubuntu Dual Boot(以及随后的 Ubuntu 本身)，以下是你需要的:

*   **一个 Nexus 4，Nexus 7 (2013)，或者 Nexus 10:** 这三个是目前唯一的 [官方积极支持的安卓设备](http://developer.ubuntu.com/start/ubuntu-for-devices/devices/) 。如果你没有这些手机或平板电脑，你可以在用户移植部分 [这里](https://wiki.ubuntu.com/Touch/Devices) 查看**非官方支持的设备列表**。然而，我们的指南将集中在这三个方面。他们也必须运行 Android 4.4.2，所以如果你还没有更新，现在是一个好时机。
*   **Root 权限:**在安装 Ubuntu 之前，你需要确保你的手机或者平板电脑已经 [拥有 root](http://lifehacker.com/everything-you-need-to-know-about-rooting-your-android-5789397) 。幸运的是，我们看到的三个 Nexuses 都可以使用 [fastboot oem 解锁方法](http://wiki.cyanogenmod.org/w/Template:Fastboot_oem_unlock) 。如果你没有先扎根，先处理好再回来。
*   **Ubuntu 安装(非 Live CD):** 为了安装 Ubuntu Dual Boot，你需要在电脑上安装桌面版 Ubuntu。遗憾的是，Live CD 版本不允许您安装必要的组件。然而，如果你有大约 25GB 的空闲空间，你可以 [安装它，相对来说没什么痛苦](http://lifehacker.com/getting-started-with-linux-installing-linux-on-your-co-5774997) 。
*   **ADB:** 你需要安装 ADB 来设置双引导(如果你还没有安装的话，还需要启动你的设备)。幸运的是，在大多数现代 Linux 发行版中，您可以通过一个简单的命令来实现。在 Ubuntu 中，打开一个终端，输入以下内容:`sudo apt-get install android-tools-adb`
*   **设备上大约 2.7GB 的可用空间:** Ubuntu for Devices 需要大约 2.7GB 的空间来存放操作系统和相关文件。如果空间不足，在开始之前清理一些空间。

一旦你把一切都设置好了，你就准备好迎接主赛事了。

### 如何安装 Ubuntu 双引导

Canonical 已经创建了一个(相对)简单的脚本，用于在您的 Android 设备上安装必要的双引导应用程序。一旦你完成了上一部分的所有基础，启动 Ubuntu 并执行以下操作:

#### 启用 USB 调试

首先，你需要在手机或平板电脑上启用 USB 调试，如果还没有的话。下面是如何做到这一点:

1.  在平板电脑上，打开“设置”应用程序，然后选择“关于平板电脑”
2.  轻按“内部版本号”七次以启用开发人员模式。
3.  返回主设置菜单。
4.  点击新的开发人员选项。
5.  启用 USB 调试。

完成后，用微型 USB 电缆将平板电脑连接到电脑。

#### 安装 Ubuntu 双启动应用程序

接下来，从 [这里](http://humpolec.ubuntu.com/latest/dualboot.sh) 下载 Ubuntu 双引导安装脚本到你的主目录。然后按照以下说明操作:

1.  打开一个终端窗口(Ctrl+Alt+T)。
2.  运行以下命令使脚本可执行:`chmod +x dualboot.sh`
3.  通过运行以下命令执行脚本:`./dualboot.sh`

注意:在我用 Nexus 7 对全新安装的 Ubuntu 进行的测试中，脚本在试图执行 curl 命令时陷入了一个循环(如下所示)。如果您遇到这种情况，请关闭终端窗口，打开一个新窗口，并运行以下命令来安装包:`sudo apt-get install curl`这将安装必要的组件。完成后，再次运行双引导安装脚本。

#### 下载并安装 Ubuntu for Devices

该脚本将自动运行，并重置您的设备几次。一旦完成，你的手机或平板电脑应该会回到 Android 主屏幕。在那里，从你的应用抽屉里打开新的 Ubuntu 双启动应用。然后:

1.  轻按“选取要安装的频道”
2.  选择下载渠道(Canonical 推荐“乌托邦”)。
3.  当要求超级用户访问时，点击“授权”。
4.  一旦 Ubuntu 完成下载和安装，点击重新启动到 Ubuntu。

恭喜你！你现在可以在手机或平板电脑上运行 Ubuntu 了。现在你只需要访问它。

### 如何在 Android 和 Ubuntu 之间切换

与许多其他双引导解决方案不同，您不需要在启动时选择您想要的操作系统。相反，一旦你启动到 Android，打开 Ubuntu 双启动应用程序，点击“重启到 Ubuntu”。你的设备将重启进入 Ubuntu。然而，无论你在哪个操作系统中，**硬重启总是会引导到 Android** 。这通常是通过按住电源按钮大约十秒钟来完成的。如果你愿意，Ubuntu 中还有一个双启动应用程序可以切换回 Android。

你也可以从 Android 中的 Ubuntu Dual Boot 应用程序或者 Ubuntu 的系统设置中更新 Ubuntu。然而，这两种方法都要求你在 Android 中安装更新，所以无论如何，最好是在更新的时候先启动 Android。