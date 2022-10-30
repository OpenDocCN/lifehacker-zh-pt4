# 如何用 Lakka 将你的电脑(或其他设备)变成复古街机

> 原文：<https://lifehacker.com/how-to-turn-your-pc-or-other-device-into-a-retro-arca-1703576831>

如果你正在寻找一种使用旧 PC 的有趣方式，Lakka 可以将它变成一台令人惊叹的复古游戏机。这个简单的设置不需要任何高级的 Linux 知识，你甚至可以使用你已经拥有的控制器来玩你最喜欢的老式学校游戏。以下是实现这一目标的逐步指南。



### **你将从 Lakka 得到什么，它与其他模拟器有何不同**

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-JwUVV3xMRwU&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-JwUVV3xMRwU&start=0) 

Lakka 是一个轻量级的基于 Linux 的操作系统，源自[open elec](http://lifehacker.com/openelec-is-a-fast-booting-self-updating-version-of-xb-5851924)(Kodi 家庭影院软件的一个版本)，它将最好的复古游戏模拟器结合到一个现成的安装系统中。一旦你设置好了，你就有了一个可以模拟从 Atari 游戏到 Playstation 游戏的一体化游戏机。以下是您可以模拟的系统的完整列表:

*   3DO ( [4DO](http://www.fourdo.com/) )
*   Playstation ( [甲壳虫 PSX](http://wiki.libretro.com/index.php?title=Beetle/Mednafen_PSX) )
*   SNES /超级 Famicom([bsnes-水星平衡](http://wiki.libretro.com/index.php?title=Bsnes-mercury) ， [SNES9x 下一个](http://www.snes9x.com/) )
*   任天堂 ds(t1【脱毛】T3】
*   街机( [FBA](http://www.gametronik.com/site/emulation/FBA/)
*   Game Boy/Game Boy Color([Gambatte](http://sourceforge.net/projects/gambatte/))
*   世嘉主控系统/游戏装备/ Mega Drive / CD ( [创世纪加 GX](http://segaretro.org/Genesis_Plus_GX) )
*   Lynx ( [得心应手](http://handy.sourceforge.net/) )
*   neo Geo Pocket/Color([Mednafen Neopop](http://mednafen.sourceforge.net/documentation/ngp.html))
*   PC 发动机/ TurboGrafx 16 ( [梅德纳芬 PCE FAST](http://mednafen.sourceforge.net/documentation/pce.html) )
*   PC-FX([Mednafen PC-FX](http://mednafen.sourceforge.net/documentation/pcfx.html))
*   虚拟男孩( [Mednafen VB](http://mednafen.sourceforge.net/documentation/vb.html) )
*   旺德万/色([【medna fen cygne】](http://mednafen.sourceforge.net/documentation/wswan.html)
*   任天堂 64 ( [Mupen64Plus](http://en.wikipedia.org/wiki/Mupen64Plus)
*   NES /法米科姆( [内斯特皮亚](http://nestopia.sourceforge.net/) )
*   PSP(便携式游戏机)
*   Atari 7800 系统
*   雅达利 2600()
*   Game Boy 进阶([)VBA-M](http://sourceforge.net/projects/vbam/)【T3)
*   雅达利美洲虎( [虚拟美洲虎](http://www.icculus.org/virtualjaguar/) )

在你用一些 rom 加载你的系统后，你将可以用一个控制器来浏览 Lakka 的菜单和游戏。事实上，Lakka 类似于我们在 之前介绍过的 RetroPie 版本，但有一个主要区别:Lakka 可以安装在很多地方，而不仅仅是小小的树莓派迷你电脑。它支持大量不同的设备，**包括几乎任何普通的个人电脑**。

以下是您可以安装 Lakka 的所有机器:

*   一台 PC(记住，它是自己的操作系统，所以你不能同时运行 Windows 或 OS X)
*   一杯树莓酱 A+ / B+(最好是 B+
*   CuBox-i
*   蜂鸣板
*   香蕉派
*   立体棋盘 2
*   Cubietruck

如果你注意到树莓派 2 没有上市，你没有疯。Raspberry Pi 2 和 Odroid-C1 的构建都还在进行中。你仍然可以下载和安装 Lakka，但是在撰写本文时，开发人员认为它在 Pi 2 上不太稳定，所以请记住这一点。幸运的是，RetroPie 在 Raspberry Pi 2 上工作得很好，所以你现在可以使用。

如果你有一个树莓派 A 或 B+,你正在决定 Lakka 和 RetroPie 之间，有一些差异应该注意到。如果你喜欢时尚和简单，Lakka 的界面看起来干净得多——非常类似于 PS3 或 PS4 操作系统——控制台在屏幕上水平运行，而游戏则垂直运行。虽然有点沉闷，但 RetroPie 的菜单——特别是在当前的 3.0 版本中——更加丰富多彩，并在您探索时显示每个系统的实际徽标。然而，Lakka 的版本正在不断更新，更好的图标据传正在路上。

当涉及到系统设置时，Lakka 使动态调整变得更加容易。在最左边有一个设置菜单，里面有很多选项，不用键盘就可以轻松访问。你可以插入一个带有 home 按钮的控制器——PS3/PS4 或 Xbox 360/Xbox One——控制器将被识别并准备好立即使用。然后，你可以开始玩游戏，通过 home 键返回到系统的主菜单(你的游戏状态是冻结的)，只需用你的控制器更改一些设置，然后跳回到你的冻结游戏状态，就像它从未发生过一样。RetroPie 在使设置更易访问方面越来越好，但 Lakka 总体上感觉更快更容易一些。总的来说，Lakka 感觉更像是一个普通用户更喜欢的实际控制台。

当然，虽然 Lakka 在像 Pi 这样的紧凑系统上运行得很好，但一台旧 PC 在使旧系统现代化方面会做得更好。显然，如果你对模仿任天堂 64 和 Playstation 等系统的游戏感兴趣，那么越强大越好。幸运的是，如果你在个人电脑上安装，你很可能比 [更有能力](http://lifehacker.com/whats-the-best-device-for-emulating-my-retro-games-1543810224) 顺利运行一切。或者，如果您有一台旧笔记本电脑，您可以创建一个便携式游戏控制台，可以随身携带到任何地方。如果您愿意，您甚至可以将您的旧 PC 塔式机拆成 [定制机柜](http://lifehacker.com/how-to-create-the-ultimate-tech-infused-retro-arcade-co-521331796) 。这些事情以前肯定有人做过，但是 Lakka 让任何人做起来都更容易。

### **你需要什么**

要在 PC 上安装 Lakka，您需要一些东西:

*   Mac 或 PC 下载 Lakka 并创建 USB 拇指驱动器安装程序。
*   一台旧电脑(或上面列出的其他设备),你不介意把它作为你的 Lakka 主机。安装 Lakka 就是把它作为系统的 OS 安装。**不要把它安装在你需要做其他事情的机器上**(如果你没有额外的电脑来做这件事，我们稍后会介绍另一种方法)。
*   至少 512MB 大小的空闪存驱动器(至少 2 GB 可能是最好的)。在此过程中，您将无法使用此 u 盘进行任何其他操作，因此在擦除之前，请备份 u 盘上的所有内容。
*   一个 USB 键盘，用于 Lakka 控制台上的设置和一些高级选项和设置。
*   路由器(通过家庭网络传输您的 rom)。
*   至少一根以太网电缆(用于将您的 Lakka 机器连接到路由器；尚不支持 Wi-Fi)。
*   显示器或电视(如果你没有在笔记本电脑上安装 Lakka)。
*   一份免费的 [7-Zip](http://lifehacker.com/the-best-file-archive-utility-for-windows-5820410) 软件(如果你是 Windows 用户，没有解压文件的选择)。
*   一份免费软件[win32 diski manager](http://sourceforge.net/projects/win32diskimager/)(如果你是 Windows 用户的话)。
*   PS3、PS4、Xbox 360、Xbox One 或其他可通过 USB 连接的控制器。

### **第一步:准备好你的专用拉卡机**

值得重申的是，在 PC 上安装 Lakka 意味着清除硬盘上的所有内容。在深入研究之前，请务必备份您需要的任何数据。不过，如果你要为这个设置添加一个不同的硬盘，那就万事俱备了。

在你做任何事情之前，你需要确定你安装 Lakka 的机器上的 CPU 是什么类型的。32 位和 64 位系统有不同的软件包可以下载，所以这很重要。如果您要使用的机器上仍然有操作系统，那么检查起来很容易:

*   **Windows XP / 7 / Vista / 8:** 打开开始菜单>右键电脑>选择属性。您应该在系统类型旁边看到 32 位或 64 位。
*   **基于英特尔的 Mac:** 点击苹果菜单>关于这台 Mac >更多信息… >找到处理器名称部分，将名称与苹果 T5 的图中的[进行比较。](https://support.apple.com/en-vn/HT201948)

有了这两样东西，你就可以安装 Lakka 了。

### **第二步:将 Lakka 下载并“刻录”到 USB 驱动器**

跳上你的普通电脑(没有安装 Lakka 的那台)。无论你使用的是 Windows 还是 Mac，下载和安装 Lakka 都非常简单:

1.  从拉卡网站下载 [32 位拉卡软件包](http://sources.lakka.tv/nightly/Generic.i386/Lakka-Generic.i386-devel-20150307205832-r20834-ge8d52d6.img.gz) 或 [64 位拉卡软件包](http://sources.lakka.tv/nightly/Generic.x86_64/Lakka-Generic.x86_64-devel-20150307205641-r20834-ge8d52d6.img.gz) 。
2.  解压软件包得到 Lakka 镜像。在 Windows 上，你可以使用像 7-Zip 这样的程序。在 OS X 上，你只要双击文件就可以解压。
3.  如果你用的是 Windows，插入你的闪存盘，打开 Win32DiskImager，设置 Lakka。img 作为您的图像文件。然后选择您的闪存驱动器作为设备，并选择写入。
4.  如果你在 OS X 上，打开一个终端(/Applications/Utilities/Terminal)并运行`diskutil list`来记录你当前的驱动器和分区。然后插入您的闪存驱动器并再次运行`diskutil list`以识别哪个磁盘是您的闪存驱动器并记下它。去拉卡。img 文件的位置，并运行`sudo dd if=Lakka-*.img of=/dev/diskN`(其中 diskN 是您之前识别的 USB 驱动器的名称。**确保您有正确的磁盘名称！**)。过一会儿，你会收到一条消息，告诉你转了多少钱，然后你就可以再次控制你的提示了。
5.  弹出并移除闪存驱动器。

现在 Lakka 安装程序已经准备好了。

### **第三步:从你的 u 盘启动并运行安装程序**

当你准备好了，继续把 USB 驱动器、键盘和显示器插到你想用来玩 Lakka 的 PC 上。然后，准备从系统 BIOS 中的 USB 驱动器 将您的 Lakka PC 引导至 [:](http://lifehacker.com/how-to-boot-from-a-usb-drive-or-cd-on-any-computer-5991848)

1.  重启你的 Lakka 电脑，等待第一个屏幕弹出。您应该在屏幕上的某个地方看到一条类似“按 F12 选择引导设备”的快速消息。一看到就按。
2.  然后会出现一个菜单，上面有一个列表，列出了你可以启动的东西。突出显示您的 USB 驱动器，然后按 Enter 键。
3.  如果您没有看到 USB 驱动器选项，请选择“BIOS 设置”或“BIOS 设置”选项(您可能需要重新启动并在启动时点击不同的键来找到此菜单)。转到“引导设备”，或类似的东西，并确保从 USB 驱动器启动是启用的。

一旦你能够从 USB 驱动器启动，按照以下步骤安装 Lakka 作为电脑的新操作系统:

1.  从 USB 驱动器启动，你应该看到 Lakka 启动菜单。
2.  选择运行安装程序，选择确定，然后选择(1)快速安装 OpenELEC.tv(不要担心任何其他选项)。
3.  现在选择要安装它的驱动器(你可能只有一个选项) >选择 OK >你应该会看到 Lakka 开始安装。

完成后，你会被要求重新启动。选择重新启动，并在 USB 驱动器再次启动前将其移除。它会很快自动重启，但之后你会看到 Lakka 主菜单干净的红色屏幕。

### **替代选项:从你的 u 盘运行 Lakka Live】**

当你打开 Lakka 启动菜单时，你可能会注意到有一个选项可以实时运行。如果你对将整台机器作为你的复古游戏主机不感兴趣，你可以从 USB 驱动器运行整个操作系统作为替代，而不用擦除你原来的机器。

当您选择 Run Live 时，您会看到与安装时完全相同的东西。一旦你将一些游戏加载到 USB 驱动器上，你就可以启动驱动器，加载 Lakka，并在几乎任何一台装有相同类型系统的计算机上玩它们(如果你有 64 位映像，你几乎可以在任何 64 位系统上运行它)。您甚至可以将保存的游戏和截图保存在 u 盘上。这非常适合在旅行时让笔记本电脑发挥双重功能。插入 USB，启动 Lakka，在长途飞行中玩复古游戏。当你吃饱了，你可以重新启动你的正常操作系统，做一些平常的工作。

**专业提示:**从 USB 驱动器运行 Lakka live 是测试您的硬件是否也能运行 Lakka 的一个很好的方法。Lakka 应该可以在大多数个人电脑上运行，但开发者确实提到硬件可能会有很大差异，所以不能保证所有系统都能运行。

### **第四步:从你的主电脑上给 Lakka 添加 rom**

假设你已经有了一些自己的 rom(或游戏文件)，你需要将它们从你的主电脑转移到你的新 Lakka 主机上。为此，请确保您的主计算机通过 Wi-Fi 或直接连接到路由器连接到您的家庭网络，并遵循以下步骤:

1.  确保您的 Lakka 机器已开机，并且仅通过直接以太网连接连接到您的路由器。Lakka 目前不支持 Wi-Fi。
2.  在你的主计算机上找到你的只读存储器并复制它们。下面是当前支持的文件类型 的 [列表。](http://www.lakka.tv/doc/ROMs-and-BIOSes/)
3.  如果您的主电脑使用 Windows，请选择开始，然后选择电脑，在左侧的列表中找到网络，然后选择 LAKKA。然后打开 rom 文件夹，粘贴你的 rom。务必让传输完成。有几次，Windows 很难在网络上找到 Lakka，但我可以通过在 Windows 资源管理器中键入“//lakka”并按 Enter 键来解决这个问题。
4.  如果您的主电脑使用 OS X，请打开 Finder，在左侧的列表中找到 LAKKA，转到 ROMs 文件夹，然后将您的 rom 粘贴到那里。务必让传输完成。
5.  在你的 Lakka 控制台上，打开最左边的设置菜单，向下滚动退出 RetroArch 并选择它。

Lakka 应该重新启动，当它回来了，你会看到你所有的 rom 都准备好了。只需前往您想要玩的游戏，在游戏手柄上点击 B 或 **O** (圆圈)来选择它，然后再次点击 B 或 **O** 来运行它。

### **控制器和其他功能**

Lakka 的设计可以自动识别你插入的几乎任何 USB 控制器。任何 PS3、PS4、Xbox 360 或 Xbox One 控制器都保证开箱即用。如果你有一个蓝牙加密狗 ，你甚至可以无线使用它们。虽然我测试的大多数控制器都运行良好，但还是有一些意外。

一个通过 USB 连接的任天堂 Wii U Pro 控制器根本不能工作，这并不奇怪。然而，当我的余辉 PC 控制器(看起来完全像 Xbox 360 控制器)也不工作时，我感到很惊讶。然而，对于工作正常的控制器来说，如果它们有一个“home”按钮——比如 Xbox 和 Playstation 控制器——它会暂停你的游戏状态，并带你回到主操作系统菜单。

我遇到的最大惊喜是当我测试真正的超级任天堂控制器时，它们工作得完美无缺。我用了 Mayflash 的这个 [USB SNES 控制器适配器，没有任何问题。能够用经典曲目演奏经典曲目*真是太棒了。*](http://www.amazon.com/SNES-Controller-Adapter-USB-Super-NES/dp/B002IXZ5DE/ref=sr_1_7?asc_campaign=InlineText&asc_refurl=https://lifehacker.com/how-to-turn-your-pc-or-other-device-into-a-retro-arca-1703576831&asc_source=&ie=UTF8&keywords=super nintendo usb&qid=1431116496&sr=8-7&tag=kinjalifehackerlink-20)

Lakka 还内置了其他一些非常有趣的功能。你可以保存游戏截图，甚至录制游戏视频。当然，视频是古老的 BSAVE 位图格式，所以我不知道你能做什么(如果你让我知道)。它还有一个内置的“倒带”功能。如果你在插入键盘的情况下启用了它，你可以按“r”键来回放游戏中刚刚发生的事情。如果你错过了一次跳跃，被敌人杀死，或者犯了其他错误，你可以重新开始，再试一次。这是一个非常方便的功能，对于那些艰苦的游戏，你想得到怀旧，但不想把你的头撞上。

### **更多资源**

你应该有你需要的一切来运行或安装 Lakka 在你的电脑上。如果您需要帮助或对更高级的技巧感兴趣，可以去以下几个地方:

*   [其他 Lakka 安装教程](http://www.lakka.tv/get/) :如果你想学习如何在 Raspberry Pis 和其他设备上安装，这里有那些安装的说明。

*   [LibRetro 论坛](http://libretro.com/forums/forumdisplay.php?f=26) :用于故障排除或其他高级问题。

*   [RetroZone](http://www.retrousb.com/index.php?cPath=21&osCsid=5c0df50d7eff05c5586ccdd4f1b1b7f5) :老派控制器适配器和 USB 控制器的绝佳来源。

<small>*插图由塔拉·雅各比创作。*T3】</small>

[Open *kinja-labs.com*](http://kinja-labs.com/related-widget/?posts=1536403860,521331796,1516605379&title=More Ways to Get Your Retro Game On)