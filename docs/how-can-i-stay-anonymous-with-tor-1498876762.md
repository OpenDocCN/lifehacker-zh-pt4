# 我怎样才能在 Tor 面前保持匿名？

> 原文：<https://lifehacker.com/how-can-i-stay-anonymous-with-tor-1498876762>

即使最近揭露出 NSA 正在监听，Tor 仍然可能是匿名上网的最佳方式。但是为了做好这件事，你必须采取一些预防措施。 [信息安全栈交易所](http://security.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=security-100) 的专家为安全使用 Tor 提供指导。



**众所周知**[](http://security.stackexchange.com/questions/37430/is-the-fact-that-tors-development-is-largely-government-funded-cause-for-concer?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=security-100)****在安全社区中，像**[**Tor**](https://www.torproject.org/)**这样多功能的工具很可能是情报机构强烈关注的目标。虽然美国联邦调查局已经承认对一起**[**Tor**](https://lifehacker.com/how-can-i-prevent-my-isp-from-tracking-my-every-move-5923017)**恶意软件攻击负责，但 SIGINT 组织的参与尚未得到证实。2013 年 10 月初,《卫报》发布了“**[**Tor stanked**](http://www.theguardian.com/world/interactive/2013/oct/04/tor-stinks-nsa-presentation-document)**”一份 NSA 演示文稿(2012 年 6 月)概述了当前和拟议的利用网络的策略，这消除了所有疑问。****

****一些要点:****

*   **从根本上说，Tor 是安全的；但是，在某些情况下可以取消匿名**
*   ****“哑用户”总是容易受到攻击(内部称为“epic fail”)****
*   ****NSA/GCHQ 运营 Tor 节点****
*   ****各种形式的流量分析似乎是首选工具****

**在查阅文献之后，Tor 用户应该实施什么样的改变来确保——在技术上最大程度地可行——他们的持续安全性？**

***见原问题* [*此处*](http://security.stackexchange.com/q/43369/21882?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=security-100) *。***

#### **安全 Tor 使用指南( [答](http://security.stackexchange.com/a/43485/11291?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=security-100) 作者 [迈克尔·汉普顿](http://security.stackexchange.com/users/11291/michael-hampton?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=security-100) )**

**作为一个很长时间的 [Tor](https://lifehacker.com/roll-your-own-anonymizing-tor-proxy-with-a-raspberry-pi-513525281) 用户，对我来说，国家安全局文件中最令人惊讶的部分是他们在对抗 Tor 方面进展甚微。尽管它有众所周知的弱点，但它仍然是我们拥有的最好的东西，只要使用得当，不出差错。**

**既然你想要“技术上可行的最大程度”的，我将假设你的威胁是一个资金充足的政府，拥有显著的能见度或对互联网的控制，正如许多 Tor 用户一样(尽管有警告说 Tor 不足以保护你免受 [这样的演员](https://www.torproject.org/docs/faq.html.en#AttacksOnOnionRouting) 。**

**考虑一下你是否真的需要这种级别的保护。如果你的活动被发现不会危及你的生命或自由，那么你可能不需要这么麻烦。但是如果它真的发生了，那么如果你想继续活着和自由，你绝对必须保持警惕。**

**我不会在这里重复 Tor Project 的 [自己的警告](https://www.torproject.org/download/download.html.en#Warning) ，但是我会注意到它们只是一个开始，并不足以保护你免受这样的威胁。**

#### **你的电脑**

**迄今为止， [NSA](https://lifehacker.com/what-the-nsa-spying-scandal-means-to-you-511808090) 和 FBI 对 Tor 用户的主要攻击是 MITM 攻击(NSA)和隐藏服务 web 服务器入侵(FBI)，它们要么向 Tor 用户的计算机发送跟踪数据，要么破坏它，或者两者兼而有之。因此，你需要一个相当安全的系统来使用 Tor，并降低被跟踪或泄密的风险。**

1.  **不要用 Windows。就是不要。这也意味着不要在 Windows 上使用 Tor 浏览器捆绑包。TBB 软件中的漏洞在国家安全局的幻灯片和联邦调查局最近对自由主机的攻击中都很突出。**
2.  **如果你不能构建自己的工作站，能够运行 Linux，并仔细配置为运行最新版本的 Tor、Privoxy 之类的代理和 web 浏览器(具有所有传出的 clearnet 访问)的话，可以考虑使用 [Tails](https://tails.boum.org/) 或 [Whonix](https://www.whonix.org/) 来代替，这里的大部分工作已经为你完成了。这是绝对关键的外出访问防火墙，使第三方应用程序不能意外泄漏您的位置数据。**
3.  **如果您使用任何类型的永久存储，请确保它是加密的。当前版本的 LUKS 相当安全，主要的 Linux 发行版会在安装过程中为您设置它。TrueCrypt 可能是安全的，尽管它没有很好地集成到操作系统中。BitLocker 可能也是安全的，尽管你仍然不应该运行 Windows。即使你在一个合法使用橡胶软管的国家，比如英国，加密你的数据可以保护你免受各种其他威胁。**
4.  **请记住，您的计算机必须保持最新。无论您是使用 Tails 还是从零开始构建自己的工作站，还是使用 Whonix，请经常更新以确保您免受最新安全漏洞的攻击。理想情况下，您应该在每次开始会话时更新，或者至少每天更新。如果有更新，Tails 会在启动时通知您。**
5.  **非常不愿意在 JavaScript、Flash 和 Java 上妥协。默认情况下禁用它们。如果一个网站需要这些，请访问其他地方。只在万不得已的情况下才启用脚本，只是暂时的，并且只在获得网站功能所必需的最低程度上启用。**
6.  **恶意丢弃网站发送给您的 cookies 和本地数据。对我的口味来说，TBB 和泰尔斯都做得不够好；考虑使用一个插件，如 [自毁 cookie](https://addons.mozilla.org/en-US/firefox/addon/self-destructing-cookies/)来保持你的 cookie 最少。零的可能性。**
7.  **您的工作站必须是笔记本电脑；它必须足够轻便，便于随身携带，并能迅速处理或销毁。**
8.  **不要用谷歌搜索互联网。好的 [备选](https://startpage.com/eng/privacy-policy.html) 是[start page](https://startpage.com/)；这是 TBB、Tails 和 Whonix 的默认搜索引擎。另外，它不会说你恶意或要求你填写验证码。**

#### **你的环境**

**Tor 包含 [弱点](https://www.torproject.org/docs/faq.html.en#AttacksOnOnionRouting) ，这些弱点只能通过在现实世界中的行动来缓解。可以查看您的本地互联网连接和您正在访问的站点的连接的攻击者可以使用统计分析来关联它们。**

1.  **永远不要在家或在家附近使用 Tor。永远不要在家里做任何敏感到需要 Tor 的事情，即使你保持离线。电脑有一个有趣的习惯，喜欢联网。这也适用于你暂住的任何地方，比如酒店。从不在家进行这些活动有助于确保他们不会被束缚在那些地方。(请注意，这适用于面临高级持续威胁的人。在家运行 Tor 对其他人来说是合理和有用的，特别是那些自己什么都不做，但希望通过运行 [出口节点](https://blog.torproject.org/blog/tips-running-exit-node-minimal-harassment)[中继](https://www.torproject.org/docs/faq.html.en#BetterAnonymity) 或 [桥](https://www.torproject.org/docs/faq.html.en#RelayOrBridge) 来提供帮助的人。**
2.  **限制你在任何地点使用 Tor 的时间。虽然这些关联攻击需要一些时间，但理论上它们可以在一天内完成。虽然长筒靴不太可能在你在星巴克喝咖啡的同一天出现，但它们可能会在第二天出现。我建议真正关心的人在任何一个物理位置使用 Tor 不要超过 24 小时；之后就当烧了，去别处。这将有助于你，即使靴子在六个月后出现；记住一个老顾客比记住一个某天出现却再也没有回来的人要容易得多。这确实意味着你将不得不去更远的地方旅行，尤其是如果你不住在大城市，但这将有助于保持你自由旅行的能力。**
3.  **当你外出进行这些活动时，让你的手机开着，留在家里。**

#### **你的心态**

**许多 Tor 用户被抓是因为他们犯了一个错误，比如在他们的活动中公布了他们的真实电子邮件地址。你必须尽可能地避免这种情况，唯一的方法就是小心的精神训练。**

1.  **把你的 Tor 活动想象成假名，并在你的头脑中创造一个虚拟的身份来对应这个活动。这个虚拟人不认识你，也永远不会见到你，即使他认识你，也不会喜欢你。他必须在精神上严格隔离。**
2.  **如果你必须使用公共互联网服务，为这个假名创建一个全新的账户。千万不要把它们混在一起；例如，在同一台电脑上用你的化名使用 Twitter 后，不要用你的真实电子邮件地址浏览脸书。等到你回家。**
3.  **同样，除非你别无选择(如与屏蔽 Tor 的提供商签约)，否则千万不要通过 clearnet 执行与你的假名活动相关的操作，并在这样做时对你的位置采取额外的预防措施。**
4.  **如果您需要拨打和接听电话，请购买一部匿名预付费电话。这在一些国家很难做到，但是如果你有足够的创造力，这是可以做到的。支付现金；永远不要用借记卡或信用卡购买手机或充值。如果你在离家 10 英里(16 公里)以内，千万不要插入电池或开机，也不要使用电池无法取出的手机。切勿将一部手机中以前使用过的 SIM 卡放入另一部手机。千万不要把它的号码，甚至不要承认它的存在给任何一个通过你的真实身份认识你的人。这可能需要包括你的家庭成员。**

#### **隐藏服务**

**这些都是最近的大新闻，最近至少关闭了两个高调的隐藏服务，丝绸之路和自由主机。坏消息是，隐藏的服务比他们能做的要弱得多，或者说 [应该是](https://blog.torproject.org/blog/hidden-services-need-some-love) 。好消息是，NSA 似乎并没有在这方面做太多(尽管 NSA 的幻灯片提到了一个名为 ONIONBREATH 的 GCHQ 项目，该项目专注于隐藏的服务，但目前还不知道其他任何信息)。**

**此外，由于隐藏的服务必须经常在其他人的物理控制下运行，因此它们很容易受到其他人的攻击。因此，保护服务的匿名性甚至更加重要，因为一旦它以这种方式受到损害，它几乎就玩完了。**

**如果你只是访问一个隐藏的服务，上面给出的建议就足够了。如果您需要运行一个隐藏的服务，请执行以上所有操作，此外还要执行以下操作。请注意，这些任务需要有经验的系统管理员；没有相关的经验，执行它们将是困难的或不可能的。**

1.  **除非您也控制物理主机，否则不要在虚拟机中运行隐藏服务。Tor 和服务在防火墙物理主机上的防火墙虚拟机中运行的设计是可以的，前提是该物理主机由您控制，并且您不仅仅是租用云空间。**
2.  **Tor 隐藏服务的一个更好的设计是由两台物理主机组成，这两台主机是从两个不同的提供商那里租用的，尽管它们可能在同一个数据中心。在第一台物理主机上，一台虚拟机运行 Tor。主机和虚拟机都有防火墙保护，以防止除 Tor 流量和第二台物理主机流量之外的传出流量。第二台物理主机将包含一个具有实际隐藏服务的虚拟机。同样，这两个方向都有防火墙保护。它们之间的连接应该用 IPSec、OpenVPN 等来保护。如果怀疑运行 Tor 的主机可能受到危害，则可以立即移动第二台服务器上的服务(通过复制虚拟机映像),并停用两台服务器。这两种设计都可以用 [Whonix](https://www.whonix.org/) 相当容易地实现。**
3.  **从第三方租赁的主机很方便，但在服务提供商获得硬盘副本的情况下，特别容易受到攻击。如果服务器是虚拟的，或者它是物理的，但使用 RAID 存储，这可以在不使服务器离线的情况下完成。同样，不要租用云空间，并仔细监控物理主机的硬件。如果 RAID 阵列显示为降级，或者如果服务器莫名其妙地停机超过一段时间，则应该认为服务器受到了威胁，因为无法区分简单的硬件故障和这种性质的威胁。**
4.  **确保您的主机提供商提供对远程控制台的 24x7 访问(在主机行业，这通常被称为，尽管它通常是通过[【IPMI】](http://en.wikipedia.org/wiki/Intelligent_Platform_Management_Interface)实现的，它也可以安装操作系统。在安装过程中使用临时密码，并在安装并运行 Tor 后更改所有密码(见下文)。远程控制台还允许您运行完全加密的物理主机，降低通过物理危害丢失数据的风险；但是，在这种情况下，每次系统启动时都必须更改密码(即使这样也不能减少所有可能的攻击，但是可以为您争取时间)。**
5.  **你对运行该服务的主机的初始设置必须通过 clearnet，尽管是通过 ssh 然而，要重申的是，不要在家里或你以前去过的地方做。正如我们所见，仅仅使用 VPN 是不够的。由于此类提供商可能会使用欺诈保护，这可能会导致您在实际注册服务时出现问题。但是，如何处理这个问题超出了本答案的范围。**
6.  **一旦你启动并运行 Tor，不要再通过 clearnet 连接任何服务器或虚拟机。配置通过 ssh 连接到每个主机和每个虚拟机的隐藏服务，并始终使用它们。如果你必须通过 clearnet 连接来解决一个问题，同样，从一个你永远不会再访问的地方这样做。**
7.  **隐藏的服务必须定期移动，即使不怀疑有危害。2013 年的一篇论文描述了一种攻击，这种攻击可以在短短几个月内定位一个 [隐藏服务](http://www.ieee-security.org/TC/SP2013/papers/4977a080.pdf) ，云计算费用大约为 10，000 美元，这甚至在一些个人的预算之内。虽然一点也不方便，但至少每月移动一次隐藏的服务是比较安全的。理想情况下，应该尽可能频繁地移动它，尽管这很快就会变得不切实际。注意，Tor 网络将花费 [大约一个小时](http://tor.stackexchange.com/q/13/201?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=security-100) 来识别被移动的隐藏服务的新位置。**

#### **结论**

**[隐姓埋名](https://lifehacker.com/is-it-possible-to-be-truly-anonymous-in-an-online-commu-5953212) 难。光有技术，再好也永远不够。它需要清晰的头脑和对细节的仔细关注，以及现实世界中的行动来减轻不能仅通过技术解决的弱点。正如经常提到的那样，攻击者可能是笨手笨脚的傻瓜，他们只能依靠纯粹的运气，但你只需犯一个错误就可以毁了。我们称之为“高级持续威胁”,因为在某种程度上，它们是持续的。他们不会放弃，你也一定不会。**

***<small>不同意上面的答案？有自己的专长可以贡献？查看</small>* [*<small>原问题</small>*](http://security.stackexchange.com/q/43369/21882?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=security-100)<small>*并在*</small> [<small>*信息安全栈交流*</small>](http://security.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=security-100) <small>*查看更多类似问题，这是一个面向信息安全专业人士的问答网站。现在还有*</small> [<small>*一个 Tor 站点*</small>](http://tor.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=security-100) <small>*在栈交换网络中。如果你有自己的 Tor 问题需要解决，*</small> [<small>*提出问题*</small>](http://tor.stackexchange.com/questions/ask?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=security-100) <small>*。你会得到答案的。(而且是免费的。)*</small>**