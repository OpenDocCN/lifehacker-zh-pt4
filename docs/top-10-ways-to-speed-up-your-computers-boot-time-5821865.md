# 加速计算机启动时间的 10 大方法

> 原文:[https://life hacker . com/top-10-ways-to-speed-your-computers-boot-time-5821865](https://lifehacker.com/top-10-ways-to-speed-up-your-computers-boot-time-5821865)

如果有一件事每个人都害怕，那就是重启他们的电脑。这可能只需要一两分钟，但它可能会像永远。以下是我们的 10 大调整，可以让你的电脑启动得更快一点。

Watch

这是一个非常有争议的话题，因为有很多关于创业的神话。因此，我们走上街头(在互联网上)，尽可能多地搜索我们能找到的简单、有充分依据的提示。可能还有其他的，其中一些是有争议的，但这 10 件事几乎肯定能让你得到一台启动更快的机器。

## 10.调整你的 BIOS

当你第一次设置你的计算机时，你的 BIOS 被设置成使事情对你来说更加方便，但是一旦你设置好了，那些事情可以被禁用。如果您在启动电脑时按住 DEL 键(或 BIOS 告诉您进入设置的任何键)，您可以打开“快速启动”选项，并将您的硬盘移动到启动优先级列表的顶部。快速启动设置将关闭您的计算机首次开机时运行的测试，启动优先级调整将告诉您的计算机*而不是*在它首次启动时寻找 CD、拇指驱动器或其他媒体，这将使您更快地启动到您的操作系统。如果需要的话，你可以随时从光盘 [启动](http://lifehacker.com/how-to-boot-from-a-usb-drive-or-cd-on-any-computer-5991848) 。

## 9.清除启动时启动的程序

加速启动过程的最可靠的方法之一是阻止不必要的程序随计算机一起启动。在 Windows 10 中，您可以通过按 Ctrl+Alt+Esc 打开任务管理器，然后转到启动选项卡来完成此操作。如果你还在运行 Windows 7，打开开始菜单，键入`msconfig`，然后回车。当你启动电脑时，你会看到所有启动的程序。

[这个应用程序列表](https://lifehacker.com/know-which-apps-to-remove-from-msconfig-with-this-start-5718799) 会告诉你这些应用程序中的每一个是做什么的，这样你就知道哪些你可以禁用，哪些你不想禁用。 [之前提到的](http://lifehacker.com/soluto-is-an-awesome-tool-to-speed-up-your-system-boot-5561303) [Soluto](http://www.soluto.com/) 也是清理这些程序的一个极好的方法，现在它还有一堆其他方便的功能，值得下载。

## 8.延迟启动时运行的 Windows 服务

许多人认为从`msconfig`开始禁用服务也会加快你的启动时间，但是我们发现 [比](https://lifehacker.com/debunking-common-windows-performance-tweaking-myths-5033518) 更有问题。然而， [你可以*延迟*某些启动服务](http://www.howtogeek.com/howto/windows-vista/start-your-computer-more-quickly-by-delaying-the-startup-of-a-service-in-vista/) ，这样你的电脑可以快速启动，然后再担心它们——毕竟，你启动电脑的时候并不需要所有这些服务。只需打开“开始”菜单，键入 services，然后按 enter 键—然后右键单击任何服务以更改其属性。

## 7.更改启动菜单的超时值

如果你在双引导你的机器，那么你的引导菜单可能有一个“超时值”，意思是在它引导到默认操作系统之前等待你做出选择的时间。在 Windows 上，这个超时值通常是 30 秒，如果你不是直接看着屏幕的话，这个时间会很长。要更改这个超时值，请转到`msconfig`，单击 Boot 选项卡，并将超时框中的数字更改为较低的值。如果你用 Linux 双引导，你可能正在运行 GRUB 引导菜单，你也可以 [改变超时](http://www.howtogeek.com/howto/ubuntu/change-the-grub-menu-timeout-on-ubuntu/) 。

## 6.禁用未使用的硬件

您的电脑在首次启动时会加载许多驱动程序，其中一些您甚至可能不会使用。从“开始”菜单的搜索框进入“设备管理器”,寻找任何你不用的东西——蓝牙控制器、调制解调器和虚拟 Wi-Fi 适配器是常见的罪魁祸首。右键单击要禁用的条目，然后点击“禁用”。记住，只对你实际上不使用的东西这样做——如果你使用无线托管网络，你需要保持那些虚拟 Wi-Fi 适配器启用。

## 5.安装好的杀毒软件并保持更新

这应该不用说，但我们还是要说:安装一些 [*好的*杀毒软件](https://lifehacker.com/the-best-antivirus-app-for-windows-5865356) ，保持最新，并运行定期扫描。这更多的是一种预防措施，而不是一个实际的启动加速提示，但是如果你曾经*得到*恶意软件，它肯定会减慢你的计算机的启动时间。此外，任何防病毒程序都是轻量级的，启动速度很快——所以它不会像其他臃肿的程序那样拖慢你的启动时间。

## 4.删除不必要的字体

从一开始，Windows 就在启动时加载字体，并减缓启动时间。这已经不像以前那样是个问题了，但是它仍然会让你慢下来一点。Windows 7 在启动时加载超过 200 种字体；如果你安装了微软办公软件，那就更好了。机会是，你很少使用这些字体，所以你可以隐藏它们，以加快这一进程。在 Windows 7 中，从开始菜单的搜索框中打开 Fonts 文件夹，勾选所有你不需要的字体。然后单击工具栏中的“隐藏”按钮。这样，如果你需要它们，你可以把它们带回来，但 Windows 不会在启动时加载它们。请注意，仅仅删除一些字体可能不会产生明显的影响——您可能需要删除几百种字体。也就是说，你安装的字体可能比你意识到的要多几百种，所以这并不像听起来那么荒谬。

## 3.升级你的内存

安装更多的内存一直是提高计算机速度的有效方法，这包括启动时间。如果你有一台相对较新的电脑，你可能不需要升级内存，但是如果你在一台较旧的机器上工作，特别是如果你使用许多在启动时运行的较新的程序，内存升级可能会有帮助。我们已经讨论了如何在 [中替换台式机](http://lifehacker.com/hack-attack-how-to-install-ram-138665) [和笔记本电脑](http://lifehacker.com/diy-laptop-repairs-and-upgrades-upgrading-ram-5649112) ，即使对于没有经验的人来说，这也是一个非常简单的过程。

## 2.升级您的操作系统

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-6It3HNXxEZE&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-6It3HNXxEZE&start=0) 

还在运行 Windows 7？升级到 Windows 8 或 10 将严重加快您的启动时间。并不是每个操作系统的升级都一定会更快，但从 7 到 8 的跳跃是巨大的，而且免费提供 Windows 10 的，这绝对值得转换。

## 1.安装固态硬盘

如今，您的硬盘可能是您机器中最大的瓶颈。你可以对你的电脑进行的最好的升级之一是安装一个固态硬盘，它具有超快的读取时间，可以大大加快你的启动速度。它们当然不是廉价的升级版 ，也不是没有自己的维护需求[，但是如果你想加快你的电脑和它的启动时间，安装固态硬盘是不会错的。差别将是惊人的。](https://lifehacker.com/how-to-take-full-advantage-of-your-solid-state-drive-5586733)

* * *

同样，这些不是缩短计算机启动时间的唯一方法，但它们是我们发现的一些最广为人知、最值得信赖的方法。如果你有任何自己喜欢的调整，请在评论中与我们分享，但 [当心神话和蛇油](https://lifehacker.com/debunking-common-windows-performance-tweaking-myths-5033518)——有很多调整弊大于利。

* * *

Lifehacker 的前 10 名汇集了我们最好的指南、解释者和其他关于某个主题的帖子，这样你就可以轻松应对大项目。更多内容，请查看我们的 [*<small>十大 tagpage</small>*](http://lifehacker.com/tag/lifehacker-top-10)*<small>。</small>T15】*

*标题照片由* [*亚历克斯·施文科*](http://www.flickr.com/photos/schwenke/2421138425/) 拍摄。