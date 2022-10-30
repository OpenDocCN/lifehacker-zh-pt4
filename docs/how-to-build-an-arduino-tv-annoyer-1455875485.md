# 如何建立一个 Arduino 电视烦扰

> 原文：<https://lifehacker.com/how-to-build-an-arduino-tv-annoyer-1455875485>

Arduino 粉丝们，这个项目可以在你想关掉电视的时候打开电视。它是一个完美的愚人节玩笑或恶作剧礼物——或者，本着 [邪恶周](http://lifehacker.com/tag/evil-week) 的精神，在一年中的任何时候用它来让人疯狂。你可以把它藏在一个不显眼的地方，假设你已经有了一个 Arduino 和工具，它的制作成本不到 1.50 美元。



***本帖最初出现在*** [***上***](http://www.instructables.com/id/150-Arduino-TV-Annoyer-Turns-TVs-on-when-you-/?ALLSTEPS) ***。*T15】**

我几乎一生都在和电子打交道。大约六个月前，我开始做 [Arduino](https://lifehacker.com/getting-started-with-arduino-electronics-hacking-5752663) ，我已经做了 150-200 个不同的项目。我还用 Arduino 和其他微控制器创造了许多其他原创的东西。我甚至自己造了一台电脑，所以你知道我不是在瞎搞！让我们开始吧。

### 第一步:零件清单

这是你做这个项目需要的东西。我已经包括鼠标链接和项目旁边的价格。

**组件**

*   1x 红外探测器(0.78 美元)[http://goo.gl/6sSN6](http://goo.gl/6sSN6)
*   1x 广角红外线 LED(0.23 美元)[http://goo.gl/5PFlS](http://goo.gl/5PFlS)
*   1x 窄角红外 LED(0.23 美元)[http://goo.gl/67sCf](http://goo.gl/67sCf)
*   1 个 2N3904 PNP 晶体管(或同等产品)(0.08 美元)[http://goo.gl/XD3jI](http://goo.gl/XD3jI)
*   1x 10 欧姆电阻器(棕色、黑色、黑色、金色)(0.05 美元)[http://goo.gl/UiKDs](http://goo.gl/UiKDs)
*   1x 47 欧姆电阻器(黄色、紫色、黑色、金色)($ 0.10)[http://goo.gl/89jXQ](http://goo.gl/89jXQ)
*   1x Arduino Uno(或同等产品)(25.00 美元)[http://goo.gl/p9wVs](http://goo.gl/p9wVs)
*   一些电线(最好是实芯的，22 号左右)(在你当地的五金店大约 7-8 美元)

**工具**

*   1 根 USB A-B 线(用于 Arduino 编程)($ 2.95)[http://goo.gl/3f6rx](http://goo.gl/3f6rx)
*   1 个烙铁(可选)(在您当地的五金/电子商店大约 15-25 美元)
*   1 卷薄焊料(在当地五金/电子商店大约 10 美元)
*   1 块无焊试验板(在当地电子商店大约 5-6 美元)
*   1 台电脑(我希望你知道在哪里可以买到)
*   1x Arduino IDE(这里可以下载)

### 第二步:接线

集合时间到了！我是在无焊试验板上做的。(*注:完整的分步照片见原始说明书。)*

1.插入红外探测器。确保它上面的穹顶正对着你。

2。将探测器最左边的管脚连接到 Arduino 数字管脚 2，中间的管脚接地，最右边的管脚连接到+3.3v
T3。插入 2N3904 NPN 晶体管。确保平的一面朝向你。

4。将晶体管最左边的引脚连接到 47 欧姆电阻，中间的引脚通过 10 欧姆电阻连接到 Arduino 数字引脚 3 (PWM)，最右边的引脚接地。

5。将阴极(负极，引脚较短，侧面标有扁平部分以指示阴极)连接到 47 欧姆电阻的另一端，将阳极(较长的引线，不是阴极)连接到+3.3V。

### 第三步:上传草图

现在为 [编程](http://lifehacker.com/how-to-start-making-your-own-electronics-with-arduino-a-5875365) 。使用 USB A-B 线将您的 Arduino 连接到电脑，然后下载T5。ZIP 文件 。在。ZIP 文件，应该有一个文件夹叫“TV_Annoyer。”将此文件夹复制到 Arduino Sketchbook 文件夹中。在 Windows 机器上，它通常位于“C:\Users\\Documents\Arduino”

在 Arduino IDE 中打开草图(从 Arduino.cc 网站下载)，上传到 Arduino 板上。如果上传不正确，试试这些故障排除技巧:

1。重新启动 Arduino IDE。

2。尝试将 Arduino 插头拔出/重新插入电脑。

3。确定您的 Arduino 已正确连接到电脑。

4。检查是否在 IDE 顶部的“工具>板”菜单中选择了正确的板。

5。确保在 IDE 顶部的“工具>端口”菜单中选择了正确的 COM 端口。你可以通过点击“开始”按钮，搜索“设备管理器”来检查你的 Arduino 在哪个 COM 端口上。然后点击“端口(COM & LPT)”选项旁边的箭头。您的 Arduino 板应该在列表中，在它所连接的 COM 端口旁边。

### 第四步:使用它！

在您成功连接所有设备并将草图上传到 Arduino 后，它就可以使用了！将它放在电视机旁边，插上电源，然后点按电视机的遥控器，进行测试。确保红外 led 指向电视，并且红外探测器上的圆顶朝向遥控器。

### 第五步:焊接(可选)

如果你想把它焊小一点，请便。我建议使用一小块 perfboard 来焊接它。(如果你愿意，它甚至可以是一个盾牌！)

[$1.50 Arduino 电视烦扰器](http://www.instructables.com/id/150-Arduino-TV-Annoyer-Turns-TVs-on-when-you-/?ALLSTEPS) |指示物

* * *

<small>*亚历克斯·盖伊(Alex Gay)喜欢编写代码，构建东西，拆解东西，看看它们的内部工作原理。他希望有一天能为微软或英特尔设计电脑和电脑部件。【T2*</small>

*<small>这篇文章是我们的</small>* [*<small>恶周</small>*](https://lifehacker.com/welcome-to-lifehackers-fourth-annual-evil-week-1453143089) *<small>系列的一部分，在这里我们看到了做事的阴暗面。知道邪恶意味着知道如何打败它，所以你可以用你的邪恶力量做好事。想要更多吗？查看我们的</small>* [*<small>恶周标签页</small>*](http://lifehacker.com/tag/evilweek) *<small>。</small>*

<small>*想看看你在 Lifehacker 上的作品？邮箱*</small> [<small>*泰莎*</small>](https://mail.google.com/mail/?view=cm&fs=1&tf=1&to=tessa@lifehacker.com) <small>*。*T15】</small>