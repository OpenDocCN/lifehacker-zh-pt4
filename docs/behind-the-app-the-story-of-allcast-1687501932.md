# 应用背后:AllCast 的故事

> 原文：<https://lifehacker.com/behind-the-app-the-story-of-allcast-1687501932>

你上一次刻录 DVD 以便在电视上看视频是什么时候？或者在客厅的地毯上放一台笔记本电脑，电缆散落一地，这样你就可以在大屏幕上看视频了？多亏了像 [AllCast](http://www.allcast.io/) 这样的应用，这一切都变得过时了。

Watch

近年来，随着 Chromecast 或 Roku 等低成本设备成为媒体柜中的常见产品，我们可以轻松地将媒体从一个设备传输到另一个设备。由 Android 开发者 Koushik Dutta 创建的 AllCast 是一个简单的解决方案，用于将媒体从 Android 设备“播放”到 Chromecasts，并为更广泛的实施而发展。

十几年前，我记得我小心翼翼地对 MPEG 视频进行编码，这样我就可以在我破解的 Dreamcast 上播放它们；也许不值得这么麻烦，但当没有简单的方法将电脑连接到电视时，在电视上看到我的视频有一种神奇的感觉。当然，利用大屏幕的简单满足感现在比以往任何时候都容易，我不认为我的 Dreamcast 对兼容 AllCast 的设备构成太大威胁。我们采访了 Koushik，以了解他决定创建 AllCast 的方式和原因，以及他对未来的规划。

#### 这款应用的创意来自哪里？你是在试图解决你经历过的问题，还是灵感来自其他地方？

这个想法已经流传了一段时间；Android 上没有明显的 AirPlay 版本。当 Chromecast 发布时，他们提供了一个 SDK，这成为了一种真正的可能性。Chromecast 是第一款大举进军 Android 用户生态系统的设备。

#### 你想出这个主意后，下一步是什么？

当 Chromecast 团队决定关闭一些未记录的 API，以允许开发人员绕过测试版 API 锁定时，我开始研究其他解决方案。那是在 2013 年年中，支持[【DLNA】](http://en.wikipedia.org/wiki/Digital_Living_Network_Alliance)选角的智能电视开始变得越来越普遍。我发现 Xboxes 也支持 DLNA。同时，Roku 也推出了自己的铸造方案。我意识到这是一个制作一体化演播解决方案的机会:用户不关心电视上连接了什么，他们只想在电视上播放他们的媒体。它是如何工作的只是一个细节。

#### 你如何选择目标平台，忽略或等待哪些平台？

我选择 Android 和 Chromecast 作为我的主要移动/cast 平台。Android 是我现有的用户群，Chromecast 的销量高达数百万。Chromecast 最初迟迟没有为独立开发者发布最终的 API，是因为我转向了其他目标。我没有选择忽略 iOS，而是确保我提供了可靠的体验——我从未做过任何 iOS 开发。iOS 人群更有眼光。如果我自己做，我很可能会搞砸它，所以我带了 [杰克逊哈珀](https://twitter.com/jacksonh) 到 [建造那个](https://lifehacker.com/allcast-streams-tons-of-media-content-from-ios-to-your-1679233191) 。

#### Chromecast 花了一段时间才真正与独立开发者友好相处。你认为他们只是没有预料到人们想要制作自己的软件的热情，并且觉得维护一个有围墙的花园更安全吗？

我认为两者都有一点。从我和他们的聊天中，他们肯定对这款设备的巨大成功感到措手不及。但我也认为，谷歌内部有一些企业想独享这些玩具。

#### 你最大的障碍是什么，你是如何克服的？

迄今为止，最困难的部分是学习如何处理用户的家庭网络。奇怪的路由器配置会阻止发现。糟糕的 Wi-Fi 硬件可能会阻止从手机上播放高清视频——而现在手机有令人难以置信的摄像头。安卓上高清视频 20Mbps。许多 Wi-Fi 网络，取决于与其他网络的拥塞和许多其他因素，只能支持 3-4Mbps。有相当多的人只是使用由他们的 ISP 如康卡斯特等提供的劣质 Wi-Fi 路由器。

#### 对你来说，发射是什么样的？

安卓发布会太疯狂了。在发布之前，我做了一个“非正式的”测试，最终有 30，000 多名测试者。每当我做一个原型/测试版/发布版，似乎每个主要的技术网站都会报道它。科技网站似乎也喜欢 Chromecast 团队停止使用未记录的 API 的故事。

#### 你如何有效地处理用户的要求和批评？

我实际上已经不再看评论和邮件了。不健康哈。燕麦片在“ [制造东西](http://theoatmeal.com/comics/making_things) ”上做的漫画有一个面板总结道:

我请了我的老朋友雷·沃尔特斯来处理这类支持问题。

#### 现在，如何在开发新功能和管理现有功能之间分配时间？

Ray 将错误报告和特性请求提炼成可用的反馈，并让我知道是否有很多用户在抱怨某个特定的痛点。我没有一个过程本身。我认为可能 25%的时间花在 bug 上，75%的时间花在特性上。

#### 除了简单地增加对更多设备的支持，你希望在 AllCast 更广阔的未来看到什么？

我有两个不同的想法，但是我还没准备好讨论它们。一个是在原型阶段，另一个是涉及硬件的更大的努力(不，它不是一个 AllCast 棒)。

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-5k_NLVrbxss&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-5k_NLVrbxss&start=0) 

#### 你会给那些想从事类似项目的人什么建议？

我以前在其他地方说过:通过攻击通常不值得一个小型工程团队花费时间的项目，有很多机会赚到六位数的薪水。一个拥有广泛技能的人可以经济地解决这个问题。

* * *

<small></small>*[<small>*App 背后*</small>](http://lifehacker.com/behindtheapp) <small>*让我们深入了解一些我们最喜欢的应用是如何诞生的——从创意到发布(以及之后)。有你想看到的人吗？邮箱*</small> [<small>*安迪*</small>](mailto:andy@lifehacker.com) <small>*。*</small>*

**<small>插画由</small>* [*<small>燕麦片</small>*](http://theoatmeal.com/comics/making_things) *<small>。</small>T15】**