# 如何在你的电脑上安装 SteamOS 测试版

> 原文：<https://lifehacker.com/how-to-install-steamos-on-your-computer-1484150623>

SteamOS 已经 [终于落下了它所有的 beta 荣耀](https://lifehacker.com/steamos-beta-is-available-for-download-1482911466) 。如果你是幸运的 300 人中的一员，拥有一些可以玩的硬件，你就万事俱备了。然而，我们其余的人必须将它安装在我们自己的机器上。以下是如何做到这一点。

Watch

在我们开始之前，有一些非常重要的警告:

*   这将擦除您的机器。由于 Valve 分发此映像的方式，您无法使用现有设置对硬盘进行分区或双重引导。这是一个恢复映像，如果您尝试将它安装在同一个硬盘上，您的分区表将被清除。如果想无损地摆弄一下，可以在虚拟机 里试试 [。一旦你安装了 SteamOS，你可以创建一个新的 Windows 分区，但是这将会清除你现有的设置。](http://steamcommunity.com/sharedfiles/filedetails/?id=204085700#-1)
*   **这也可能会擦除您的辅助硬盘。**基本方法不适用于在具有多个驱动器的系统上安装。根据启动表的设置方式，您也可能会无意中丢失其他驱动器上的数据。为了安全起见，移除所有硬盘，除了你想安装 SteamOS 的硬盘。
*   你需要一个 NVIDIA 显卡。对不起 AMD 用户。据报道，支持将在未来到来，但现在如果你没有 NVIDIA 显卡，你将不得不坐在这里。

### 你需要什么

开始之前，您需要下载和/或收集以下内容:

*   [steams OS 安装程序](http://repo.steampowered.com/download/) (这里有一个 [非官方洪流](http://magnet/?xt=urn:btih:1e4dae83371ba704d5d89e1828068ef0c4151e32&dn=SteamOSInstaller.zip&tr=udp%3A%2F%2Ftracker.openbittorrent.com%3A80%2Fannounce&tr=udp%3A%2F%2Ftracker.publicbt.com%3A80%2Fannounce) )
*   4GB 或更大的 u 盘
*   支持 UEFI 的主板

安装 SteamOS 有两种主要方法，您使用哪种方法将决定您需要哪种下载。最简单的方法是刷新恢复光盘映像，下载大约 2.4GB(在上面的链接中称为“SYSRESTORE.zip”)。稍微复杂一点的方法有所有有趣的专家按钮，大约 960MB，标记为“SteamOSInstaller.zip”。

### 方法 1:简单的方法

启动和运行 SteamOS 最简单的方法是安装恢复映像。再次提醒，这种方法将完全清除您的整个硬盘驱动器，不管分区。只要你做好了准备，你可以这么做:

1.  将 u 盘格式化为 FAT32。将其命名为“SYSRESTORE”。
2.  解压缩 SYSRESTORE.zip 并将其内容放在 USB 驱动器上。
3.  [从 u 盘](http://lifehacker.com/how-to-boot-from-a-usb-drive-or-cd-on-any-computer-5991848)启动机器。
4.  引导时，从引导菜单中选择 UEFI 条目。
5.  选择“恢复整个磁盘”

该方法将在您的机器上创建一个完整的、随时可用的 SteamOS 安装。如果你想在 Windows 系统上安装双引导程序，你现在就可以设置了。虽然这是基于 Debian，我们的双启动 Windows 和 Ubuntu 指南至少可以帮你指出正确的方向。

### 方法 2:先进、灵活的方式

如果你更喜欢冒险(或者想尽量减少直接从 Steam 下载的量)，你可以使用第二种方法。这种方法与前一种方法有两个主要区别。首先，下载量要小得多。部分原因是因为一旦你安装了操作系统，你仍然需要下载 Steam。你安装的大部分只是 Debian 的定制版本。

更重要的是，这种方法有一个专家安装模式。您可以使用这种方法来调整一些设置。也就是说，如果您对 Linux 发行版和安装不是很有经验，您可能不应该弄乱它。

要通过这种方法安装 SteamOS，请按照下列步骤操作:

1.  将较小的 SteamOSInstaller.zip 文件解压到 u 盘。
2.  [从 u 盘](http://lifehacker.com/how-to-boot-from-a-usb-drive-or-cd-on-any-computer-5991848)启动机器。
3.  从引导菜单中选择 UEFI 条目。
4.  选择“自动安装”
5.  安装完成后，引导进入操作系统。您将会看到一个登录屏幕。有一个默认帐户，用户名和密码都是“steam”。使用这些凭据登录。
6.  双击桌面上的 Steam 图标下载并安装 Steam。
7.  之后，您可以使用相同的凭证通过您在步骤 5 中使用的登录菜单(通过下拉框选择“SteamOS ”)登录 SteamOS。

如果你想维护 Debian 的安装，并且只在需要的时候才登录 SteamOS，你可以直接在这里结束。然而，如果你想一直提交，从最后一节的第 8 步开始，按照 Valve 的说明 [这里](http://store.steampowered.com/steamos/buildyourown) 进行最后的定制调整，使分区 100%为 Steam。

### 方法#2.5:关于虚拟化的说明

好吧，那么你已经走了这么远，你仍然不确定你要冒险。这是公平的。SteamOS 仍然是一个测试版，它需要一个相当大的承诺。如果你还想尝试一下，你可以在 VirtualBox 中安装 SteamOS。如果您还没有安装 VirtualBox， [我们这里的向导](https://lifehacker.com/the-beginners-guide-to-creating-virtual-machines-with-v-5204434) 将帮助您开始安装。

创建虚拟化 SteamOS 机器的过程比上面的安装稍微复杂一点，但是 [这个指南](http://steamcommunity.com/sharedfiles/filedetails/?id=204085700#-1) 可以很好地引导你完成这个过程。它建立在上面的方法#2 的基础上，虽然不是 USB 安装，而是在安装程序中创建一个 ISO。但是请记住，在虚拟机中运行 SteamOS 可能会导致一些非常糟糕的性能，并且几乎肯定不会对真正的游戏有好处。这种方法可能最适合那些只想瞎搞的无聊的好奇者(他们不满足于摆弄大图片并声称它是好的)。

<small>*标题图片由*</small>[<small>*kaczor 58*</small>](http://www.shutterstock.com/pic.mhtml?id=49295692)<small>*(Shutterstock)和*</small>[<small>*sash kin*</small>](http://www.shutterstock.com/pic.mhtml?id=131230868)<small>*(Shutterstock)。*</small>