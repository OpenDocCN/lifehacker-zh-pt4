# 为什么苹果最近的安全漏洞如此可怕

> 原文:[https://gizmodo . com/why-apple-huge-security-flaw-is-so-terrible-1529041062](https://gizmodo.com/why-apples-huge-security-flaw-is-so-scary-1529041062)

周五，苹果悄悄发布了 iOS 7.0.6，在一份简短的发布说明中解释说，它修复了一个漏洞，即“具有特权网络地位的攻击者可能会在受 SSL/TLS 保护的会话中捕获或修改数据。”那是低调的版本。换种说法？现在就更新你的 iPhone*。*

*Watch*

*哦，顺便说一下， [OS X 也有同样的问题](http://www.crowdstrike.com/blog/details-about-apple-ssl-vulnerability-and-ios-706-patch/index.html)——只是还没有解决。*

***更新，2014 年 2 月 25 日:**苹果刚刚发布了 OS X 10.9.2，修补了下述安全漏洞。现在就去 App Store 下载吧，最好是通过安全网络。*

*如果你完全理解那个发行说明的意思，你很可能是第一个获得 iOS 更新的人。如果它读起来像是从*运动鞋*中删除的场景，那么这对你和你的苹果设备意味着什么。*

### *什么是 SSL？*

*SSL 代表安全套接字层，它有助于确保您的浏览器和您最喜爱的网站的服务器之间的通信保持隐私和安全。TLS，即传输层安全性，是一个更新的协议，本质上也是如此。简而言之，SSL/TLS 是一种加密密钥，让浏览器和服务器知道他们是他们所说的人，这是一种秘密的数字握手，当你在亚马逊支付或登录 wellsfargo.com 时，它可以保护你的财务信息安全。*

*这一切都发生在后台；您与 SSL/TLS 的唯一直接交互是当您注意到搜索栏中的锁图标已经关闭时。这意味着你有一个直接的，私人的，安全的线路。*

*问题中的苹果漏洞——同样，已经在 iOS 中得到修补，但在 OS X 尚未得到修补，尽管 [苹果告诉路透社](http://www.reuters.com/article/2014/02/22/us-apple-encryption-idUSBREA1L10220140222) “很快”就会修复——这意味着 Safari 或 [这些其他受影响的应用程序之一](https://gizmodo.com/the-os-x-apps-affected-by-apples-unpatched-security-fl-1529152561) 实际上无法确定它正在与之对话的服务器是否是他们所说的人。这使得你和你在网上传输的任何东西都容易受到中间人的攻击。*

### *什么是中路进攻的人？*

*中间人攻击，为了简洁起见，我们在这里称之为 MitM，基本上是高科技窃听。在这种情况下，共享网络上的 MitM 攻击者拦截您的浏览器和某个站点之间的通信，监视、记录、查看你们之间发生的一切。*

*Gmail。脸书。金融交易。好吧丘比特调情。所有这些都是由一个完全陌生的人实时阅读的。这是一张非常简单的图表:*

*通常像这样的攻击会被 SSL/TLS 挫败(加密的握手很难被打断)，或者至少变得太困难而不值得。但是这个苹果臭虫让它变得非常容易。发行说明中提到的攻击者需要处于的“特权网络位置”？它是任何公共网络。那只能说明他和你在同一个星巴克。*

*这种情况从 9 月份就开始了。 [*2012*](https://twitter.com/Jeffrey903/status/437273379855667201) 。*

### *有多严重？*

*如果您还在为这一切意味着什么以及它有多糟糕而挠头，最简单的解释方式是，深刻理解它的开发人员甚至不愿意公开谈论它，因为他们害怕给黑客更多的弹药:*

 *[https://gizmodo.com/embed/inset/iframe?id=twitter-437000491663630336&autosize=1](https://gizmodo.com/embed/inset/iframe?id=twitter-437000491663630336&autosize=1)*  *[https://gizmodo.com/embed/inset/iframe?id=twitter-437072656186478592&autosize=1](https://gizmodo.com/embed/inset/iframe?id=twitter-437072656186478592&autosize=1)*  *[https://gizmodo.com/embed/inset/iframe?id=twitter-437333111861309440&autosize=1](https://gizmodo.com/embed/inset/iframe?id=twitter-437333111861309440&autosize=1)*  *[https://gizmodo.com/embed/inset/iframe?id=twitter-437357549227360257&autosize=1](https://gizmodo.com/embed/inset/iframe?id=twitter-437357549227360257&autosize=1)* 

*约翰·霍普金斯大学的密码学教授马修·格林也在 [向路透社](http://www.reuters.com/article/2014/02/22/us-apple-flaw-idUSBREA1L01Y20140222) 解释说，这是“你能想象到的最糟糕的情况，我只能这么说。”所以你走吧！*

*你可以深呼吸一下。您的受密码保护的家庭网络是安全的；显然不是每个咖啡店都潜伏着黑客；你的个人信息对别人来说从来没有你想象的那么有趣。如果你已经把你的 iPhone 或 iPad 升级到 7.0.6，你就没事了。*

*但是知道这种情况已经持续了一年半，仅仅从原则上来说就很麻烦了。而且知道它已经被广泛宣传，还没有为 MacBooks 修复，这意味着它值得采取一些额外的预防措施。*

### *这是怎么发生的？*

*没人知道，苹果也没说，这可以理解。但是各种理论从似是而非到戴着锡箔帽。让我们从可能发生的事情开始，一步步来。*

*谷歌的亚当·兰利在他的个人博客 中详细描述了这个漏洞的细节，如果你想盯着一些代码看的话。但本质上，它归结为近 2000 条线中的一条简单的额外线。正如 [ZDNet 指出的](http://www.zdnet.com/apple-and-the-ssltls-bug-open-questions-7000026628/) ，多一个“goto fail 语句放在大约三分之一处意味着 SSL 验证几乎在所有情况下都会通过，不管密钥是否匹配。*

*兰利的观点，最可信的是？它可能发生在任何人身上:*

> *这种隐藏在代码深处的细微错误简直是一场噩梦。我相信这只是一个错误，我为任何可能使用编辑器创建它的人感到难过。*

*不过，这并不需要太多的想象力，就能在这个漏洞和国家安全局的棱镜计划之间划出几条不确定的界限。就在昨天晚上，约翰·格鲁伯,指出“goto 失败”command 首先潜入了 iOS 6.0，据报道，在苹果被加入间谍机构的 [信息窥探棱镜计划](https://gizmodo.com/the-nsa-and-fbi-have-been-spying-on-our-internet-habits-511750202) 之前一个月，iOS 6.0 才发布。*

*如果你想在这个时间基础上实现完整的锡纸帽，欢迎你，但这不太可能是苹果故意添加的这段代码。不过，完全有可能，美国国家安全局在苹果之前发现了它，并一直在秘密利用它来达到棱镜的目的。*

### *我该如何预防？*

*如果你在 iOS 设备上，你需要立即下载 7.0.6。如果你有 3GS 或者旧的 iPod touch，你可以下载 iOS 6.1.6。如果你想知道苹果对此有多认真，他们支持一个他们非常渴望淘汰的 iOS 版本的事实应该是一个很好的指标。*

*不过，到目前为止，如果你在 OS X 上，你就没那么幸运了。漏洞仍然存在，而且现在它已经被广泛宣传，坏人会热衷于利用他们可以利用的机会。有一个非官方的补丁，但请知道这不是为初学者。*

*与此同时，你最好的选择是使用 Chrome 或 Firefox，它们在 OS X 上不会受到影响。还要确保你呆在安全的网络上，如果你真的在共享网络上，那就聪明点(没有财务信息，没有交易，没有个人信息)。一般来说，这是一个很好的经验法则，但在这一点得到正确解决之前尤其重要。*

*让我们都希望“很快”修复是指几小时或几天，而不是几周。*

***更新:**关于 OS X 更新的时间，苹果发言人告诉我们如下:*

> *“我们已经意识到了这个问题，并且已经有了一个软件补丁，很快就会发布。”*

*这与路透社之前的报道相呼应，但也给人一些即将发布的希望。*

**顶级镜像功劳:* [*推特*](https://twitter.com/christinagignac)*

**连同图表:*[*【wiki common】*](http://commons.wikimedia.org/wiki/File:Man_in_the_middle_attack.svg)*/*[*【miraceti】*](http://commons.wikimedia.org/wiki/User:Miraceti)*