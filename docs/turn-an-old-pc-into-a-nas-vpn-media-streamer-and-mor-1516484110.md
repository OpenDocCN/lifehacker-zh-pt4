# 使用 Amahi 将旧 PC 转变为 NAS、VPN、媒体流等

> 原文:[https://life hacker . com/turn-an-old-PC-into-a-nas-VPN-media-streamer-and-mor-1516484110](https://lifehacker.com/turn-an-old-pc-into-a-nas-vpn-media-streamer-and-mor-1516484110)

如果你有一台还有点寿命的旧电脑，或者你正在构建一台全能的家庭服务器，可以存储你的备份、音乐、电影和其他一切你需要备份和安全的东西， [阿玛希](https://www.amahi.org/) 是完成这项工作的完美工具。Amahi 可以将任何 PC 变成一个家庭 VPN，一个你所有文件的 NAS，等等。以下是方法。

Watch

### 阿玛希是什么？

Amahi 是基于 Fedora Linux 的免费开源家庭服务器软件。它灵活、可定制、易于安装，并且有大量插件、扩展和其他附加软件，可以扩展其功能以满足您的需求。如果你需要将流媒体传输到你的移动设备上，Amahi 可以做到。如果你只是在寻找一个简单的文件服务器，或者想把一堆硬盘合并成一个 NAS，Amahi 也可以做到这一点。如果你想要一个 VPN，可以在你外出时安全地连接到你的家庭网络，Amahi 也能满足你。你可以 [在这里阅读更多关于它的功能，或者](http://www.amahi.org/gallery) [在这里](http://www.amahi.org/tour) 快速浏览一下产品。

我们 [很久以前就提到过 Amahi](https://lifehacker.com/amahi-turns-old-systems-into-full-featured-media-server-5332535)，但是从那以后它成长了很多，甚至比以前更容易安装。启动和运行需要一些时间，虽然一些配置可能很复杂，但一旦开始工作，它就会自动处理，您永远不需要登录到服务器本身，一切都可以从它的仪表板进行管理，您可以从网络上的任何其他计算机登录到它。

我们已经向您展示了旧 PC 的一些其他伟大用途，如使用 [FreeNAS 8 构建家庭 NAS](https://lifehacker.com/turn-an-old-computer-into-a-do-anything-home-server-wit-510023147) 或 [使用 Ubuntu 构建全功能家庭服务器](http://lifehacker.com/turn-an-old-computer-into-a-networked-backup-streaming-5919558) ，Amahi 采取了类似的方法。如果您是一个高级用户，希望设置完美的 NAS，并且需要大量的驱动器配置和访问选项，那么 FreeNAS 是一个不错的选择。如果你想让你的家庭服务器做很多事情，比如充当 VPN、媒体服务器、web 服务器等等，Amahi 是一个更好的选择——不仅仅是因为它更容易安装，还因为它支持做所有这些事情的插件(我们将在后面重点介绍其中一些插件)。)

### 开始工作需要什么

在我们开始之前，您需要一些基础知识:

*   一台 [满足最低系统要求](http://docs.amahi.org/requirements.html) 的计算机。任何具有相对现代组件的系统都应该可以工作。
*   Amahi 安装介质，你可以在 这里 [下载。](https://wiki.amahi.org/index.php/Express_CD)
*   在注册账户即可获得一个 Amahi 安装代码。安装代码是将您的 Amahi 服务器(称为 HDA)链接到 Amahi 自己的集中式 web 服务的关键。它也是生成您的动态主机名的关键(因此，即使您的 ISP 更改了您的家庭 IP 地址，您也可以连接到您的服务器),也是使 Amahi 的一键式插件安装(稍后将详细介绍)工作的功能。

当您注册 Amahi 帐户时，控制面板会询问您家庭网络上 Amahi 服务器的 IP 地址(通常是 192.168.x.x)。这有点奇怪，因为你甚至还没有安装它，但不要担心。选择家庭网络中其他设备没有使用的内容，并写下来。如果你已经知道你想安装 Amahi 的电脑的 IP 地址，使用它。请记住，它与您的安装代码相关联，您不能更改您的安装代码。如果这里有一个错误，你必须改变 IP 地址或安装代码，你可能必须重新安装 Amahi。

在本指南中，我使用的是 Amahi Express 安装程序，它是为全新安装而设计的——它会在安装之前清除你的硬盘。如果您想要保持数据完整或安装在分区上，您可以使用下面的高级安装选项，或者断开包含您想要保留的数据的驱动器，并在 Amahi 启动并运行后将其添加回系统。

### 如何安装 Amahi

安装阿玛希 相当容易。以下是如何做到这一点:

1.  从上面的链接下载 ISO，然后刻录到 DVD 或放到 USB 闪存驱动器上。
2.  [从光盘或闪存盘](http://lifehacker.com/how-to-boot-from-a-usb-drive-or-cd-on-any-computer-5991848) 启动安装。
3.  您将被要求选择您的时区、语言，并检查一些其他系统要求(如果需要，您可以在这里选择一些高级设置选项，但我们将一切都保留为默认值。
4.  点击安装，你就可以开始了。在 Amahi 安装过程中，您可以为系统设置 root 密码，并创建一个在安装完成后有权登录系统的用户。当安装在后台运行时，继续设置这些。
5.  安装完成后，系统会提示您输入 Amahi 安装代码，这会将您的安装绑定到您的 Amahi 网络帐户。该软件将在后台连接到互联网来完成这一操作，一旦通过验证，就会提示您重新启动。
6.  重新启动后，您将看到一个控制台登录屏幕。不要在这里做任何事情。Amahi 将继续在后台配置自己并重新启动。当它回来的时候，你们都完了。

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-F78Lm6zpHKw&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-F78Lm6zpHKw&start=0) 

您可以使用您之前设置的用户名和密码直接登录到控制台，但是您会被带到命令行。取而代之的是，通过打开网络浏览器，进入 [http://hda/](http://hda/) ，从网络上的任何其他计算机访问您的 Amahi 服务器。这将把你带到一个欢迎屏幕，在这里你可以设置你的用户帐户。一旦创建完成，您将到达 Amahi 仪表板。接下来，这是您访问 Amahi 服务器的方式——您只需登录控制台进行故障排除和任何您需要的系统调整。

登录后，您将进入仪表板上的“用户”选项卡。在这里，您可以添加需要登录服务器或访问 HDA 上的任何共享文件或应用程序的任何其他用户。这是 Amahi 团队关于如何设置和管理用户账户的视频指南:

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-i_O6bx5AaXA&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-i_O6bx5AaXA&start=0) 

在我们继续之前，请前往您的 Amahi 控制面板 以确保您的服务器显示在那里。如果一切顺利，并且正确输入了安装代码，您还应该会收到一封祝贺您成功安装的电子邮件。在控制面板中，您可以获得安装代码(如果您还需要的话),并且在这里您可以找到 Amahi 服务器的动态主机名——这是您进行远程访问所需要的。

### 设置您的共享文件夹和驱动器

从这里，您可以登录到仪表板，并开始定制您的 Amahi 安装。如果您安装在单个驱动器上，您不必做任何其他事情。如果您有多个驱动器，您必须向其中添加共享文件夹，或将现有共享移动到这些驱动器。我们一会儿就会谈到这一点。首先，这是 Amahi 团队关于设置共享文件夹的视频:

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-PMi4fGD8nsY&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-PMi4fGD8nsY&start=0) 

默认情况下，Amahi 会创建一堆所有用户都可以访问的共享文件夹(书籍、电影、音乐、图片等等)。以下是找到他们的方法:

1.  单击控制面板顶部的共享选项卡。您应该会看到所有可用共享文件夹的列表，包括 Amahi 为您创建的文件夹。
2.  单击他们中的任何一个，重置他们的权限，完全删除他们，或更改谁有访问权限。默认情况下，所有用户都可以使用所有共享。要指定用户，请取消选中“所有用户”将出现一个用户列表，您可以选择哪些 Amahi 用户对每个文件夹具有读写权限。
3.  要创建新共享，请向下滚动到“创建新共享”给它起个名字，把它设置为可见，然后等待它被创建。完成后，重复上述过程以指定哪些用户可以访问它，或者将其设置为“所有用户”以使每个人都可以访问它。
4.  要获得更精细的控制，请单击仪表板页面顶部的设置选项卡，并启用“高级设置”然后，返回到“共享”选项卡。您将看到新的选项来指定共享文件夹位于哪个驱动器上以及每个共享的标签。

如果你遇到了麻烦，Amahi 网站 上有一些 [有用的视频教程，可以帮助你完成添加用户和管理共享的过程。](https://www.amahi.org/videos)

如果你稍微高级一点，并且在你的服务器中有多个硬盘驱动器，你可能想要设置 [磁盘“池化”](https://wiki.amahi.org/index.php/Storage_pooling) ，这样它们看起来就像一个大卷。在 Amahi wiki 上有关于如何做这个 [的详细说明，而](https://wiki.amahi.org/index.php/Adding_drives_to_your_HDA) [How-To Geek 在这里也有一篇关于这个过程](http://www.howtogeek.com/69192/learn-how-to-upgrade-and-manage-your-amahi-server-storage/) 的精彩文章。不过这肯定是为高级用户准备的，所以我们不会在本指南中深入讨论。

### 你可以用你的新 Amahi 服务器做三件很酷的事情

一旦你建立了文件和文件夹共享，世界就是你的了。我们将向您展示如何将您的 Amahi 服务器转变为媒体流，这是一个 VPN 服务器，当您离开家时，您可以连接到它进行安全浏览，或者在您的手机或平板电脑上访问您的文件。这一切都从几十个 [Amahi 应用](https://www.amahi.org/apps) 开始，你可以直接从仪表盘上下载并安装。

#### 设置个人 VPN

运行你自己的 Amahi 服务器的一个好处是，你可以把它设置成你自己的个人 VPN。不像 [一些 VPN](https://lifehacker.com/why-you-should-be-using-a-vpn-and-how-to-choose-one-5940565)通过另一个国家路由你的流量，以隐藏你的位置或让你访问位置受限的内容，这个 VPN 会在你离开时将你的流量路由回你的家庭网络。它不会让你绕过定位块，但它会让你在公共 Wi-Fi 上安全，并让你无论在哪里都可以在家里访问你的文件。你可以在咖啡店或酒店无线网络上工作，而不用担心有人会偷听你的连接或窃取你的数据。此外，您将始终连接到您的家庭网络，这意味着您可以使用 Amahi 服务器或其他家庭计算机上的所有数据。

Amahi 开箱支持三种 VPN 选项: [**OpenVPN**](https://www.amahi.org/apps/openvpn) ， [**思科的 IPSec VPN**](https://www.amahi.org/apps/ipsec-vpn) ，以及[**OpenVPN ALS**](https://www.amahi.org/apps/openvpn-als)。由于这些应用程序是付费的(分别为 5 美元、5 美元和 4 美元)，你必须在购买之前 [用 Amahi Credit](https://www.amahi.org/credit) 给你的账户充值。一旦你的帐户上有了一些点数，只需点击绿色按钮就可以直接安装到你的 Amahi 服务器上。我们应该注意的是，你不需要使用付费安装程序，他们只是让事情变得超级简单。你总是可以下载软件包并自己安装在 Amahi 服务器上，但是一键安装就没那么麻烦了。

这种情况下，我们建议 [OpenVPN](http://openvpn.net/) 。你将不会被限制到一个 VPN 客户端来连接到你的 Amahi 服务器，因为你可以使用任何支持 OpenVPN 的 iOS、Android、Windows、OS X 或 Linux 应用程序来连接。你所需要的只是你的服务器的主机名(可以在你的 Amahi 控制面板中找到)，即使你的家庭 IP 地址改变了，它也会继续工作。如果你选择使用官方的 OpenVPN 客户端连接，你可以 [使用他们的文档](http://openvpn.net/index.php/access-server/docs/admin-guides-sp-859543150/howto-connect-client-configuration.html) 来设置一切。

#### 随处流式播放您的媒体

Amahi 目录中有几个应用程序可以帮助您与世界或您自己的设备共享音乐、电影和照片。例如，Amahi 完全支持 [**Gallery2**](http://galleryproject.org/) ，这是我们 [最喜欢的在线发布和分享自己照片的方式之一](https://lifehacker.com/how-can-i-take-control-and-host-my-own-photos-online-1461903693) 。它没有一键安装程序，所以你必须自己动手，但设置起来并不困难(有 [文档帮助](http://codex.galleryproject.org/Main_Page) )。完成后，您可以使用 Gallery 移动应用程序在智能手机或平板电脑上查看您的照片库，或者只是在网上访问它们。

如果音乐和电影更符合你的风格，4 美元就能让你一键安装[**亚音速**](http://www.subsonic.org/pages/index.jsp) ，我们 [最喜欢的媒体服务器之一](https://lifehacker.com/five-best-desktop-media-servers-5975362) 。安装后，您可以从仪表板访问它，添加媒体和设置用户，选择通过互联网或仅在本地家庭网络上流式传输您的媒体，并使整个事情都可以通过 web 访问，这样您就不必登录仪表板。

最后， [$5 让你一键安装**阿玛希 DLNA 服务器**](https://www.amahi.org/apps/dlna) ，它将你的阿玛希 HDA 变成一个家庭流媒体发电站，你网络上的任何联网电视、蓝光播放器、Xbox、PlayStation 或 A/V 接收器都可以与之通话。

#### 推出您自己的云存储

如果你不喜欢 Amahi 的界面，或者你只是想要一种更简单的方式来共享、同步和管理我们之前设置的所有文件，你会很高兴听到 [Amahi 支持 **OwnCloud**](https://www.amahi.org/apps/owncloud) 。设置过程是 [很像我们自己的云设置指南](https://lifehacker.com/how-to-set-up-your-own-private-cloud-storage-service-in-5993596) 。这次没有一键安装，但一旦你有了自己的云并运行，你就可以在你的桌面和移动设备上安装客户端，配置它们与你的 Amahi 服务器同步，再也不用为别人的云服务支付费用或担心空间限制了。

此外，安装后，你可以利用 OwnCloud 自己的仪表盘和界面与其他人共享文件，同步你的日历和联系人，将其用作流媒体音乐服务器，或使用 OwnCloud 自己的 [插件和扩展](http://apps.owncloud.com/) 数据库进行扩展。

#### 额外收获:从任何地方访问 Amahi 服务器上的所有内容

如果你想要的只是在旅途中访问你的 Amahi HDA 及其所有文件和文件夹，[Amahi iPhone 和 iPad 应用](https://itunes.apple.com/us/app/amahi/id761559919?ls=1&mt=8) 将为你提供这一切，而且是免费的。目前还没有 Android 应用，尽管根据 Amahi 团队 12 月份的推文T5，他们现在正在进行 beta 测试。尽管如此，由于 Amahi 的大多数功能都可以通过仪表盘使用，你甚至不需要特定的移动应用程序来访问你的文件和文件夹。只要您将动态主机名加入书签，您就可以随时登录。登录后，点按屏幕顶部的“HDA”按钮，或者使用搜索栏来查找您想要的内容。您将看到您所有的共享文件、文件夹和媒体，并且可以将其下载或流式传输到您的移动设备。

我们实际上只是触及了表面。Amahi 还支持 iCal 或 Outlook 日历共享、基于浏览器的文件搜索等等。Amahi 的美妙之处在于它很容易安装和运行，你可以按照你想要的方式调整它，而不用安装一大堆你不需要的软件。虽然它也有缺点，但如果你正在考虑构建一个全能的家庭服务器，它还是值得一看的。这就像建立一个家庭服务器一样简单。

*<small>标题图像制作使用</small>* [*<small>尾音</small>*](http://www.shutterstock.com/pic.mhtml?id=101651263&src=id)*<small>(Shutterstock)。</small>T15】*