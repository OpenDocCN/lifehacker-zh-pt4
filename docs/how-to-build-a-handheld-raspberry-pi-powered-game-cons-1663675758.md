# 如何构建一个手持的、基于 Raspberry Pi 的游戏机

> 原文:[https://life hacker . com/how-to-build-a-handset-raspberry-pi-powered-game-cons-1663675758](https://lifehacker.com/how-to-build-a-handheld-raspberry-pi-powered-game-cons-1663675758)

树莓派是一款很棒的迷你电脑，可以让 [在童年时玩经典的视频游戏](https://lifehacker.com/how-to-turn-your-raspberry-pi-into-a-retro-game-console-498561192) 。但是，由于它的小尺寸，它也可以变成一个便携式手持游戏机，播放你最喜欢的游戏，从 NES 到 N64。我称之为“eNcade”。

Watch

eNcade 是一个用于预购 的 [Kickstarter 项目，但只要有一点工程和焊接技能，自己制作一个并不困难。](https://www.kickstarter.com/projects/2032055368/the-encade-a-portable-raspberry-pi-gaming-console)

### 你需要什么

就像 DIY 的一贯做法一样，你可以调整这些说明...好吧，随便你！但是我们将在指南中使用以下内容:

*   一个 [覆盆子](http://www.raspberrypi.org/) (很明显)。我用的是型号 B，但是你可以用你想要的任何一个——B+功能更强大一点，而新型号 A+ 更苗条。
*   一个 3.7v 的锂聚合物电池(至少 2000mah 最好)，像 [这个来自 Adafruit](http://www.adafruit.com/products/328)
*   一个屏幕。像这种 的简单复合 TFT 显示器 [就可以了。你也可以使用触摸屏，尽管](http://www.amazon.com/gp/product/B00IUGW7PM?asc_campaign=InlineText&asc_refurl=https://lifehacker.com/how-to-build-a-handheld-raspberry-pi-powered-game-cons-1663675758&asc_source=&tag=kinjalifehackerlink-20) [需要一些额外的工作](http://www.adafruit.com/product/1601) 。
*   充电/升压电路，例如 [PowerBoost 500](http://www.adafruit.com/product/1944)
*   一个箱子，可以装下所有东西(见下文)
*   一个你选择的 USB 游戏手柄——我用的是 [罗技 F310](http://www.walmart.com/ip/16419686?wmlspartner=wlpa&selectedSellerId=0&adid=22222222227000769916&wl0=&wl1=g&wl2=c&wl3=40880497232&wl4=&wl5=pla&wl6=78810873152&veh=sem)
*   单刀单掷开关，就像 RadioShack 中的
*   一些多股电线
*   焊料
*   烙铁

### 第 0 步(可选):精简你的 Pi

我使用的是型号 B Pi，但将其修改为更纤薄，这样我最终可以得到一个纤薄的设备。你可以用 B+做同样的调整，或者只使用已经更苗条的 A+。本指南 [这里](https://lifehacker.com/slim-down-a-raspberry-pi-with-a-few-mods-1654104188) 会帮你搞定。在这种情况下，大多数端口(USB、以太网、音频插孔、RCA 插孔)被完全移除，以使引脚更容易焊接，并尽可能节省空间。

### 第一步:连接电源

你的电源是手持设备最基本的部分，也是最容易连接的部分，所以我们先做这个。Raspberry Pi 需要 5 伏电压才能运行，您可以将其直接连接到 GPIO(通用输入/输出)——黄色视频输出插座旁边的 26 个引脚(如上所示)。

不过，你的电池不仅仅要为 Pi 供电——你还需要用同一块电池为你的其他组件(比如屏幕)供电。我们使用的是 3.7v 锂电池，它在 [PowerBoost 500](http://www.adafruit.com/product/1944) 的帮助下，将输出转换为 5v。有了这个电路，您可以通过连接器插入电池，并焊接两条导线:一条从 PowerBoost 上的 5v 输出引脚到 Pi 的 5v 输入(在上面的 GPIO 图上标记)，另一条从 PowerBoost 上标记为“gnd”的引脚到 GPIO 上标记为“Ground”的引脚:

虽然通常不建议直接焊接到 GPIO，但这可以节省设计空间。通常，您会使用 GPIO 接头来连接电线。PowerBoost 500 也有可以连接您的开关的引脚，如在 [PowerBoost 500 页面](http://www.adafruit.com/product/1944) 上所述。此时它应该是这样的:

### 第二步:连接你的屏幕

屏幕也不难，因为我们已经选择了一个接受复合输入并已知与 Pi 兼容的屏幕。拆开屏幕，焊接屏幕复合输入的电线(电线连接到 RCA 插孔),其中中心是信号，外部导体接地。如果你没有瘦身你的 Pi，那么这就简单多了:只需将黄色 RCA 插孔插入型号 B 的黄色插座。

屏幕的电源输入可以直接连接到电池(红色(+)连接到红色，黑色(-)连接到黑色)，因为它只有在收到来自 Pi 的信号后才会打开。

### 第三步:连接你的控制器

显然，玩游戏，你需要一个游戏手柄。这里你有很多选择，因为你可以拆开 USB 控制器，抢救电路板，并将其连接到 Pi。 [本指南](http://people.cs.vt.edu/~vanmetre/arcade/controls.html) 讲述了拆卸类似控制器的一些细节。一旦你把它拆开，你最简单的选择就是把 USB 连接从电路板直接焊接到 Pi 板的底部，就像这样:

然后，你可以把电路板放在你的盒子里(见下一节),这样按钮就会从顶部出来。这是我拿到手后的样子:

您的按钮布局将与原始控制器的布局相同，因为您只是移植了电路板。如果你想要一个更复杂的定制按钮布局，你可以使用一个 [Teensy](https://www.pjrc.com/teensy/) 微控制器，从输出端连接轻触开关来定制按钮布局。您还可以将按钮直接连接到 GPIOT5，如下文 所述。

#### 第四步:建立你的案例

在这种情况下，你可以真正发挥创造力。有很多选择，从 3D 打印( [，如果你有资源的话](https://lifehacker.com/how-to-get-started-with-3d-printing-without-spending-a-1340345210) )到切割特百惠塑料制品或其他塑料部件。如果你走 3D 打印路线，有许多 Pi 外壳 [像这个](http://www.thingiverse.com/thing:110354)STL 格式的，你可以免费得到并自己 3D 打印。看看 [Thingiverse](http://www.thingiverse.com/) ，里面有一大堆不同的选项。请记住，您必须在设计中考虑您的特定按钮位置和布局方案，以便所有东西都能很好地组合和运行。

最后，这是我的车内部的样子，全部连接起来。

### 第五步:安装你的软件和游戏

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-00QyL0AgPAE&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-00QyL0AgPAE&start=0) 

现在，简单的部分:安装您的模拟器和游戏！我们已经向您展示了如何使用 RetroPie 将树莓派变成经典的游戏机，所以只需按照我们原始指南(或上面的视频)中的说明准备好游戏。

实际的 eNcade 有自己独特的软件方法，包括一个在线多人交付服务，所以你可以和你的朋友在线玩，但使用 RetroPie 将让你的 DIY 设备走得更远。尽情享受吧！

如果你对 eNcade 项目感兴趣，请查看 Kickstarter 了解更多信息。如果你承诺，还有一个选项是获得一个 DIY 工具包，这可以省去你分别购买所有东西的麻烦。