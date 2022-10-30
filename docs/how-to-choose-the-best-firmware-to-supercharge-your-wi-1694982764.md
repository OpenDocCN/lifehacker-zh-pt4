# 如何选择最好的固件来为你的 Wi-Fi 路由器充电

> 原文：<https://lifehacker.com/how-to-choose-the-best-firmware-to-supercharge-your-wi-1694982764>

在 Wi-Fi 路由器上安装定制固件就像是家庭网络的上帝模式。你可以看到正在发生的一切，增强你的 Wi-Fi 信号，加强你的安全性，甚至可以做一些高级的事情，比如安装你自己的 VPN。然而，有这么多的选择，很难选择正确的。以下是你需要知道的。

Watch

### 何必呢？

安装你自己的定制固件不仅仅是阿尔法极客们寻找酷事做的下午项目——它实际上让你的路由器变得更好。选择正确的一个，你可以实时监控你的网络，确保你的室友不会通过下载音乐来减缓你的网飞狂欢(但要确保你的音乐下载又好又快)，使你的网络对客人友好但对入侵者不友好，等等。开放式固件可以让你更好地控制 Wi-Fi 性能，大多数甚至可以让你提高 Wi-Fi 信号，这样房子的某个角落就不会再是盲区了。你还可以得到额外的好处，比如可以在家里运行自己的 VPN(你绝对应该试试)，并且比制造商更新他们的库存软件更频繁地更新以修复安全问题，这两者对安全性都非常重要。

当然，这可能需要一点工作，但如果你能胜任这项任务，你将获得一个更快、更安全的家庭网络，一个你在任何时候都能完全控制的网络。如果你的速度下降，你会知道确切的原因。你将能够记录和监控你的连接，以确保你的服务提供商(如康卡斯特或威瑞森)没有因为你敢看网飞或启动 Spotify 而限制你。

### 三巨头:DD-WRT、OpenWRT 和番茄

一些最受欢迎的开放式路由器固件是你可能已经听说过的名字，像[DD-WRT](http://www.dd-wrt.com/site/index)[OpenWRT](https://openwrt.org/)和 [番茄](http://www.polarcloud.com/tomato) 。在 之前，我们已经 [向您展示了如何在您的路由器上安装 DD-WRT，并且向您展示了](https://lifehacker.com/how-to-supercharge-your-router-with-dd-wrt-508138224) [如何用番茄](http://lifehacker.com/turn-your-60-router-into-a-user-friendly-super-router-344765) 为路由器增压，但是这里快速回顾一下它们之间的区别:

*   [**OpenWRT**](https://openwrt.org/) 是很多其他人诞生的固件。它是完全开源和可定制的，基于 Linux 内核，支持包管理，有大量额外的附加组件和实用程序。它不是最容易使用和安装的，但它支持最广泛的硬件基础，从功能强大的高端家用路由器到袖珍旅行路由器，甚至企业硬件。它提供了任何开放固件的大部分功能，但它通常很难配置。例如，OpenWRT 几乎支持你可以放在网络上的任何 Linux 设备(如打印机、网络摄像头等)，具有丰富的界面、实时网络监控、内置动态 DNS(这样你就可以 [从远处访问你的家庭计算机](http://lifehacker.com/know-your-network-lesson-4-access-your-home-computers-5831841) )、内置 VPN 的 IP 隧道、内置服务质量(QoS)让你可以将一些事情(如流媒体或 VoIP 呼叫)优先于其他事情(如 torrents 或其他下载您可以在这里 查看 [支持的设备。](http://wiki.openwrt.org/toh/start)
*   [**DD-WRT**](http://en.wikipedia.org/wiki/DD-WRT) 基于 OpenWRT。DD-WRT 承载了 OpenWRT 的许多功能，如实时监控、访问控制、QoS 和建立自己的 VPN 的能力，所有这些都打包在一个更加用户友好的界面后面。你还可以获得像 [网络唤醒](http://lifehacker.com/rule-your-computer-from-afar-by-setting-up-wake-on-lan-5786791) 这样的额外功能，这样你就可以让你的家庭网络上的电脑进入睡眠状态，但当你需要从国外连接电脑时，你可以唤醒它们。它比 OpenWRT 更容易安装，也更容易管理。它支持的设备不像 OpenWRT 那么多，但它支持一些最常见的家用路由器。您可以在这里 [搜索您的路由器是否受支持](http://www.dd-wrt.com/site/support/router-database) 。
*   [**番茄固件**](http://www.polarcloud.com/tomato) 最值得注意的是它的超级轻量级，它的用户界面是直观的，它甚至比 DD-WRT 更容易安装和使用。它最大的优势是它的实时带宽和连接监控，这意味着您可以在发生时看到您网络上发生的一切*，这对于排除连接问题或确保没有人在您的网络上爬行非常有用。它也很精简，不像这里的其他固件，它的设计让你不必在每次小小的改变后重启路由器。同样，它比这里的许多其他设备更容易增强你的无线信号强度。即使是防火墙配置和访问控制等高级功能也很容易实现，即使是新用户也不例外。Tomato 唯一的缺点是支持的设备相对较少。如果您的路由器支持这里的 ，您可以看到 [。](http://www.polarcloud.com/tomatofaq#what_will_this_run_on)*

*对于大多数人来说，这三个中的一个将支持你所拥有的设备，并提供你可能需要的所有功能。在这三者中，DD-WRT 是家庭路由器上支持得最好的，而且相对容易安装和设置。番茄是最用户友好的，当然也是三者中最有吸引力的，但是它支持的设备最少。OpenWRT 通常支持大多数设备，包括只有网络工程师才会使用的东西，但是它的学习曲线可能很陡。它也是最容易修改和调整的，如果你的硬件不被其他任何东西支持，这是一个很好的选择。即便如此，他们也不是你唯一的选择。*

### *调整者和黑客的其他选择:路由器专用或开发友好的固件*

*虽然这三个可能是最著名和最受欢迎的，还有很多其他的选择。以下是你所有选择的概要:*

*   *[**石像鬼**](http://www.gargoyle-router.com/) 也是基于 OpenWRT，专门为基于 Broadcom 和 Atheros 的路由器硬件设计的轻量级。它很小，易于安装，有一个漂亮的网络管理页面，并支持许多旅行和便携式路由器。它最显著的特点是能够将带宽限制在特定的 IP 地址，或者让你对带宽的使用情况有独特的见解。石像鬼是拥有旅行路由器的人的理想选择，或者如果你是那种不太关心安全和 Wi-Fi 信号，而更关心家里每个人如何使用你的带宽的人。它非常适合有带宽限制的人。你可以在这里查看 [支持的路由器](http://www.gargoyle-router.com/wiki/doku.php?id=supported_routers_-_tested_routers) ，或者从他们的网站购买一个预装石像鬼的开放式硬件路由器。*
*   *[**librevrt**](http://librewrt.org/index.php?title=Main_Page)是一个完全自由开放的固件，它遵循了 [自由软件基金会](http://www.fsf.org/) 的 [自由系统发布指南](http://en.wikipedia.org/wiki/GNU_Project#GNU_Free_System_Distribution_Guidelines) 。如果你想知道像理查德·斯托尔曼或莱纳斯·托沃兹这样以开源为生的人会选择什么样的路由器固件，这可能就是了。LibreWRT 还被设计成一个轻量级的选项，供有抱负的开发人员参与其中并做出贡献。它也是基于 OpenWRT 的，但是它 [只支持少数设备](http://librewrt.org/index.php?title=Hardware_Support) (虽然你当然可以 [自己构建](http://librewrt.org/index.php?title=How_To_Build_LibreWRT) ，虽然这不是一个面向初学者的项目。)*
*   *[**DebWRT**](http://debwrt.net/) 是另一个有很多衍生产品的保护伞固件。基于 Debian 的 Linux 系统——如 Ubuntu 或 Linux Mint——的用户会喜欢它，因为它本质上是 Debian，建立在 OpenWRT 之上，并设计为在家用路由器上运行。它包含了您需要的所有基本功能，但它本身并不是功能最丰富的。你需要添加包和额外的工具来充分利用它，它的命令行界面并不完全是初学者友好的(尽管，如果你已经熟悉 Debian，它会像你的家一样。)它还提供了你在标准 Debian 安装中所能得到的一切，以及它的软件包管理器和任何兼容的实用程序。不过，它可能不适合心脏虚弱的人。*

*这些只是三大玩家最大的衍生品。它们很棒，但如果你喜欢 OpenWRT 的外观，但需要一些特定的东西， [可以看看它的其他衍生物](http://en.wikipedia.org/wiki/OpenWrt#Derivatives) 。例如，石像鬼旨在为 OpenWRT 提供一个友好、可用的 web 界面，使得定制和设置它变得更加简单。其中许多还支持第三方插件功能，如家庭 VPN、网状网络以 [将您的网络与您朋友的家庭网络](https://lifehacker.com/build-your-own-vpn-to-pimp-out-your-gaming-streaming-5900969) 连接，或者您可能想到的任何其他更复杂的设置。如果您愿意动手，并且有一些编码经验，您可以重新构建其中的任何一个来进行自己的调整，或者添加自己的包。*

### *从硬件支持的内容开始，按功能浏览*

*如果你试图在这些固件选项中做出选择，首先要考虑的是你的路由器，以及支持它的开放固件。如果你曾经安装过你自己的固件，你应该已经知道了。几率是你的——即使是 [如果是更新的 802.11ac 型号](https://lifehacker.com/five-best-home-wi-fi-routers-5920709) 支持这些选项中的一个，你只需要找出哪个。*

*如果您只找到一个支持您的路由器的选项，那么这个决定就是为您做出的。如果你找到几个，根据你的需要选择，但不要忘记看看固件支持的程度。有没有可以遵循的指南或文档，或者可以获得帮助的论坛？你想要最好的选择，但是如果你有麻烦，你也不想被冷落。“一旦你选择了你的固件，只需按照他们提供的安装说明进行操作——但要了解更多信息，请查看我们关于安装 DD-WRT 和 [番茄这里](http://lifehacker.com/turn-your-60-router-into-a-user-friendly-super-router-344765) 的指南。*

### *去哪里寻求帮助*

*最后，如果你仍然停滞不前，或者你不知道一个特定的固件是否会做你想要它做的事情，做一些挖掘。正如我们提到的，这些项目中的许多都有论坛，供用户讨论项目和解决彼此的问题。除此之外，在你自己安装之前，谷歌一下你的路由器型号和你正在看的固件，看看它是否兼容，或者是否有人在抱怨它。毕竟，一旦它被安装和设置好，它将是你进入互联网的门户，所以在你完成工作后，不是开始做研究的时候。*

*如果您找不到支持您的路由器的开放固件，或者您想要的固件与您现有的路由器不兼容，您可以选择购买专门用于您想要运行的固件的路由器。查看您想要运行的固件的兼容性列表，并从列表中选择您最喜欢的路由器型号。这样你就知道你会得到一个没有问题的路由器。或者，你可以买一个预装固件的路由器。例如，Buffalo 销售预装了 DD-WRT 的路由器，一些 VPN 提供商甚至销售安装了开放固件的路由器*和*他们的 VPN 设置就绪。 [TorGuard](http://torguard.net/store/) 和 [SlickVPN](http://www.slickvpn.com/routers.html) 都是这么做的。在购买之前，请确保您在路由器 中获得了与您相关的功能以及您想要的固件。*

*<small>*标题图片使用*</small>[<small>*kentoh*</small>](http://www.shutterstock.com/pic.mhtml?id=230742631&src=id)<small>*(Shutterstock)*</small>[<small>*vik torus*</small>](http://www.shutterstock.com/pic.mhtml?id=168653069&src=id)<small>*(Shutterstock)，以及*</small>[<small>*ridjam*</small>](http://www.shutterstock.com/pic.mhtml?id=200530865&src=id)附加图片由 [<small>*音频库*</small>](https://www.flickr.com/photos/audioreservoir/14764070934)<small></small>*[*Arkadiusz Sikorski*](https://www.flickr.com/photos/arakus/8114432077)*[<small>*Kevin Jarrett*</small>](https://www.flickr.com/photos/kjarrett/8303707166)<small>T83】</small>***

**[Open *kinja-labs.com*](http://kinja-labs.com/related-widget/?posts=915783308,1646574925,5833254&title=Recommended%20stories)**