# 如何建立一个树莓派点唱机任何非极客可以使用

> 原文：<https://lifehacker.com/how-to-build-a-raspberry-pi-jukebox-any-non-geek-can-us-1712107103>

你有大量的选择来从你的立体声系统访问你的计算机的音乐库，但是大多数需要一点技术知识来实际使用。你可以用树莓派(一种微型电脑)制作一台点唱机，任何人都可以使用，即使他们不知道树莓派是什么。

Watch

当你完成这个项目时，你将在你的客厅里有一个微型触摸屏点唱机，可以在另一台 PC(或你的 [网络连接存储](https://lifehacker.com/five-best-nas-enclosures-5968677) )上播放、控制和挑选你的音乐库中的歌曲，然后在你的立体声音响上播放它们。这里的界面很容易理解，所以它非常适合聚会或一些非极客可能想要进入播放列表的房子，而无需学习复杂的系统、计算机、Wi-Fi 密码或其他任何东西。更好的是，它都在自己的网络上工作，所以不需要担心配对设备或任何这类事情。要完成这个项目，您需要了解一些命令行知识，但仅此而已。

### 你需要什么

*   (型号 B、B+或 2 均可)
*   用于 Pi 的电源线、以太网电缆(或 Wi-Fi 卡)、SD 卡和用于设置的键盘
*   一个触摸屏( [我们用的这个，来自 Adafruit](http://www.adafruit.com/products/2423) 的 PiTFT)
*   一台 [家庭服务器或装有 MP3 文件的电脑](http://lifehacker.com/turn-an-old-computer-into-a-do-anything-home-server-wit-510023147)
*   连接点唱机的立体声音响和扬声器
*   机箱(可选，但人们会接触到它，所以您应该将它放在某个地方。新 [官案将功大](http://lifehacker.com/the-official-raspberry-pi-case-protects-your-tiny-compu-1711970411)

### 第一步:在 Pi 上安装 Raspbian

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-aTQjuDfEGWc&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-aTQjuDfEGWc&start=0) 

首先:您需要设置并安装 Raspbian。如果你用的是我用过的 PiTFT 触摸屏显示器，用 [Adafruit 的自定义 Raspbian 图像](https://learn.adafruit.com/adafruit-pitft-28-inch-resistive-touchscreen-display-raspberry-pi/easy-install) 来设置就容易多了。您将按照与 Raspbian 相同的方式在 SD 卡上安装映像，但是操作系统已经为显示器进行了配置。你可以按照我们的指导在这里 制作一张 [的图片，不过这里有个简短的版本:](http://lifehacker.com/a-beginners-guide-to-diying-with-the-raspberry-pi-5976912)

**窗户**

1.  [下载最新版本的 Raspbian](https://learn.adafruit.com/adafruit-pitft-28-inch-resistive-touchscreen-display-raspberry-pi/easy-install) 并解压。img 文件在里面。
2.  [下载 win32 diski manager](https://launchpad.net/win32-image-writer/+download)并解压应用程序(。exe 文件)中。
3.  使用读卡器将 SD 卡插入 Windows PC。
4.  双击打开您刚刚下载的应用程序 Win32DiskImager.exe。如果你运行的是 Windows 7 或 8，右击它，选择“以管理员身份运行”。
5.  如果应用程序没有自动检测到您的 SD 卡，请单击右上方的下拉菜单(标有“设备”)并从列表中选择它。
6.  在应用程序的图像文件部分，单击小文件夹图标并选择 Raspbian。您刚刚下载的 img 文件。
7.  单击 Write 按钮，等待 Win32DiskImager 完成它的工作。完成后，您可以安全地弹出您的 SD 卡，并将其插入您的 Raspberry Pi。

**OS X**

1.  [下载最新版本的 Raspbian](https://learn.adafruit.com/adafruit-pitft-28-inch-resistive-touchscreen-display-raspberry-pi/easy-install) 并解压。img 文件在里面。
2.  [下载 RPi-sd 卡构建器](http://alltheware.wordpress.com/2012/12/11/easiest-way-sd-card-setup) (一定要为你安装的 OS X 版本选择合适的版本)并解压应用程序。
3.  使用读卡器将 SD 卡插入 Mac。
4.  打开 RPi-sd 卡生成器。你会立即被要求选择一个拉斯比图像。选择。您之前下载的 img 文件。
5.  系统会询问您是否连接了 SD 卡。因为我们之前插入了它，所以它是，所以继续并单击 Continue。您将看到 SD 卡选项。如果您只插入了一个，您将不会在列表中看到任何其他内容，它将被检查。如果没有，只需检查您想要使用的卡，然后单击确定。
6.  输入您的管理员密码，然后单击确定。
7.  您将被询问 SD 卡是否被弹出。这是应该发生的，因为应用程序需要卸载它，以便它可以执行直接拷贝。仔细检查您的 SD 卡在 Finder 中是否不再可用。不要将其从 USB 端口上移除。确定后，点按“继续”。
8.  RPi-sd 卡生成器完成准备您的 sd 卡，安全弹出它并将其插入您的 Raspberry Pi 单元。

### 第二步:挂上你的显示器

Raspberry Pi 有一个 GPIO(通用输入/输出),触摸屏可以插入其中。如果你看看你的树莓皮，它是角落里的一组大头针。如果你还没有，继续点击你的树莓派上的显示屏。当它连接好后，插入键盘、以太网电缆(或 Wi-Fi 适配器)，然后是电源线。你将被要求校准触摸屏。按照屏幕上的说明操作，你就一切就绪了。

### **第三步:分享你电脑的音乐库**

在您开始使用 Raspberry Pi 之前，您应该在家用电脑上设置音乐共享。Windows 和 Mac 的过程是不同的。

**窗户**

1.  导航到您电脑的音乐文件夹。
2.  右键单击文件夹，选择“共享”，然后选择域。如果您只在家庭网络上，您可以将它保持为公共的，并且它只对家庭网络上的其他电脑可用。否则，选择受密码保护的共享，然后输入密码。
3.  记下文件夹的位置和您的电脑名称(类似于 ThorinPC/Music)。

**Mac**

1.  打开系统偏好设置。
2.  点击“共享”图标。
3.  确保选中“文件共享”框。
4.  点按“共享文件夹”下方的“+”，选择您的音乐文件夹，然后点按“完成”
5.  回到共享菜单，选择“选项…”
6.  选择“Windows 文件共享”并输入您的密码。这将使树莓派很容易抓取你的文件。

现在你的家庭电脑共享了它的音乐库，你可以回到你的 Raspberry Pi 了。

### 第四步:安装和配置 MPD

这个项目的基础是 [音乐播放器守护进程](http://mpd.wikia.com/wiki/Music_Player_Daemon_Wiki) (MPD)。这是一个用于播放音乐的服务器端应用程序。这意味着它没有图形界面，它只是允许你的树莓皮播放音乐文件。一旦这个项目设置好了，您就不需要在命令行中挖掘来实际使用它，但是在初始设置过程中您将需要这样做。首先，你需要下载 MPD 和 MPC(控制器)。当您之前启动您的 Raspberry Pi 时，您应该在触摸屏校准后到达命令行。如果没有，并且你在 Raspbian 中，点击菜单图标并选择“注销”您将从 Raspberry Pi 的命令行完成本指南中的所有工作，键入:

```
sudo apt-get install mpd mpc
```

等待安装。完成后，您应该通过运行以下命令来更改一些设置:

```
sudo nano /etc/mpd.conf
```

找到以下列开头的行:

```
 #zeroconf_enabled “yes”
```

并删除它前面的#来取消对它的注释。按 CTRL+X，选择 Y 保存并退出。

### 第五步:建立音乐库

接下来，你需要将 MPD 指向你的音乐库。为此，您将创建一个文件夹，然后在其中安装音乐库。你需要用 [sudo 命令](http://lifehacker.com/become-a-command-line-ninja-with-these-time-saving-shor-5743814) 来完成大部分工作，因为你需要 root 权限来安装所有的东西并正常工作。首先制作一个文件夹:

```
sudo mkdir /mnt/music
```

接下来，我们将确保它在 Pi 启动时挂载。运行这个:

```
sudo nano /etc/fstab
```

然后添加这一行，用您在第三步中收集的信息和/文件夹名替换计算机名作为您的音乐文件夹位置:

```
//Computername/foldername /mnt/music cifs guest,uid=1000,gid=1000,iocharset=utf8 0 0
```

它应该是这样的:

```
//WindowsPC/music /mnt/music cifs guest uid=1000,gid=1000,iocharset=utf8 0 0
```

**注意**:如果你需要登录你的共享文件夹，你也需要用`username=yourusername,password=yourpassword`替换`guest`。

完成后，点击 Ctrl+X 保存并退出。接下来，让我们测试并确保挂载正常工作。键入:

```
sudo mount -a
```

如果您没有收到错误消息，则说明它安装正确。现在，请快速浏览一下，确保您所有的音乐文件都在那里。运行该命令:

```
ls -l /mnt/music
```

你应该看到你所有的音乐文件。如果一切正常，您需要为 MPD 创建一个符号链接，这样它就知道去哪里寻找那些文件。键入:

```
sudo ln -s /mnt/music /var/lib/mpd/music
```

现在，MPD 应该都设置好了。你只需要浏览你的音乐库，就可以得到所有的内容。键入:

```
mpc update
```

根据您的库的大小，这将需要一点时间，所以让它做它的事情。

### 第六步:配置网络和 USB 驱动器访问

接下来，您将配置 Zeroconf，如果您不想走过去使用触摸屏，它将允许您从其他设备控制您的点唱机。键入:

```
sudo apt-get install libnss-mdns
```

完成后，启动它:

```
sudo service avahi daemon restart
```

现在你可以随意使用类似安卓版 的 [MPDroid 或者 iOS 版](https://play.google.com/store/apps/details?id=com.namelessdev.mpdroid&hl=en) 的 [MPDluxe 这样的手机 app 作为 Pi 点唱机的遥控器。在我们开始之前，您还可以设置自动点唱机来读取连接的 USB 驱动器上的文件，如果朋友带着一堆 MP3 来，这很方便。遗憾的是，你不能只插上手机就能访问音乐，因为树莓派很可能无法识别它。要打开 USB 支持，请键入:](http://kineticfactory.com/MPDluxe/)

```
sudo apt-get install usbmount
```

然后将 MPD 指向 u 盘:

```
sudo ln -s /media/ /var/lib/mpd/music/
```

就是这样。现在你应该可以在任何地方播放音乐了。

### 第七步:安装自动点唱机软件

现在，您的 Pi 可以从命令行访问您的音乐并播放它。那很无聊。让我们来设置漂亮的触摸屏界面。

为此，我们将使用一个名为 [Pi-Jukebox](https://github.com/mark-me/Pi-Jukebox) 的程序。它本质上是 MPD 的一个前端，允许你使用触摸屏来控制音乐播放。这里的安装非常简单。从命令行运行:

```
git clone https://github.com/mark-me/Pi-Jukebox
```

这会将所有需要的文件下载到 Raspberry Pi 和 Pi-Jukebox 文件夹中。在运行它之前，我们需要安装 Python:

```
sudo apt-get install python-pip
```

一旦安装完毕，就该运行 Jukebox 程序了。

### 第七步:运行并使用自动点唱机软件

要启动自动存储塔，您只需键入一个命令:

```
sudo python pi-jukebox.py
```

如果一切按计划进行，您现在应该会在触摸屏上看到 Pi-Jukebox 软件。以下是每个按钮的含义:

在很大程度上，界面的工作方式与您预期的一样。你可以上下滑动来浏览你的库，点击任何控制来开始和停止播放，点击选择来加载它。Pi-Jukebox 的工作方式就像一个自动点唱机，所以你可以将你的每一个选择添加到当前正在播放的播放列表中，然后从那里开始播放。没有一种直接的方法可以简单地播放一张专辑而不将其添加到播放列表中。

设置选项也很简单，但是值得一试。您可以将点唱机设置为随机播放、重复播放轨道等。但是对于所有的意图和目的，你已经准备好开始听音乐了。如果您还没有，请将您的 Pi 连接到您的立体声系统并开始演奏。