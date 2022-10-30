# NetfliXBMC 为 XBMC 带来了更好的遥控网飞

> 原文：<https://lifehacker.com/netflixbmc-brings-a-better-remote-controlled-netflix-t-1484237283>

有了一台好的家庭影院电脑，你可以 [播放任何东西](https://lifehacker.com/create-a-kickass-seamless-play-everything-media-cente-5900626)——尽管网飞总是有点困难。一个名为 NetfliXBMC 的新 XBMC 插件使这一过程比以往任何时候都更加简单和高效。下面是如何设置它。

Watch

已经有一些网飞插件了，但是因为网飞使用 Silverlight 和一些严格的 DRM，它总是很难与 XBMC 集成。由用户 AddonScriptorDE 创建的 NetfliXBMC 是我们见过的最好的附加组件，它只需要几分钟就可以设置好。

### 你需要什么

与其他 XBMC 附加组件不同，它不像安装和运行附加组件那么简单。在开始之前，您需要下载一些东西:

*   运行在 Windows、OS X 或 Linux 上的 XBMC 12“佛罗多”。在本指南中，我们将使用 Windows，但会注意这些不同之处。如果你使用的是我们价值 500 美元的 [媒体中心建筑](http://lifehacker.com/how-i-built-the-media-center-of-my-dreams-for-under-50-5936546) 或类似的东西，这个指南会让你非常顺利地完成这个过程。Linux 用户需要安装 pipellight[，如附加组件页面](http://forum.xbmc.org/showthread.php?tid=178693) 所述。
*   Chrome 浏览器、Safari 浏览器或 Internet Explorer 浏览器。NetfliXBMC 需要一个浏览器来播放视频，所以你需要安装一个浏览器(目前不支持 Firefox)。在本指南中，我们将使用 Chrome。
*   **一个网飞账户**。原因很明显。

### 第一步:安装 Chrome Launcher 和 NetfliXBMC

您需要两个附加组件来完成这项工作，并且您不会在默认的 XBMC 库中找到它们。因此，要安装它们:

1.  [在这里](http://code.google.com/p/addonscriptorde-beta-repo/downloads/list) 下载 AddonScriptorDE 的测试库。将它保存到您的下载文件夹(或任何您想要的地方)。
2.  打开 XBMC，进入设置>附加组件>从 ZIP 文件安装。选择您刚刚下载的 ZIP 文件，它应该会安装存储库。
3.  前往获取附加组件并选择 AddonScriptorDE 的测试回购。如果里面什么都没有，回到获取附加组件菜单，按“c”键调出上下文菜单，然后选择“强制刷新”如果您返回到 AddonScriptorDE 的测试报告，您应该会看到一个类别列表。
4.  进入程序插件，选择“Chrome 启动器”按 Enter 键并安装附加组件。
5.  一旦安装了 Chrome Launcher，回到类别列表，进入视频插件。选择 NetfliXBMC 并安装。

现在，您应该已经安装了所有必需的附加组件，可以继续下一步了。

### 第二步:配置 NetfliXBMC

接下来，你需要设置 NetfliXBMC 来使用你的网飞帐户和其他偏好设置。前往 XBMC 的视频>视频附加组件，突出显示 NetfliXBMC，然后按“c”键调出上下文菜单。选择“附加设置”开始。这里有一些你可能想调整的东西:

*   **账号>邮箱和密码**:在这里输入你的网飞凭证。
*   **账户>单用户账户**:如果你的网飞账户 上有 [多个配置文件，你会想要取消选择这个(否则你的浏览器每次都会询问你，这不容易用遥控器控制)。如果您有多个用户在同一台 XBMC 机器上使用网飞，请选择“每次启动时显示配置文件选择”选项，这将询问您每次使用该插件时哪个用户正在观看。](http://lifehacker.com/netflix-profiles-ensure-roommates-wont-mess-up-your-re-987927584)
*   **高级>删除缓存/删除 cookie**:如果您在登录时遇到问题，请尝试这些按钮。
*   **高级> Win 浏览器/OS X 浏览器**:如果你使用的是 Internet Explorer 或 Safari 浏览器，而不是 Chrome 浏览器，你需要在这里选择你的浏览器。

一旦你设置好了，进入 NetfliXBMC，试着播放一部电影或电视剧。如果你遇到问题，试着调整设置让它工作，或者看看这篇文章底部的故障排除部分。

如果你可以播放视频，那么现在是最后一步:设置你的遥控器。

### 第三步:配置遥控器(可选)

如果你用遥控器 (而不是鼠标和键盘)控制你的家庭影院电脑，你也需要为你的遥控器配置 NetfliXBMC。

在 Windows 上，NetfliXBMC 有一个小助手应用程序，它在后台运行，并将你指定的按键映射到网飞的内置快捷方式。回到 NetfliXBMC 的设置，转到高级标签，并前往配置控制实用工具。在那里，只需输入每个任务要使用的键。你可能需要查找遥控器上的哪个键对应哪个按钮才能做到这一点——尽管 XBMC 的默认键盘快捷键是一个很好的起点。

我们还没有测试 Mac 和 Linux 版本，所以请查看 NetfliXBMC 的论坛帖子 了解更多关于用遥控器控制网飞的信息。通常它只需要单独安装一个小应用程序并映射您的按键，就像上面的 Windows 说明一样。

### 如果你有问题

NetfliXBMC 仍然处于早期阶段，但在我们的测试中，它工作得相当好。但是，根据您的设置，您可能会遇到问题，也可能不会遇到问题。确保你已经逐字阅读了整个指南，以及 NetfliXBMC 论坛帖子[。如果您仍然有问题，该线程是询问它们的最佳位置，尤其是如果它是开发人员需要修复的 bug 的结果。他非常敏感，所以如果你有困难，不要害怕让他知道！祝你好运！](http://forum.xbmc.org/showthread.php?tid=178693)