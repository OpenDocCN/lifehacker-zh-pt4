# 如何将一个树莓派变成一个私人流媒体音乐服务

> 原文：<https://lifehacker.com/how-to-turn-a-raspberry-pi-into-a-private-streaming-mus-1583221462>

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-2aca18JURvg&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-2aca18JURvg&start=0) 

如果你厌倦了在智能手机上携带大量的音乐库，又不想为谷歌音乐这样的服务付费，树莓 Pi 可以充当音乐服务器。只要做一点工作，无论你在哪里，你都可以使用你所有的 MP3。下面是如何设置它。

Watch

*我们假设你对树莓派有一个基本的了解，但如果没有，* [*你可以从这里开始*](https://lifehacker.com/a-beginners-guide-to-diying-with-the-raspberry-pi-5976912) *让一切井然有序。*

### 你需要什么

*   **树莓派**:如果你不确定在哪里可以买到，那么 [看看我们对树莓派](https://lifehacker.com/a-beginners-guide-to-diying-with-the-raspberry-pi-5976912) 的介绍吧。
*   4GB SD 卡:你需要一些东西来安装操作系统。 [本页面](http://elinux.org/RPi_SD_cards) 告诉你哪些 SD 卡兼容 Pi。
*   **以太网电缆或 Wi-Fi 适配器**:你需要互联网来设置和运行你的音乐流媒体服务。
*   USB 键盘:你只需要它来进行初始设置。
*   **iOS 或 Android 设备，或电脑传输到**:这项服务的目的是将你的音乐从你的 Raspberry Pi 发送到你的远程设备，所以你需要一些远程设备。
*   **每月 1 美元订阅** [**亚音速高级版**](http://www.subsonic.org/pages/premium.jsp) :在测试了一系列在树莓 Pi 上设置音乐服务器的免费选项后，亚音速胜出，因为它最容易使用，支持最好。虽然通过互联网播放音乐需要每月付费，但亚音速公司可以免费使用 30 天。
*   存储音乐的地方:你的 Raspberry Pi 会把你的音乐传到外面，但是你仍然需要把这些 MP3 文件存放在某个地方。这个 [可能是 NAS](http://lifehacker.com/turn-an-old-pc-into-a-nas-vpn-media-streamer-and-mor-1516484110) 或者 [外置硬盘](http://lifehacker.com/five-best-external-hard-drives-1490604801) 。

### 你会得到什么

当你完成后，你可以从任何有互联网连接的地方访问你的整个音乐库，所有这些都是通过你家里的一个小盒子连接到你的路由器上。为此，我们将在树莓派上安装 [亚音速](http://www.subsonic.org/pages/index.jsp) 。然后，您可以通过智能手机或电脑上的应用程序访问您的音乐库。您还可以与朋友共享该媒体库，一起创建播放列表，等等。本质上，它将是你自己的类似 Spotify 的私人小服务(或者更准确地说，是谷歌音乐)。

亚音速可以在任何电脑上运行，但在 Raspberry Pi 上尤其方便，因为你不需要担心一直运行电脑的成本，也不需要担心将主电脑暴露在互联网上。有了树莓派，你可以把它放在某个角落里，让它 24/7 全天候工作，而不用太担心它。

### 第一步:设置 Raspbian

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-aTQjuDfEGWc&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-aTQjuDfEGWc&start=0) 

为了将您的 Raspberry Pi 用作私人流媒体音乐服务，您需要在 SD 卡上安装 Raspbian 操作系统。我们的 [向导在这里](https://lifehacker.com/a-beginners-guide-to-diying-with-the-raspberry-pi-5976912) 告诉你到底该怎么做。一旦解决了这个问题，您可以引导到命令行，我们将运行一个更新。在控制台中键入以下内容:

```
sudo apt-get update  sudo apt-get upgrade
```

坐下来等待更新运行。可能需要一点时间来抓取所有内容。

### 第二步:更新 Java

我们将要用来从 Raspberry Pi 中播放音乐的软件在安装了最新版本的 Java 后效果明显更好。所以，我们准备 [手动安装 OpenJFX】。要做到这一点，请从您的家用计算机进入](https://wiki.openjdk.java.net/display/OpenJFX/OpenJFX+on+the+Raspberry+Pi) [Java 下载页面](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-arm-downloads-2187472.html) ，单击“接受许可协议”按钮，右键单击“下载”下面的链接，然后选择“复制链接地址”回到 Raspberry Pi，在控制台中键入以下内容:

```
wget [link you just copied]
```

它应该看起来像这样

```
wget http://download.oracle.com/otn-pub/java/jdk/8-b132/jdk-8-linux-arm-vfp-hflt.tar.gz
```

下载完成后，为安装创建一个目录:

```
mkdir -p /opt
```

然后打开包装:

```
sudo tar zxvf [file you downloaded] -C /opt
```

例如，应改为:

```
sudo tar zxvf jdk-8-linux-arm-vfp-hflt.tar.gz -C /opt
```

现在我们需要将新的 Java 安装设置为默认安装:

```
sudo update-alternatives —install "/usr/bin/java" "java" "/opt/jdk1.8.0/bin/java" 1
```

然后

```
sudo update-alternatives —set java /opt/jdk1.8.0/bin/java
```

测试以确保安装了正确版本的 Java:

```
java -version
```

最后，包括亚音速在内的一些程序需要知道在哪里可以找到这个新版本的 Java。所以，我们需要编辑一些文本文件。在终端中键入以下内容:

```
sudo nano /etc/environment
```

并将该行添加到文本文件中:

```
JAVA_HOME="/opt/java/jdk1.8.0
```

保存文件并返回命令行。我们将对 bash 控制台做同样的事情:

```
sudo nano ~/.bashrc
```

添加以下行:

```
export JAVA_HOME="/opt/jdk1.8.0"
```

```
export PATH=$PATH:$JAVA_HOME/bin
```

保存文件，然后一切都准备好了。重启 Pi，我们将准备好音乐服务器。

### 第三步:安装亚音速

现在是时候安装亚音速软件了，这款软件实际上将为音乐流提供动力。我们需要像获取 Java 链接一样获取下载链接。从你的家用电脑进入 [亚音速下载页面](http://www.subsonic.org/pages/download.jsp) ，点击 Debian 安装程序链接，右键点击“直接链接”并选择“复制链接地址”现在，在树莓界面上，输入:

```
wget [the URL you copied above] -O subsonic.deb
```

例如:

```
wget http://downloads.sourceforge.net/project/subsonic/subsonic/4.9/subsonic-4.9.deb
```

下载完成后，输入以下内容进行安装:

```
sudo dpkg -i subsonic.deb
```

现在亚音速已经安装好了，但是因为我们要向互联网开放 Pi，我们需要采取一些安全措施。这意味着 [创建一个没有 root 权限的新用户](http://www.subsonic.org/pages/installation.jsp#debian) 。所以，输入:

```
sudo adduser [new user name]
```

例如:

```
sudo adduser subsonic
```

现在我们将编辑亚音速的配置与这个新的信息。键入:

```
sudo nano /etc/default/subsonic
```

接下来，将下面一行添加到文本文件的末尾:

```
SUBSONIC_USER=[new username]
```

然后，重新启动亚音速:

```
sudo service subsonic restart
```

亚音速现在以您刚刚创建的用户身份运行在 Raspberry Pi 上，因此它没有 root 访问权限。当您将来启动 Pi 时，它也会自动设置为运行。

### 第四步:设置静态 IP 地址

现在，我们需要给 Raspberry Pi 一个静态 IP 地址，这样您就可以通过在浏览器中键入相同的 URL 来访问它。首先，我们需要了解一下您家庭网络的情况。键入:

```
ifconfig
```

这将显示您当前连接到路由器的位置和方式。注意“inet addr”号，它看起来应该类似于`192.168.1.115`。写下那个数字。现在我们需要得到默认的网关号。键入:

```
route -n
```

默认网关列在“UG”标志行上。一般是你路由器的地址，比如:`192.168.1.1`。记下这一点。接下来，编辑配置文件:

```
sudo nano /etc/network/interfaces
```

在这里，您会看到一行类似这样的内容:iface eth0 inet dhcp。替换为:

```
iface eth0 inet static
```

```
address [the IP address you wrote down above]
```

```
netmask 255.255.255.0
```

```
gateway [the gateway you wrote down above]
```

就是这样。现在你的 Raspberry Pi 每次都有相同的 IP 地址，所以很容易连接。如果你需要更多的信息，你可以在这里找到设置静态 IP 地址或设置 [的完整指南，更好、更容易地使用 DHCP 预订](https://lifehacker.com/how-to-set-up-dhcp-reservations-and-never-check-an-ip-5822605) 。

### 第五步:配置亚音速

一旦你在你的 Raspberry Pi 上运行了亚音速，就该从你的家用电脑上访问它了。在浏览器中，键入 IP 地址，如下所示:

```
[ip address you just got]:4040
```

例如:

```
192.168.1.115:4040
```

这将打开亚音速登录页面。使用用户名 admin 和密码 admin 登录。

首先，按照说明更改您的用户名和密码。接下来，我们将亚音速指向一个音乐库。

单击“设置”>“媒体文件夹”,将媒体文件夹更改为您在 Raspberry Pi 上存储音乐的位置。如果您使用的是外置硬盘或 USB 驱动器， [请遵循以下指南之一](http://elinux.org/RPi_Tutorials) 首先进行设置。现在，您可以在本地 Wi-Fi 网络内的任何地方访问您的音乐库。但这还不够。让我们授权从任何地方访问该库:

1.  进入设置>网络
2.  选中“自动配置您的路由器以允许亚音速
3.  选中“通过互联网访问您的服务器”复选框
4.  输入您想要访问它的 URL 地址
5.  单击保存按钮

等亚音速再装弹。如果一切正常，您的状态应该列为:“成功注册的网址。”现在，您可以通过您创建的 URL 从任何地方访问您的音乐库。

如果状态显示其他内容，则意味着您的路由器不支持自动端口转发，因此您需要手动设置。 [本指南](http://www.subsonic.org/pages/getting-started.jsp#2.2) 带您完成基本步骤，但设置和故障排除取决于您的具体路由器。

### 第六步:配置亚音速的移动应用

亚音速的 [可以从桌面和手机上的大量不同应用](http://www.subsonic.org/pages/apps.jsp) 中访问。测试了几个出来，我最喜欢 Mac 上的[Submariner](http://www.read-write.fr/subapp/)和 iOS 上的 [Audiophone](https://itunes.apple.com/us/app/audiophone/id704052103?mt=8) 。设置取决于你使用的应用程序，但通常很简单。您只需要第四步中的服务器地址和端口，以及您的用户登录信息。一旦设置好，只要 Raspberry Pi 打开，亚音速服务器运行，你就可以从任何地方调出你的库。

<small>*音乐由*</small> [<small>*约什伍德沃德*</small>](http://freemusicarchive.org/music/Josh_Woodward/The_Simple_Life_Part_2_1667/JoshWoodward-TSL-NoVox-207-GoodToGo_1291)<small>*/*</small>[<small>*恶劣天气加州*</small>](http://badweathercalifornia.tumblr.com/) <small>*。照片由*</small> [<small>*塔齐什尼克*</small>](http://www.shutterstock.com/pic.mhtml?id=125978432&src=id)<small></small>*[<small>*多纳塔斯 1205*</small>](http://www.shutterstock.com/pic.mhtml?id=121247890&src=id)*