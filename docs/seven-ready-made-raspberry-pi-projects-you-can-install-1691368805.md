# 七个现成的 Raspberry Pi 项目，点击几下就可以安装

> 原文：<https://lifehacker.com/seven-ready-made-raspberry-pi-projects-you-can-install-1691368805>

树莓派是 DIYers 的梦想，但如果你不想摆弄命令行和从头开始建立一个项目，这里有七个项目，你只需点击几下就可以启动并运行。



这些项目中的每一个仍然需要一点开机后设置来配置一切，但是它们都有你需要的所有软件来让你的项目快速起步。最多，你需要做的就是输入你的网络密码。

### 如何安装这些项目

要安装这些项目，你只需要将图像克隆到 SD 卡上，然后放入你的 Raspberry Pi。所有这些 的 [过程都是一样的:](http://lifehacker.com/a-beginners-guide-to-diying-with-the-raspberry-pi-5976912)

**窗户**

1.  从您想要制作的项目中下载 IMG 文件。
2.  [下载 win32 diski manager](https://launchpad.net/win32-image-writer/+download)并解压应用程序(。exe 文件)中。
3.  使用读卡器将 SD 卡插入 Windows PC。
4.  双击打开您刚刚下载的应用程序 Win32DiskImager.exe。如果你运行的是 Windows 7 或 8，右击它，选择“以管理员身份运行”。
5.  如果应用程序没有自动检测到您的 SD 卡，请单击右上方的下拉菜单(标有“设备”)并从列表中选择它。
6.  在应用程序的图像文件部分，单击小文件夹图标，选择您刚刚下载的 IMG 文件。
7.  单击 Write 按钮，等待 Win32DiskImager 完成它的工作。完成后，您可以安全地弹出您的 SD 卡，并将其插入您的 Raspberry Pi。

**OS X**

1.  从您想要制作的项目中下载 IMG 文件。
2.  [下载 RPi-sd 卡构建器](http://alltheware.wordpress.com/2012/12/11/easiest-way-sd-card-setup) (一定要为你安装的 OS X 版本选择合适的版本)并解压应用程序。
3.  使用读卡器将 SD 卡插入 Mac。
4.  打开 RPi-sd 卡生成器。您将立即被要求选择一个图像。选择您先前下载的 IMG 文件。
5.  系统会询问您是否连接了 SD 卡。因为我们之前插入了它，所以它是，所以继续并单击 Continue。您将看到 SD 卡选项。如果您只插入了一个，您将不会在列表中看到任何其他内容，它将被检查。如果没有，只需检查您想要使用的卡，然后单击确定。
6.  输入您的管理员密码，然后单击确定。
7.  您将被询问 SD 卡是否被弹出。这是应该发生的，因为应用程序需要卸载它，以便它可以执行直接拷贝。仔细检查您的 SD 卡在 Finder 中是否不再可用。*不要*将其从 USB 端口上移除。确定后，点按“继续”。
8.  RPi-sd 卡生成器完成准备您的 sd 卡，安全弹出它并将其插入您的 Raspberry Pi 单元。

RPi-sd card builder 与其说是一个应用程序，不如说是一个行为类似的自动机操作。有些人报告了使用它的问题，所以如果你遇到问题，只需打开终端应用程序(你的硬盘→应用程序→实用程序→终端),并按照 Linux 的指示操作。

### 将您的覆盆子 Pi 变成 AirPlay 扬声器

将一个树莓派变成一个 [AirPlay 扬声器的过程并不太激烈](http://lifehacker.com/turn-a-raspberry-pi-into-an-airplay-receiver-for-stream-5978594) ，但它确实需要在命令行中进行大量调整才能正常工作。这就是为什么 Raspberry Pi 论坛成员 rapsberrye [创建了一个预配置的图像](http://www.raspberrypi.org/forums/viewtopic.php?f=38&t=41504) 这样你就不用做任何工作了。

你需要做的就是 [下载镜像](http://snippets.khromov.se/files/shairport-configured-latest.tar.gz)[放到你的 SD 卡上](http://lifehacker.com/a-beginners-guide-to-diying-with-the-raspberry-pi-5976912) ，然后给你的树莓派加电。你的 Raspberry Pi 将立即显示为 AirPlay 兼容播放器，你甚至可以安装看门狗来重启 AirPlay 软件，以防出现任何问题。

### 制作《我的世界》服务器

令人惊讶的是，Raspberry Pi 是一个很棒的小型《我的世界》服务器，但是自己设置整个系统有点麻烦。你不得不通过挖掘一堆不同的设置和调整不同的选项来让《我的世界》实际上运行顺畅。 [MinecraftPi](http://www.raspberrypi.org/forums/viewtopic.php?f=78&t=75882&hilit=minecraftpi) 修复。

你需要做的就是把 MinecraftPi 安装到 SD 卡上，然后在你的 Raspberry Pi 上启动它。你需要 [让自己成为管理员](http://www.ign.com/wikis/minecraft/Admin_and_Server_Commands) ，但是除此之外，你可以马上在你的本地网络上开始玩《我的世界》。该图像甚至从一开始就被设置为超频，所以你甚至不必乱动这些设置。

### 运行一个私人或公共的 WordPress 网站

正如您所料，将您的 Raspberry Pi 设置为 web 服务器需要付出很多努力。 [PressPi](http://everyday-tech.com/wordpresspi-wordpress-web-server-image-on-raspberry-pi/) 让它变得非常简单，还在图片上安装了一个 WordPress install。

一旦你用 PressPi 镜像启动了你的 Raspberry Pi，你就可以立即登录到 WordPress 的本地版本。如果你想让任何人都可以访问，你需要遵循 PressPi 页面上的指南，将你的路由器向外部流量开放，否则这可能是立即将你的 Pi 变成 web 服务器的最简单方法。

### **制作无线接入点**

Raspberry Pi 可以做一个很棒的小路由器或无线接入点。设置好之后，您可以使用它来扩展您的 Wi-Fi 网络，创建一个单独的接入点，甚至使用它来让客人访问您的 Wi-Fi，而不让他们进入您的整个网络。

手动设置所有这些东西需要很多时间，由 [Pi-Point](http://www.pi-point.co.uk/) 是一个定制的图像，包括你需要的一切。如果你用它来做任何超出简单接入点的事情，你需要 [做一点点配置来让它](http://www.pi-point.co.uk/documentation/) 与你的网络一起工作，但除此之外，它几乎是一键设置。

### **成立复古游戏中心**

我们已经 [谈了很多关于使用](http://lifehacker.com/how-to-turn-your-raspberry-pi-into-a-retro-game-console-498561192) [RetroPie](http://blog.petrockblock.com/retropie/) 把你的树莓派变成复古游戏机，但它确实是最好的现成图像之一。手动安装 [RetroPie 镜像上的所有东西需要花费几个小时](http://emulationstation.org/gettingstarted.html) ，而且在这个过程中很容易出错。

有了 [RetroPie image](http://blog.petrockblock.com/retropie/retropie-downloads/) 你就有了几十个模拟器，SAMBA 共享和 SSH 被自动打开，USB 守护进程被启用用于从 USB 复制 rom，它还打包了大多数流行控制器的驱动程序。你所需要做的就是启动它，复制你的 ROM 收藏，然后你就可以开始了。

### 从您的 Raspberry Pi 中流式播放所有音乐

如果你想把你的树莓派当做一个小小的音乐流媒体设备，你最好的选择是 [MusicBox](http://www.woutervanwijk.nl/pimusicbox/) 。您可以使用您的 Raspberry Pi 从 Spotify、Google Music、SoundCloud、各种广播电台和播客中播放音乐。

最棒的是，除了输入您的登录信息，您不需要做任何事情来设置它。MusicBox 附带遥控接口、MPD 支持、AirPlay 支持、DLNA 流、USB 音频支持，并支持各种声卡。你甚至不需要深入命令行来让它工作。

### **同时运行 Ubuntu Linaro、Raspbian、OpenELEC 和 RISC 操作系统**

在 Raspberry Pi 上设置多重引导系统出奇的困难，但是 Raspberry Pi 论坛成员 Mequa 创造了一个漂亮的杀手多重引导系统，它有几个很棒的操作系统。

Mequa 的“怪物”镜像需要一个 32GB 的 SD 卡和一个 Raspberry Pi 2。你会得到一个包含[Ubuntu Linaro](http://www.linaro.org/)[Raspbian](http://www.raspbian.org/)[open elec](http://openelec.tv/)和 [RISC OS](https://www.riscosopen.org/content/) 的单一映像。一切都是预先配置好的，随时可以使用，所以一旦你有了 SD 卡，你马上就可以使用你选择的操作系统了。