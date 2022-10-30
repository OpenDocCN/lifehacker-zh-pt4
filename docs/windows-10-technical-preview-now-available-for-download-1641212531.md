# 如何立即安装 Windows 10 技术预览版

> 原文：<https://lifehacker.com/windows-10-technical-preview-now-available-for-download-1641212531>

昨天，微软公布了最新版本的 Windows[。如今，该公司允许喜欢冒险的用户(比如你)免费试用。以下是方法。](https://lifehacker.com/all-the-new-stuff-in-windows-10-1640838152)



### 安装前

在你做任何事情之前，有几个警告你应该知道:

*   首先备份您的数据！ [反正不是说你有什么借口不去](http://lifehacker.com/theres-no-excuse-for-not-backing-up-your-computer-do-1547987206) ，但是如果你有什么无法恢复的东西，一定要在升级之前对你的数据进行备份。或者即使你不知道。做个备份就行了。
*   您将无法使用您的恢复分区来降级。如果您的系统上有一个恢复分区，它将无法再将您的计算机恢复到以前的 Windows 版本。
*   您需要外部恢复介质来撤消升级。正如你所料，由于你没有恢复分区，如果你不喜欢或不能使用 Windows 10，你需要一个装有 Windows 8(或更旧版本)的光盘或 USB 驱动器来恢复原状。

正如微软多次提到的，这是预发布软件，预计会有很多错误，很可能会崩溃。此外，他们可以 [收集大量数据](http://lifehacker.com/windows-10s-keylogger-fiasco-has-been-blown-out-of-pr-1642931793)——包括你键入的文本或你打开的文件种类——以改进产品。**不建议你把这个安装在你的工作机器或者任何你日常需要或者敏感使用的东西上**。我们将向您展示如何在备用 PC 上安装它，或者如果您没有，在 VirtualBox 中安装它。如果你不确定是否要安装它， [我们的视频演练](https://lifehacker.com/heres-what-windows-10-looks-and-feels-like-1641369982) 可以让你一窥它的外观和感觉。

### 你需要什么

这一次，微软创造了 [Windows Insider 程序](https://insider.windows.com/) 让用户测试新的热点。你需要同意一个特殊的条款和条件，除了通常的行话之外，可能主要包括“如果这打破了你的东西，不要责怪我们”。除了下载更新，Insider 计划将是您提供反馈和从社区获得帮助的方式。

一旦您注册了该计划，以下是您需要的:

*   足够大的 DVD 或 USB 驱动器，可容纳 4GB 的 ISO 文件。
*   Windows 10 ISO 文件之一
*   安装它的备用电脑(微软不建议使用你的日常驱动)，或者安装在你的主机上的 [VirtualBox](https://www.virtualbox.org/) 。

一旦您注册了 Insider 计划，您将被引导下载几个 ISO 文件中的一个。目前，在 32 位和 64 位配置中，支持四种语言(英语、英国英语、简体中文和巴西葡萄牙语)。获取符合您需求的版本，让下载发挥作用。虽然你可能想吃点零食，因为下载的大小从 3-4GB 不等。

### 选项一:在您的电脑上安装 Windows 技术预览版

一旦你有了你需要的一切，按照以下步骤:

1.  将 ISO 复制到磁盘或 USB 驱动器。你可以使用类似 ImgBurn 这样的工具来解压缩内容，不过如果你在已经运行 Windows 的设备上安装，操作系统应该能够自己挂载 ISO。
2.  将磁盘或 USB 驱动器插入要安装 Windows 10 的计算机。
3.  如果您在该计算机上安装了旧版本的 Windows，请启动它，并从安装介质中双击 setup.exe。如果没有，您可以从安装盘 的 [引导您的电脑开始安装。](http://lifehacker.com/how-to-boot-from-a-usb-drive-or-cd-on-any-computer-5991848)
4.  按照向导在您的计算机上安装 Windows。

Microsoft 的向导将引导您完成剩余的安装过程。如果您想进行全新安装，请确保在向导过程中选择“不保留任何内容”。

### 选项二:在 VirtualBox 中安装 Windows 技术预览版

如果您没有备用机器来试用技术预览版，我们建议您将其安装在 VirtualBox 中。这样，您可以尝试一下，看看有什么新的东西，并在不覆盖您的主系统的情况下进行尝试。

1.  [下载安装最新版本的 VirtualBox](https://www.virtualbox.org/) ，启动。
2.  单击主窗口中的“新建”按钮创建新的虚拟机。
3.  给你的操作系统起个名字(比如“Windows 10 技术预览版”)，从列表中选择 Windows 8.1(因为 VirtualBox 还没有 Windows 10 选项)。
4.  按照 VirtualBox 向导设置您的虚拟机。你可以 [在这里](https://lifehacker.com/the-power-users-guide-to-better-virtual-machines-in-vir-1569943402) 了解更多关于 VirtualBox 的设置，不过默认设置应该没问题。
5.  完成后，您应该会在左侧边栏中看到您的新机器。点击它并点击位于 VirtualBox 窗口顶部的设置按钮。
6.  在左侧边栏中指向存储，在“控制器:IDE”旁边，单击添加 CD 按钮。
7.  选择“选择磁盘”并导航到您下载的 Windows 10 ISO。
8.  单击确定。
9.  按 Start 启动您的新虚拟机，并完成 Windows 10 安装过程。

为了改善您的 VirtualBox 体验，请查看我们的 VirtualBox 高级用户指南，了解可以加快系统速度的调整和提示。

记住，这是预发布软件，安装风险自担！如果你对拿你的机器冒险不感兴趣，我们会仔细研究新的操作系统，让你知道 Windows 10 在接下来的几天里还有什么很酷的东西。祝你好运！