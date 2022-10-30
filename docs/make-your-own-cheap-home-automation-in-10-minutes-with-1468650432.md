# 用忍者积木在 10 分钟内构建一个廉价的家庭自动化系统

> 原文:[https://life hacker . com/make-your-own-buy-home-automation-in-1468650432](https://lifehacker.com/make-your-own-cheap-home-automation-in-10-minutes-with-1468650432)

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-BR7yjXuP_eg&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-BR7yjXuP_eg&start=0) 

家庭安全和自动化很少与廉价这个词在同一个句子中被提及，但如果你愿意自己做一些事情，这是完全可能的。我们检查了一个名为 [忍者积木](http://ninjablocks.com/collections/ninja-blocks/products/ninja-blocks-kit) 的 200 美元的 DIY 套件，并且能够在大约 10 分钟内安装并运行一个家庭自动化和安全系统。

Watch

### 你会得到什么

Ninja Blocks 是一个开源的家庭自动化系统，允许您将各种传感器连接到互联网。忍者块本质上是家庭自动化系统背后的大脑，你可以轻松地将传感器和外围设备连接到它。基本上，忍者块是物质世界的一种 [如果这个那么那个](https://lifehacker.com/how-to-supercharge-all-your-favorite-webapps-with-ifttt-5842307) 。在某种程度上，他们类似于 [贝尔金 WeMo](http://lifehacker.com/belkin-wemo-is-one-of-the-simplest-home-automation-solu-5921253) ，但是忍者块有更多的触发选项，如果你已经有一个 WeMo，也支持 WeMo。

一切设置完成后，您所有的小工具和家庭显示器都将连接到互联网，并可从您的智能手机或 PC 上看到。你将能够监控家中的温度，开灯，检查网络摄像头，切换运动传感器，以及几乎任何你能想到的关于家庭安全或自动化的事情。如果你有任何带有传感器、致动器或使用射频信号或 Wi-Fi 的小工具，你可以将其连接到忍者块。你甚至可以用你自己的 [Arduino，Raspberry Pi，或者 BeagleBone 项目](https://lifehacker.com/how-to-pick-the-right-electronics-board-for-your-diy-pr-742869540) 来添加。

您还可以设置一系列在特定时间采取行动的规则。例如，您可以让插座在一天中的特定时间打开，或者让传感器在检测到移动时向您发送短信。忍者积木的与众不同之处在于，你不需要太多的专业技术就能完成这项工作:无论你是谁，它都非常容易安装。

### 你需要什么

我们决定让事情变得简单，使用了[【199 美元忍者积木入门套件](http://ninjablocks.com/collections/ninja-blocks/products/ninja-blocks-kit) 。该套件包括:

*   一个无线运动传感器。
*   一个无线门窗接触传感器。
*   一个无线按钮。
*   一个无线温度和湿度传感器。
*   一个 Ninja Block (BeagleBone 黑色 Linux 计算机，带 Arduino)。
*   一根以太网电缆。
*   一个 5v 直流 3 安培电源，带连接器，适用于美国、欧盟、英国和澳大利亚。
*   一个温度探头

然而，硬件是开源的，所以你也可以自己制作工具包。例如，如果你已经有一个树莓派，你可以购买 49 美元的 [忍者派外壳](http://ninjablocks.com/products/ninja-pi-crust) 来添加忍者块功能，或者 [根据你的需要单独购买任何传感器或按钮](http://ninjablocks.com/collections/all) 。同样，你甚至可以用 [Ninja Block 分线板](http://ninjablocks.com/collections/all/products/ninja-breakout-kit) 制作你的传感器，或者跳过这一切，用 Ninja Block 的开源原理图和软件 [制作你自己的系统](http://ninjablocks.com/pages/open-source) 。

### 第一步:设置你的忍者区块

首先，你需要设置你的忍者块。这是一个非常简单的过程:

1.  打开 Ninja Block 外壳，记下以太网连接器旁边的序列号。
2.  关闭模块，用以太网电缆将其插入无线路由器，然后插入电源线。等待它启动并加载软件。这个过程第一次大约需要五分钟。完成后忍者眼睛上的状态灯会变成紫色。
3.  前往你的电脑，通过前往来配对你的忍者块。使用您的电子邮件和密码登录。
4.  选择设置描述文件下的“块”，然后“配对另一个块”
5.  输入你在第一步中记下的序列号。
6.  最后，单击“设置 WiFi”按钮，并输入您的本地网络名称和密码。Ninja 块将重置，然后您可以将其从以太网电缆上断开。

就初始设置而言，你的忍者块现在已经启动并运行了。

### 第二步:设置你的传感器

现在是时候把所有这些传感器连接到忍者块上了。Ninja Block 套件附带的四个传感器(温度/湿度传感器、运动传感器、接近传感器和按钮)已经设置为与 Ninja Block 配合使用，因此连接它们非常容易。事实上，你真正要做的就是安装一个电池，给你的传感器命名，并把它们放在你房子的周围。

套件中包含的每个传感器都需要一个电池，一旦安装了电池，它就会自动连接到您的忍者块。温度传感器将在通电后自动连接到 Ninja Block，并开始显示温度，但您需要标记其余的传感器:

1.  前往仪表板上你的忍者区块:。
2.  您的传感器应在“保存的传感器”下列为 1、2、3。单击每个标签旁边的钢笔图标来标记它们。如果您不确定哪个传感器是哪个，请激活传感器(移动到运动传感器前面，移动接近传感器，或单击按钮)，然后等待通知在您的仪表板上弹出。

当然，Ninja Blocks 支持的设备远不止初学者工具包中的那些。你可以加上 [遥控电源插座，灯，发光二极管，还有更多的](http://ninjablocks.com/collections/connected-devices) 。一旦你的传感器连接到你的忍者块，是时候真正用它们做点什么了。

### 第三步:建立你的规则

忍者块的酷之处在于，你可以用你的传感器设置一系列因果规则。这些规则非常简单:如果一个传感器被触发，那么一个动作就会发生。这个动作通常是打开网络摄像头、发送短信或开灯。它们的设置非常简单:

1.  前往忍者格挡 上的 [规则标签。](https://a.ninja.is/ruling)
2.  选择要制定规则的传感器，然后单击“下一步”
3.  单击您想要的结果(文本消息、切换、网络摄像头等)。
4.  命名您的规则，然后单击“完成”

要获得更多关于你的 Ninja Block 可以做什么的选项，请前往 Ninja Block 上的“设置”>“偏好设置”,然后登录 Twitter、Dropbox、Twilio 等服务。这使得你的传感器可以做一些事情，如发推文，发送电子邮件，给你发短信，或上传图片(如果你有网络摄像头)。你也可以让传感器做多种动作。例如，您可以为家庭安全设置两条规则:一条是当感应到运动时您会收到一条短信，另一条是运动传感器也会触发网络摄像头拍照。

你能用规则做什么真的取决于你自己。如果你有你的灯和加热器连接到你的忍者块，你可以设置它，这样当你到家时一切都打开了。或者，你可以设置一个运动传感器，在你洗衣服的时候提醒你。见鬼，你甚至可以设置它，让你的 [灯在黄昏](http://forums.ninjablocks.com/index.php?p=/discussion/1973/sunset-timings-for-lighting) 时打开。我推荐去看看 [忍者街区论坛](http://forums.ninjablocks.com/) 寻找灵感。

### 第四步:设置你的智能手机应用

有了忍者团，你还可以获得安卓 和 iOS 的 [和](https://play.google.com/store/apps/details?id=com.ninjablocks.remote) [应用。这些应用程序可以从任何地方控制你的任何继电器、电源开关、传感器、灯或任何其他连接到你的忍者块的东西。你所需要做的就是下载并登录。](https://itunes.apple.com/en/app/the-ninja-remote/id645792957)

安装该应用后，您可以在此处创建中继规则。只需点击右上角的笔按钮，就可以在遥控器上添加一个按钮来转动任何开关或激活任何动作。此外， [主仪表板也是移动友好的](https://a.ninja.is/home) ，如果你想监控你的家。

### 额外资源

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-cedbZiTv0hk&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-cedbZiTv0hk&start=0) 

我们只是简单介绍了忍者积木的基本功能。事实是，事情不会变得真正有趣，直到你开始自己动手修改它。我们没有时间或空间来考虑每一种可能性，但是因为忍者块是开源的，而且非常容易使用，所以有很多黑客可以扩展你的忍者块的功能。以下是一些我们认为有用的指南、提示和资源:

*   [忍者街区论坛](http://ninjablocks.com/pages/forum)
*   [如何连接 433Mhz 设备](http://help.ninjablocks.com/customer/portal/articles/687137-how-do-i-connect-433mhz-devices-) 和这个 l [ist 的兼容设备](http://help.ninjablocks.com/customer/portal/articles/692139-what-rf-devices-can-my-ninja-block-talk-to-)
*   [开发自己应用的文档](http://ninjablocks.com/pages/developers)
*   [创建一个简单的基于房间的家庭安全系统](http://ninjablocks.com/collections/apps/products/security-app)
*   [忍者格挡帮助页面](http://help.ninjablocks.com/)

对于家庭自动化 ，你有一大堆 [选项，但我喜欢忍者积木的是，一切都很好。家庭自动化和安全一直是那些令人生畏的事情之一，似乎超出了我的知识范围(和成本)，但忍者块使初学者很容易，同时仍然保持专家可以修补的开源系统。最棒的是，专家们可以分享他们的应用程序和设置，这样即使是我们这些业余爱好者也可以从这个 DIY 解决方案中受益。目前可用的套件做了很多，但 2014 年 6 月的](https://lifehacker.com/how-can-i-get-started-with-home-automation-510246491) [新版本正在路上](http://www.kickstarter.com/projects/ninja/ninja-sphere-next-generation-control-of-your-envir) 增加了对蓝牙、XBMC、Pebble 等的支持。

<small>*音乐由*</small>[<small></small>](http://freemusicarchive.org/music/The_Itchy_Creeps/The_Itchy_Creeps/Itchy_Creeps_-_01_-_Hall_Of_The_Mountain_King)*<small>*。*T15】</small>*