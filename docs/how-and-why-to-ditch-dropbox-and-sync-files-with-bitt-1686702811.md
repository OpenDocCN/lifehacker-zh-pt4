# 如何(以及为什么)放弃 Dropbox 并使用 BitTorrent Sync 同步文件

> 原文：<https://lifehacker.com/how-and-why-to-ditch-dropbox-and-sync-files-with-bitt-1686702811>

Dropbox(以及类似的云服务)很棒，但是它们不能给你太多的控制权、安全性或文件隐私。如果你想把控制权掌握在自己手中，同时又不失去云同步服务的特性， [BitTorrent Sync](http://www.getsync.com/) 就是为你准备的服务。以下是使用方法。

Watch

### 为什么在 Dropbox 上使用 BitTorrent 同步

我们喜欢 Dropbox(和其他文件同步服务),但是如果你需要超过几 g 的空间，它们会很贵。将文件存储在第三方服务器上也存在固有的安全缺陷，尽管大多数云存储服务都提供双重认证，但这些服务器总有可能在某个时候遭到黑客攻击。相反，像 [OwnCloud 这样的私有云服务很棒](http://lifehacker.com/how-to-set-up-your-own-private-cloud-storage-service-in-5993596) ，但是你需要自己的服务器来使用它们。

BitTorrent Sync 解决了这两个问题。您的文件从不存储在服务器上。它们只在你的电脑上，数据通过点对点文件共享在它们之间传输。BitTorrent Sync 也是完全免费的，您可以传输任何大小的文件，这对于文件大小较大的项目(如视频)来说非常棒。存储容量只限于你自己的硬盘，而不是你支付多少空间。让我们快速了解一下 BitTorrent Sync 与其他文件同步服务相比的优缺点。

#### BitTorrent 同步相对于 Dropbox 的优势

*   自由的
*   存储空间仅受硬盘空间的限制
*   您的文件永远不会上传到第三方服务器
*   快速传输速度，仅受设备的互联网连接速度限制
*   服务器停机不会影响您，因为您的文件不会上传到另一台服务器
*   从硬盘上的任何位置同步您想要的任何文件夹或文件
*   你可以把它安装在你自己的 NAS 上，这样它的工作方式几乎和 Dropbox 一样

#### 通过 Dropbox 同步 BitTorrent 的缺点

*   至少有一台电脑需要打开以执行同步
*   与您共享文件夹和文件的人需要安装 BitTorrent Sync，没有 web 应用程序可以访问您的文件
*   你必须共享文件夹，不能共享单个文件( [一个 Pro tier](http://blog.bittorrent.com/2014/11/19/what-to-expect-next-from-sync/) 预计会提供这个功能)
*   不像其他服务一样具有 [协作和内置文件编辑功能](http://lifehacker.com/dropbox-adds-collaborative-editing-for-microsoft-office-1561414150)
*   不如云备份有效，因为它只能在计算机之间同步

对于我们大多数人来说，如果你的主要用途是备份，BitTorrent Sync 不是 Dropbox 的好替代品，但对于共享和同步文件来说，它很棒。也就是说，在 NAS 上运行 BitTorrent Sync 使它的工作方式类似于 Dropbox 和 OwnCloud，但速度更快，而且不用担心软件开销。你不需要设置服务器，所以 BitTorrent Sync 也非常安全，因为你是唯一拥有访问你的文件的密钥的人。

### 如何设置 BitTorrent 同步

为了使用 BitTorrent 同步，您需要设置一些不同的东西。在本指南中，我们将使用最新的测试版 [BitTorrent Sync，2.0](http://forum.bittorrent.com/forum/123-sync-20-community-testing-download-here/) ，应该很快就会正式推出。也就是说，旧版本的程序也是一样的。

1.  [下载](http://www.getsync.com/) 为您的操作系统同步 BitTorrent
2.  打开应用程序
3.  选择您要在电脑间同步的文件夹。单击“+”按钮并选择您的文件夹。这些文件夹现在可以共享了
4.  单击齿轮图标并选择“链接设备”
5.  点击“手动链接桌面设备”，你会得到一个 35 位数的代码
6.  转到另一台计算机，重复步骤 1 和 2。
7.  在第二台计算机上，单击齿轮图标>链接设备>手动链接设备>回车键，并输入步骤 5 中的 35 位数字代码

现在，您选择共享的每个文件夹都会在两台电脑之间同步。你可以在你拥有的每台电脑上重复这个过程。您也可以在移动设备上设置同步。过程非常相似:

1.  下载 [安卓](https://play.google.com/store/apps/details?id=com.bittorrent.sync&referrer=utm_source%3Dbittorrent%26utm_medium%3Ddownloads%26utm_campaign%3Dhome)[iOS](https://itunes.apple.com/us/app/bittorrent-sync/id665156116?mt=8&utm_source=web&utm_medium=dlpop&utm_campaign=iOS)，或者 [Windows Phone](http://www.windowsphone.com/s?appid=61b549d6-0d88-4db3-b336-670473e4b7ef) 的手机 app
2.  在您的桌面上，单击齿轮图标>链接设备以获取二维码
3.  回到您的移动设备，点击“添加文件夹”,用您的手机扫描电脑上的二维码

有一点需要注意:目前，移动应用程序没有设置为与 BitTorrent Sync 2.0 一起工作，所以现在，如果你需要在移动设备上访问，你需要使用 [版本 1.4](http://www.getsync.com/download) 。

这就是设置标准同步。从现在开始，您的文件将在安装了 BitTorrent Sync 的所有计算机和设备之间同步，只要这些设备中至少有一台处于联机状态。

### 如何将文件夹发送给其他人

不过，设备之间的同步只是使用 BitTorrent Sync 的一部分。最有用的功能是与其他人共享文件夹。这里没有文件大小的限制，所以你可以分享任何你想要的东西。它是这样工作的:

1.  突出显示您想要共享的文件夹，然后单击“共享”按钮
2.  选择您要授予收件人的权限(只读或读写)
3.  选择您要授予的安全级别(“我邀请的对等用户必须在此设备上获得批准”使他们在使用链接之前必须获得批准，“链接将在 x 天后过期”授予在一定天数内的访问权限，“链接可以使用 x 次”设置链接可以获得的点击量的限制)
4.  选择共享链接的方式(通过电子邮件、将其复制到剪贴板或生成二维码)

就是这样。将该链接发送给你想要的任何人，他们将能够从他们的 BitTorrent Sync 版本访问该文件夹。您也可以使用此方法仅与其他电脑共享选定的文件夹，如果您的笔记本电脑没有太多硬盘空间，这将非常方便。

### 附加功能:设置版本控制和自动相机卷备份

除了 BitTorrent Sync 自带的正常同步和共享功能，它还有一些我们在文件同步服务中常见的功能:版本控制和自动相机胶卷备份。这两者都很容易建立，但是也很容易忽略这样一个事实，那就是这两者一开始就存在。

#### 签出文件的早期版本

像 Dropbox 一样，BitTorrent Sync 会保存 30 天内您对文件所做的每次更改的快照。当你把事情搞砸了，需要回滚到一个更早的版本时，这是很方便的。以下是访问这些文件的方法:

1.  在您想要查看旧版本的文件夹上，点按“共享”按钮旁边的三点图标
2.  选择“打开归档”在文件资源管理器或 Finder 中打开文件夹
3.  这里的文件是隐藏的，所以你需要为你的操作系统启用隐藏项([Windows](http://lifehacker.com/navigate-files-like-a-pro-with-these-windows-explorer-t-1466669311)//[Mac](http://lifehacker.com/show-hidden-files-in-finder-188892))
4.  您会看到一个名为。SyncArchive，在里面你会看到一个旧版本文件的集合(如果你在处理大量的大文件，这会占用很多空间)

就是这样。如果你需要，BitTorrent Sync 还有一个向导用于更改版本控制的默认行为，这样你就可以根据自己的需要进行定制。

#### 在移动设备上打开相机胶卷备份

像大多数文件同步服务一样，BitTorrent Sync 也为其移动应用程序提供了自动相机胶卷上传选项。一旦启用，相机胶卷上的所有内容都会备份到您的电脑上。这里的过程非常简单。

1.  在移动应用程序中，轻按“相机胶卷备份”
2.  您可以选择复制或通过电子邮件发送链接。如果您点按“电子邮件”,请通过电子邮件将其发送给自己，这样您就可以在家用电脑上访问它
3.  前往安装了 BitTorrent Sync 的计算机
4.  点按该链接并选择一个文件夹来同步您的照片。这将您的相机胶卷照片添加到 BitTorrent 同步

现在，你手机上的所有照片都会自动发送到任何运行 BitTorrent Sync 的计算机上。

BitTorrent Sync 可能不是 Dropbox 的完美替代品，但如果你不需要云存储，它几乎可以做 Dropbox 可以做的任何事情。如果你厌倦了花一大笔钱，或者你只是在寻找一点额外的隐私，这种方法非常有效。

<small>*图像由*</small> [*<small>蒂娜·梅洛-罗伯格</small>*](http://vervex.ca/)