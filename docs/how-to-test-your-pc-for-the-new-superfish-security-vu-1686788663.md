# 如何测试你的电脑是否存在新的“超级鱼”安全漏洞

> 原文:[https://life hacker . com/how-to-test-your-PC-for-the-new-super fish-security-vu-1686788663](https://lifehacker.com/how-to-test-your-pc-for-the-new-superfish-security-vu-1686788663)

安全研究人员在一款名为超级鱼 的 [广告软件中发现了一个漏洞，使得你的电脑容易受到各种攻击。Superfish 预装在许多联想电脑上，但也可以安装在*的任何*机器上。这是怎么回事，以及如何测试你是否被感染。](https://gizmodo.com/lenovo-installs-adware-on-new-computers-that-could-stea-1686721226)

Watch

### 什么是超级鱼

Superfish 基本上就是你的 [一般的广告软件](https://lifehacker.com/the-complete-guide-to-avoiding-and-removing-windows-c-1630577558) ，但是有一些很大的安全漏洞。联想在 2014 年[10 月至 2014 年](http://news.lenovo.com/article_display.cfm?article_id=1929)12 月期间销售的部分电脑上预装，但任何 Windows 电脑都可以感染。其核心是，Superfish 的目的是在你的网络浏览器中放置广告。问题是，该软件还会拦截加密流量，这会让你的计算机受到 [中间人攻击](http://en.wikipedia.org/wiki/Man-in-the-middle_attack) (其工作原理类似于去年 的 [Heartbleed 安全漏洞)。](http://lifehacker.com/what-the-heartbleed-security-bug-means-for-you-1560801201)

不仅如此，超级鱼还拦截 HTTPS 连接。勘误表安全 上的一个 [帖子显示，HTTPS 证书非常容易被破解，这让你更加脆弱。例如，安全研究](http://blog.erratasec.com/2015/02/extracting-superfish-certificate.html#.VOXzvLDF9K5) [克里斯·帕尔默发现，当他在安装了 Superfish 的电脑上访问美国银行的网站时，该银行的证书是由 Superfish 而不是 VeriSign 签署的。这意味着攻击者可以使用该证书创建假冒的 HTTPS 网站来获取您的密码，甚至创建“签名”后看起来合法的病毒。**更新:**联想在这里](http://arstechnica.com/security/2015/02/lenovo-pcs-ship-with-man-in-the-middle-adware-that-breaks-https-connections/) 发布了一份受影响机器的 [列表，但还是值得按照下面的说明进行仔细检查。](http://news.lenovo.com/article_display.cfm?article_id=1929)

### 如何测试您的计算机并删除 Superfish 软件和证书

令人欣慰的是，很容易测试你的电脑是否受到超级鱼的影响。我们有几台联想电脑进行测试，我们的电脑都很清晰，但测试你的电脑只需要一秒钟，所以不管你用的是什么类型的 Windows 电脑，测试都是值得的。不过，卸载和移除 Superfish 有点复杂。

1.  [前往此链接](https://filippo.io/Badfish/) ( [LastPass 也有一个工具](http://www.lastpass.com/superfish) ，如果你想再看一眼的话)在 ie 浏览器或 Chrome 中测试你的电脑是否安装了 Superfish(它在 Firefox 上不能工作)。如果你得到一个否定的回答，你就很好，如果你得到一个肯定的回答，继续第二步。
2.  打开 Windows 开始菜单或开始屏幕，搜索“卸载程序”。启动它。
3.  右键单击“Superfish Inc VisualDiscovery”并选择“卸载”，然后输入您的管理员密码。
4.  接下来，您需要卸载证书。回到开始菜单，搜索 certmgr.msc，启动它。
5.  单击“受信任的根证书颁发机构”并打开证书。
6.  查找任何包含 Superfish Inc .的证书，并右键单击将其删除
7.  重新启动浏览器，然后返回到步骤 1 中的链接来测试您的计算机。

有了这个，你的系统应该没有超级鱼了。如果你使用 Firefox 或 Thunderbird，你也可以使用 [这些指令](http://arstechnica.com/security/2015/02/how-to-remove-the-superfish-malware-what-lenovo-doesnt-tell-you/) 来检查它们的证书库。 ***更新*** :有相互矛盾的报道，有些人说卸载证书还不够。然而，包括微软自己在内的大多数人认为，删除证书就足够了。如果你想做得非常彻底，你可以一直 [进行 Windows *的全新安装，而不用*所有的膨胀软件](https://lifehacker.com/can-i-reinstall-windows-on-my-computer-without-the-bloa-1512345361) 。

如果你想了解更多关于技术(和历史)方面的信息，那么[【The Next Web】](http://thenextweb.com/insider/2015/02/19/lenovo-caught-installing-adware-new-computers/)和 [【福布斯】](http://www.forbes.com/sites/thomasbrewster/2015/02/19/superfish-need-to-know/) 都会更深入地挖掘。

<small>*照片由*</small> [<small>*绿色 Edmond mihai*</small>](http://www.shutterstock.com/pic-146064485/stock-vector-fish-icons.html?src=vKB2a1K8xDnr8d2LDj_iHw-1-5&ws=1)*。*