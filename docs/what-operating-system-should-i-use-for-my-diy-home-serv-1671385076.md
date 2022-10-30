# 我的 DIY 家庭服务器应该使用什么操作系统？

> 原文：<https://lifehacker.com/what-operating-system-should-i-use-for-my-diy-home-serv-1671385076>

亲爱的 Lifehacker，
我准备冒险和 [建立我自己的家庭服务器](https://lifehacker.com/how-can-i-build-a-quiet-low-powered-home-file-server-5938883) ，但是我不确定我应该走哪条路线。我看过 FreeNAS，Amahi，甚至普通 ol' desktop Linux 的指南，但是应该用哪个呢？这有关系吗？

Watch

真诚地，
这么多服务器

亲爱的众多服务器，你是对的，现在有很多选择，我们在过去已经写了很多，但是我们从来没有真正比较过它们。因此，这里有一些我们最喜欢的选择，以及它们之间的区别(这样你就可以决定哪一个最适合你)。

### 简单，几乎可以做任何事情

如果你正在寻找建立一个家庭服务器， [阿玛希](https://www.amahi.org) 可能是开始的地方。它易于设置，易于管理，并支持大量不同的应用程序，包括 Plex，Crashplan，Transmission，ownCloud，OpenVPN，SABnzbd+，Sick Beard，Couch Potato，以及 [许多许多](https://www.amahi.org/apps) 。所有的应用程序都可以通过 Amahi 的界面一键安装，但大多数都需要几块钱——但为了方便，还是值得的。

然而，如果你不能通过 Amahi 的界面做任何事情——或者如果你不想支付一键安装费用——你可以在 Amahi 的基本操作系统上 [安装一个更传统的 Linux 桌面](https://wiki.amahi.org/index.php/GUI_Install_for_Express_CD) 并自己完成。所以基本上，如果你能在 Linux 上做到这一点，你可能也能在 Amahi 上做到这一点，使它成为广泛人群的完美解决方案。如果你是一个普通的家庭用户，首先从 Amahi 开始。 [查看我们的指南](https://lifehacker.com/turn-an-old-pc-into-a-nas-vpn-media-streamer-and-mor-1516484110) 获取分步说明。

### FreeNAS:企业级 RAID 支持

[FreeNAS](http://www.freenas.org/) 是一款非常流行的家庭服务器操作系统。虽然它适用于简单的家庭服务器，但它确实更适合高级人群——这一点可能对大多数用户来说并不理想(至少与 Amahi 等更简单的选项相比)。它的最新版本 9.3 抛弃了低资源的 UFS 文件系统，只支持 ZFS。ZFS 是 RAID 设置的绝佳解决方案，但它需要 [大量资源](http://www.freenas.org/faq/)——包括你安装的每 TB 存储至少 1GB 的 RAM。那可以加起来很多。

因此，虽然 FreeNAS 有很多有用的插件，如 Plex、亚音速、Crashplan、Transmission 等程序，但对大多数家庭用户来说并不理想。如果您计划在家中安装一台企业级服务器，FreeNAS 是一个很好的选择，但大多数临时用户最好选择以下选项之一。查看我们的免费旅游指南 了解基本情况。

### NAS4Free:服务文件，服务好文件

如果你想要类似的东西，但是更容易使用——并且更适合低功率的机器——你可以尝试 [NAS4Free](http://www.nas4free.org/) 来代替。它本质上是一个仍由社区维护的旧版本的 FreeNAS，对于简单或高级的文件服务器，比如说，在一台旧计算机上，它是非常棒的。它没有像 FreeNAS 和 Amahi 那样的插件支持，但如果你只是想在你的网络上提供文件服务，这是一个不错的选择。查看 [Ars Technica 对 FreeNAS 和 NAS4Free](http://arstechnica.com/information-technology/2014/06/the-ars-nas-distribution-shootout-freenas-vs-nas4free/8/) 的比较，了解两者之间更深入的差异，以及 [我们的 NAS4Free 指南](https://lifehacker.com/turn-an-old-computer-into-a-networked-backup-streaming-5822590) 了解设置它的信息。

### Linux:熟悉、免费、强大

如果你已经熟悉了像 Ubuntu 这样的 Linux 发行版，你可以考虑只运行一个 Linux 桌面作为你的家庭服务器。Ubuntu 并不十分理想，但你可以使用一些功能较低的东西，如 [Xubuntu](http://xubuntu.org/) 或 [Debian](https://www.debian.org/) ，用 TeamViewer 远程访问你的机器，并像设置任何其他计算机一样进行设置。你不需要学习任何新的东西，它可以做任何 Linux 桌面可以做的事情。

如果你习惯从命令行做任何事情，像 [Ubuntu Server](http://www.ubuntu.com/download/server) 这样的面向服务器的操作系统(或者只是最小的 Debian 安装)可能会更好，因为你不必在 GUI 上浪费任何资源。

当然，由于 Amahi 有一个全功能的 Linux 桌面运行，您也可以使用 Amahi 来完成大部分工作——所以没有理由从头构建您自己的服务器，除非您想使用特定的发行版，或者想要一个完全定制的系统来满足您的需求。如果你不想创建 Amahi 帐户，也不想为 Amahi 的任何应用程序付费，这也是一个不错的选择。我们不再为此重新推荐 Ubuntu，但是我们在 Ubuntu 家庭服务器 上的旧指令应该可以在许多 Linux 发行版上工作，包括 Debian。

### 其他选择

当然，这些远不是唯一的选择，但它们是一些更受欢迎的选择。开发者和 IT 专业人士可能也会喜欢 [OpenMediaVault](http://www.openmediavault.org/) ，它比 Amahi 更复杂，但允许通过其 API 进行大量定制。Windows 用户可能更喜欢在备用计算机上运行 Windows 8 来共享文件和共享驱动器，如果你想最大限度地兼容其他 Windows 系统，这是一个很好的选择。

当然，如果你有花不完的钱，你最好完全避免自己动手做 [一个预建的 NAS 机箱](https://lifehacker.com/five-best-nas-enclosures-5968677) ，就像来自 [Synology](https://www.synology.com/) 的一个。它们可能比你自己构建的任何东西都要小，也可能更容易设置。它们也会更贵，但是如果你不想做太多的工作，这是一个不错的选择。

这不是世界上最详细的比较，但这应该给你一个好主意，先尝试什么。不管你的需求是什么，这些操作系统中的一个应该能够满足它们。实验愉快，祝你好运！

真诚地，
Lifehacker

<small>*标题图像由*</small> [<small>*李果*</small>](http://www.shutterstock.com/pic.mhtml?id=173774591&src=id)<small>*(Shutterstock)*</small>[<small>*gr Marc*</small>](http://www.shutterstock.com/pic.mhtml?id=115666318&src=id)<small>*(Shutterstock)，以及*</small>[<small>*Yganko*</small>](http://www.shutterstock.com/pic.mhtml?id=141559378&src=id)