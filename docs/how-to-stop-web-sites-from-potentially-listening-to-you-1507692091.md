# 如何阻止网站监听您的麦克风

> 原文:[https://life hacker . com/how-to-stop-websites-from-potential-listing-to-you-1507692091](https://lifehacker.com/how-to-stop-web-sites-from-potentially-listening-to-you-1507692091)

本周早些时候，网络开发者 [Tal Ater 警告 Chrome 的一个漏洞](http://talater.com/chrome-is-listening/) 将允许一个不道德的网站在你说话时监听你电脑的麦克风。谷歌驳回了这个问题，但是如果你想知道整件事对你来说意味着什么，这里有一些你可以保护自己的方法。

Watch

### 这是怎么回事？

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-s5D578JmHdU&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-s5D578JmHdU&start=0) 

这是真相。一旦你允许一个网站使用你的麦克风或摄像头，Chrome 就认为这个网站在将来会被允许这样做。这意味着该网站的每个实例，该网站上的每个页面，也可以访问您的摄像头和麦克风，这意味着一个粗略的网站所有者可以在后台弹出一个弹出式窗口，监听您所说的一切，或者更糟的是，监听并设置为在您说出特定单词或短语时触发一些操作(如录音)。

之后 [九月](http://www.theverge.com/2014/1/21/5332316/chrome-exploit-lets-websites-keep-listening-after-you-close-the-tab) 向谷歌报告。对谷歌来说， [并不认为这是一个问题](http://www.computerworld.com/s/article/9245650/Google_dismisses_eavesdropping_threat_in_Chrome) ，并表示这符合 W3C(万维网联盟)的标准。谷歌确实有一个观点:为了让这个问题成为一个真正的威胁，你不仅必须访问一个想要记录你讲话的网站，你还必须允许它访问你的麦克风，然后*然后*你必须注意不到那个网站的一个弹出窗口在后台徘徊。另外，您还必须注意到指示麦克风处于活动状态的视觉提示(omnibar 中的红点)。即便如此，谷歌的工程师*确实*对 Ater 的报告做出了回应，*确实*提出了解决这个问题的修复方案，但是——这是令人困惑的部分——*没有*向最终用户推出那个修复方案。

### 你如何保护自己

那么这给你留下了什么？简而言之，离你出发的地方不远。Chrome 的问题是，Ater 和其他安全专家坚持认为它可能被利用，你可能永远也不会知道。尽管争论仍在继续，但你可以在 Chrome 中查看你允许访问你的麦克风和摄像头的网站。不难。方法如下:

1.  打开 chrome，在 Omnibar 中键入**chrome://settings/content exceptions # media-stream**。
2.  您将看到“媒体例外”屏幕，在这里您可以看到哪些主机名对您的麦克风和摄像机有权限，以及每个站点可以访问这两者中的哪一个。
3.  突出显示您想要删除的任何站点，然后单击该行右侧的“x”。
4.  单击完成保存您的更改。

[PCWorld 还注意到](http://www.pcworld.com/article/2090083/chrome-exploit-can-secretly-listen-to-oblivious-users.html) 如果你喜欢，你可以直接进入:**chrome://settings/content**向下滚动到 Media，而不是“当一个网站想使用插件访问我的摄像头和麦克风时问我”(这是默认设置)，选择“不允许任何网站访问我的摄像头和麦克风”，这是一种核心选项。这样做还会禁用谷歌的对话式搜索等功能，这些功能可能非常有用，可能会中断与 Google Now(随时会在 Chrome 中推出)的任何语音集成，并禁用 Chrome 或网络上其他地方的任何其他语音激活功能。

值得注意的是，这些设置与使用 Adobe Flash 访问您的摄像头或麦克风的网站不同。上面的媒体例外屏幕有一个链接，您可以在那里更改这些设置并查看对您的硬件有权限的站点，但您可以在这里 获得 [。虽然大多数网站*应该*设置为“总是询问”才可以做任何事情，所以任何真正的威胁都会减少，但这个列表可能会更有趣一点。](http://www.macromedia.com/support/documentation/en/flashplayer/help/settings_manager06.html)

关于这是否是一种真正的威胁以及这种威胁有多大的辩论可能会持续数周，直到它平息下来，或者谷歌决定为 Chrome 添加一些权宜之计来解决这一问题，但这些问题随着语音命令和交互控制在我们的手机和电脑上变得司空见惯而出现。虽然专家们对其中的细微差别争论不休，但至少这些提示可以让你在需要的时候管理好自己的安全。

*<small>标题照片制作使用</small>* [*<small>荣和乔</small>*](http://www.shutterstock.com/pic.mhtml?id=136353821&src=id)*<small>(Shutterstock)。</small>T15】*