# 如何开始用 Arduino 和其他人的代码制作自己的电子产品

> 原文：<https://lifehacker.com/how-to-start-making-your-own-electronics-with-arduino-a-5875365>

一年一度的消费电子展正在举行，这意味着成千上万的人已经来到拉斯维加斯，盯着明年的灰尘收集垃圾。也许你可以做得更好。也许是时候去看看 Arduino 了。



Arduino 这个词可能会让人联想到一个蜷缩在工作台上的大嘴巴极客的形象，但它的简单性使它成为即使是最不擅长电子产品的人进入电子产品的切入点。我们将概述 Arduino 本身的基础知识，疯狂混乱的电线意味着什么，然后逐步介绍如何使用他人的代码和原理图来构建您的第一个电子项目，无需编程。

这些年来，我们已经 [展示了我们聪明的 Arduino hacks](http://lifehacker.com/arduino/) 。虽然对他们中的许多人来说，这个过程可能看起来极其复杂，非常令人讨厌，但开始起来却出奇的容易。在本指南中，我们将一步一步地介绍如何使用 Arduino 创建一个环境光线显示器(见右图),该显示器从您的电脑中获取数据。这个项目从你的计算机中获取颜色信息，并在显示器后面用相似的颜色点亮一条灯。它可以通过增加电脑背后的光线来帮助减轻眼睛疲劳，但它也为你的电影观看体验增添了一个伟大的视觉元素(这就是为什么该功能是 [一些电视](http://www.amazon.com/Philips-42PFL7432D-42-Inch-1080p-Ambilight/dp/B000NVBIM0/?asc_campaign=InlineText&asc_refurl=https://lifehacker.com/how-to-start-making-your-own-electronics-with-arduino-a-5875365&asc_source=&ref=sr_1_1&tag=kinjalifehackerlink-20) 的卖点)。在我们深入该项目之前，让我们快速浏览一下 Arduino 背后的基础知识，以及您可以仅使用其他人的免费开源 Arduino 代码进行的各种项目。

### Arduino 是什么鬼东西？

对于外行人来说，Arduino 看起来就像一个疯狂的小机器，用细小的电线连接到一小块塑料上。一旦你有了一个工具包，它就开始变得更有意义了。

Arduino 的核心是一个小型的可编程微控制器板，它接受并存储来自计算机的代码，能够产生从控制灯光到制作音乐的酷效果。电路板、编程语言和你在网上找到的大多数项目都是开源的。这意味着您可以根据自己的需要编辑和使用它们。因为它是开源的、简单的，并且标价 25 美元，Arduino 已经成为创建和分享基于电子的 DIY 项目的首选工具。

Arduino 本身是一个物理板，通过 USB 电缆连接到您的电脑，并从您电脑上的应用程序下载代码。你可以在 Arduino 官方网站 上找到 Windows、Mac 和 Linux [的安装演练。该软件也称为 Arduino，是你编写自己的代码(或草图，Arduino 软件称之为草图)的地方。对于像我们这样的 Arduino 初学者来说，这是你从别人的项目中粘贴代码的地方。当您将代码从电脑发送到 Arduino 时，代码会存储在 Arduino 上。您可以随心所欲地从 Arduino 上传和删除代码。](http://arduino.cc/en/Guide/HomePage)

首先，我建议购买一个较大的入门包，这样您就有了运行大多数项目所需的所有不同的组件。[【Adafruit】的实验套件(＄85.00)](http://www.adafruit.com/products/170)或 [SparkFun 的发明家套件(＄94.95)](http://www.sparkfun.com/products/10173)都包括各种各样的零件和使用指南。除了那些你得到的东西，最好在身边放一个[【15】](http://www.adafruit.com/products/71)万用表来测试电气元件，一个 [烙铁(9.95 美元)](http://www.sparkfun.com/products/9507) 用焊料做电线连接。

### 很酷的 Arduino 项目，你可以用别人的代码完成

虽然你可以(最终)学会自己编写 Arduino 项目并让你的 Arduino 做几乎任何事情，但你也可以简单地借用已经可用的开源项目(这就是这个初露头角的 Arduino 用户所做的)。开始使用 Arduino 不需要编程知识。你只需要一点耐心。项目的复杂程度各不相同，但大多数都可以通过 Arduino 和计算机来完成。

作为一个初学者，这些项目中的许多似乎有点势不可挡，但我在 Luminch One(交互式灯)、amp mod 和 PC 环境灯光方面都尝试过，并取得了成功。由于我通常在太阳升起之前醒来，我的下一个项目是日出闹钟，这样我就可以顺利地起床。这里有一些简单的 Arduino 项目，你可以自己做，不需要编程经验。

*   [**关掉闲置的家庭影院功放**](http://www.instructables.com/id/Arduino-turns-off-idle-Amplifier/)) **:** 如果你和我一样，你总是在听完音乐或看完电影后开着功放。这个聪明的 Arduino hack 监控音量，并在不用时关闭放大器。
*   [**监控你电脑的热度**](http://www.roboteched.net/2011/10/arduino-based-computer-temp-sensing.html) **:** 你可以使用 [程序来监控你电脑的热度](http://lifehacker.com/how-to-prevent-your-computer-from-overheating-and-why-5570909) ，但是如果你正在寻找一种有趣而浮华的方式来告诉你发生了什么，这个项目使用 Arduino 来监控你机箱内的温度。如果太热，它就会亮，这样你就知道发生了什么。
*   [**日出闹钟**](http://blog.freesideatlanta.org/2011/09/sunrise-alarm-clock.html) **:** 被闹钟叫醒，不管你多么习惯。日出闹钟通过在闹钟响起之前用日出般的颜色和灯光温暖房间来解决这个问题。由于电缆的数量，这个看起来有点复杂，但只要你能跟踪所有的东西，它就出奇的简单。
*   [**Luminch One 波控灯**](http://makeprojects.com/Project/Luminch-One/1773/1)**:**Luminch One 是一款交互式灯，你可以通过挥动你的手来控制亮度。这个项目乍看起来相当复杂，但最大的困难是用轻木组装灯罩。
*   [**PC 环境照明**](http://siliconrepublic.blogspot.com/2011/02/arduino-based-pc-ambient-lighting.html) :给 PC 增加环境照明可以让你的视频观看体验格外爽。在你的电脑上使用一个 Arduino 和一点代码，它可以监控你的屏幕，并在你的显示器后面产生光线。在下一节，我们将带你了解 Rajarshi Roy 的项目。

### 为您自己的计算机构建 PC 环境照明

虽然许多人喜欢使用 Arduino 来实现他们自己的想法，但 Arduino 也可以作为一种工具来完成其他人已经完成了所有艰苦工作的项目。把 Arduino 想象成宜家盒子里的内六角扳手。你所要做的就是按照指示去做，你就会得到正确的结果。让我们来看看 PC 环境照明项目需要哪些零件。

**你需要的零件**

*   Arduino
*   [**13 根跳线(6 美元一包 75 根)**](http://www.adafruit.com/products/153) **:** 你已经知道什么是电线，但电线是让 Arduino 项目工作的面包和黄油。您使用电线将 Arduino 连接到试验板，并创建电路来实现一切通信。这就是为什么你会在电影中看到他们需要剪断电线来阻止炸弹爆炸。如果你切断一个连接，它可以停止整个系统的工作。
*   [**【RGB LED 条($15.95)**](http://www.sparkfun.com/products/10261) **:** 这是我们项目的核心。这个灯条将以和你的电脑屏幕相同的颜色点亮，让它看起来比实际的屏幕要大。单独的 LED 灯在 Arduino 项目中很常见，因为它们提供了电路工作的证据。
*   [**【烙铁和焊料(9.95 美元)**](http://www.sparkfun.com/products/9507) **:** 烙铁用于使用焊料在零件之间创建新的永久连接。一般来说，对于 Arduino 项目，除了将一根电线连接到另一根电线，你不需要做任何更复杂的事情。如果需要的话，你可以在这个项目中使用电工胶带，但是焊接总是更好的选择。
*   [**【试验板(5 美元)**](https://www.adafruit.com/products/64) **:** 试验板可以在不同的电子设备之间建立连接，而无需将它们焊接在一起。它由一个网格状的小孔组成，你可以在那里连接不同的组件。这些洞都像一个小水晶一样连在一起。在电路板的外侧，它们水平连接，这样电路板的一端与另一端相连。在内部，它们是垂直连接的。这使得一根电线可以向另一个组件发送信息，而不必物理连接它们。右边图片中的是我们实验用的迷你试验板，但是这个项目用常规尺寸的试验板更容易。
*   [**LED 电路驱动器(60 )**](http://search.digikey.com/us/en/products/ULN2003A/497-2344-5-ND/599603) **:** 电路驱动器用于代替复杂的电子代码。存在许多不同类型的电路，但在这个项目中，我们使用 LED 驱动器，因此它可以控制灯光，而不需要很多额外的工作。
*   [**12V DC 电源(5.95 美元)**](http://www.sparkfun.com/products/9442) **:** 这是你标准的 12V 电源。你甚至可以在你的房子周围放一个，用于这个项目。你可以在电源模块的背面或者在“输出”下面找到电压我们用它来直接给 led 供电，这就是为什么你不用把它连接到 Arduino 本身。
*   [**它是可选的，但是稍微简化了项目。**](http://www.sparkfun.com/products/10811)

#### 第 0 步:在你的电脑上安装 Arduino、Processing 和 Arduino 驱动程序

下载并安装 [处理](http://processing.org/download/) 和 [Arduino](http://arduino.cc/hu/Main/Software) 软件如果你还没有的话。您还需要下载 [Arduino 兼容的 USB 驱动程序](http://www.ftdichip.com/Drivers/VCP.htm) 以便您的机器可以正确地与 Arduino 接口。如果您在让软件工作时遇到问题，请参考 [Ladyada 的优秀指南](http://www.ladyada.net/learn/arduino/lesson0.html) 了解 Arduino 的初始设置过程。

#### 第一步:复制、粘贴并运行处理中的代码

在你的电脑上打开进程。从 Rajarshi Roy 的博客的 [中复制并粘贴处理代码(橙色文本)到处理中。点击草图>运行。这将在您的计算机屏幕上打开一个小窗口，显示当前屏幕上最突出的颜色，并最终将其导出到 Arduino。如果窗口没有在你的屏幕上打开，程序就没有运行。重复这些步骤，确保它正确地构建了脚本。](http://siliconrepublic.blogspot.com/2011/02/arduino-based-pc-ambient-lighting.html)

#### 第二步:复制、粘贴并运行 Arduino 中的代码

打开 Arduino 软件，将 Arduino 代码(帖子底部附近方框中的文本)粘贴到新的草图中。单击 Sketch > Verify / Compile 以确保代码正确存在。保存文件，然后用 USB 电缆将 Arduino 连接到您的电脑。单击文件>上传。现在软件方面一切都准备好了。现在，你可以把 Arduino 从电脑上断开，因为我们要把电路组装起来。

#### 第三步:将电路驱动器和 LED 灯条连接到试验板上

组装电路是最吓人的部分。谢天谢地，Rajarshi 给我们提供了一张 [的高分辨率图像，可以从](http://2.bp.blogspot.com/-AiWZXO2GXmA/Tqab-DytJGI/AAAAAAAAADw/e3G5IsKq5VY/s1600/DSC_0108.JPG) 复制。如果图片对您来说仍然很混乱，我们已经对其进行了进一步简化。您可以单击右边的图像将其放大，以便于理解要做的事情。

首先将电路驱动器连接到你的试验板的中心，这将是你其他一切的参考点。接下来，我们将通过一些非常轻的焊接来为 LED 灯条打底。用一个烙铁，四根跨接电缆，和 LED 条， [按照本教程将跨接导线焊接并连接到 LED 条](http://www.ladyada.net/products/rgbledstrip/) 。如果你不喜欢焊接，我已经成功地用电工胶带连接电线和 LED 灯条，但这不是一个永久的解决方案。

#### 第四步:连接所有剩余的电缆

连接所有剩余的电缆，就像你在 Rajarshi 的图片中看到的那样。你只需要建立九个连接，但如果你很难保持跟踪，从左到右工作。如果你有一个 [类似图片](https://www.adafruit.com/products/64) 的试验板，那是最简单的，但这不是必需的。只要确保你的电缆像图片一样水平和垂直排列。

#### 第五步:连接电源和 DC 桶形插孔适配器

12V 电源适配器插在左上角。我们将插入 DC 桶形插孔适配器，而不是像图中那样拼接电缆，这样我们就不必担心切断电源。将插孔适配器卡入我们图表上的相同位置。然后插上电源。

如果你想让你的设置和 Rajarshi 的教程一样，你需要切断电源的适配器端，用美工刀或断线钳将塑料剥去一点，然后将其连接到一个 [端子，就像这个](http://www.sparkfun.com/products/8073) 。如果你在裁剪部分有困难， [这段视频将带你完成这个过程](http://www.ehow.co.uk/video_2372471_strip-cut-wire-circuit-bending.html) 。

#### 第六步:将 Arduino 插入电脑，运行处理和测试

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-Am55k0k9eq8&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-Am55k0k9eq8&start=0) 

将试验板连接到 Arduino，并将电源插入插座，然后使用 USB 电缆将 Arduino 插回电脑。接下来，运行我们之前编译的处理代码。Arduino 上的 led 应该会亮起，以反映您电脑的颜色。关掉灯，放一部电影，享受你的 DIY 环境照明。

#### 解决纷争

如果有些事情不正常，Rajarshi 博客上的评论区有来自其他黑客和 Rajarshi 自己的各种各样的解决方案。Rajarshi 还为您可能遇到的常见问题添加了一些注释(链接已添加):

> 要检查 LED 灯条和电源是否工作，请将电源的+12V 直接连接到灯条的+12V 引脚，并将电源的接地一次连接到每个 R、G、B 引脚，以查看它们是否亮起。
> 
> 要检查 Arduino 是否在其内存中保留了闪烁代码，请确保在断开连接并重新接通电源后，简单的 LED 闪烁代码仍然有效。
> 
> 如果您看到处理代码运行并且框中的颜色正确变化，那么它就可以工作(当然是在连接了 Arduino 的情况下)。如果没有，请更改代码中的串行端口号。如果还是不行， [检查你的 Java 安装](http://www.java.com/en/download/help/download_options.xml) 。
> 
> 如果以上都有效，那一定是你的人脉。

### 进一步阅读和资料来源

带领你完成一个简单的项目并不足以让你掌握 Arduino 能做的一切。这里有一些我们最喜欢的教程、商店和论坛，你可以向它们寻求帮助。

*   [**Ladyada 的 Arduino 教程**](http://www.ladyada.net/learn/arduino/index.html) **:** 对我来说，这是入门我的 Arduino 的最好教程。这是一个简单的线性教程，让你熟悉 Arduino 的基本功能。它引导你完成这个过程，使灯光发光，声音嗡嗡作响，部件摆动。
*   [**官方 Arduino 示例教程**](http://arduino.cc/en/Tutorial/HomePage)**:**Arduino 计算机软件加载了大量示例，供您在自己的代码中使用或作为学习体验来运行。官方网站会带你浏览软件初始下载时包含的每一个例子。如果您看到一个名字很吸引人的例子，比如 tonePitchFollower，并且想自己测试一下，那么这就很棒了。
*   [**Instructables ' Arduino Section**](http://www.instructables.com/tag/type-id/category-technology/channel-arduino/)**:**Instructables ' Arduino Section 对项目的新想法已经成熟。如果您想了解其他人使用 Arduino 的项目类型或寻找新项目，这非常有用。
*   [**Make Magazine 的 Arduino 版块**](http://makezine.com/arduino/)**:**Make Magazine 的 Arduino 版块是新项目、说明、指南和教程的巨大资源。这是 Arduino 初学者和专家的最佳一站式位置。
*   [**阿达果实业**](http://www.adafruit.com/) **:** 阿达果实业是 Ladyada 开的店，上面链接了他的教程。这是一个很棒的商店，几乎可以找到你需要的任何零件。这也是访问论坛分享或寻求项目帮助的好地方。
*   [**Sparkfun 电子**](http://www.sparkfun.com/) **:** 我从 SparkFun Industries 订购的运气最好，但这可能部分是因为他们和我在同一个州。无论如何，他们很快，愿意帮助找到特定的零件，并有一些零件很难在其他地方找到。
*   [**官方论坛**](http://www.arduino.cc/cgi-bin/yabb2/YaBB.pl) **:** 当你对一个项目有疑问或者需要帮助来完成某项工作时，官方论坛是最好的求助场所。这里有很多乐于助人的人，他们可以评论你的代码，并指导你解决你在具体项目中可能遇到的问题。

* * *

当你第一眼看到 Arduino 项目时，它完全是一片混乱，但是放慢进度会发现它其实是多么简单。当你完成第一个教程时，你已经对基础知识有了坚实的理解，最终你可以进入更复杂的项目。在我使用 Arduino 的短暂经历中，我发现学习曲线并不像最初看起来那样陡峭。到目前为止，我只做了五六个项目(完成两倍的项目都失败了)，但是我现在对基础的东西很满意。每完成一个项目后，我都更接近于降低退出率，希望它最终会完全消失。

你有没有用别人的代码或者你自己的代码完成过任何你自己的 Arduino 项目，简单的或者复杂的？在评论里听听吧。