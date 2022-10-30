# Linux 安全发行版比较:Tails vs. Kali vs. Qubes

> 原文：<https://lifehacker.com/linux-security-distros-compared-tails-vs-kali-vs-qub-1658139404>

如果您对安全性感兴趣，您可能已经听说过关注安全性的 Linux 发行版，如 Tails、Kali 和 Qubes。它们对于匿名浏览、渗透测试和收紧系统以防止潜在黑客攻击非常有用。以下是这三者的优缺点。

Watch

似乎每隔一天，我们就会听到另一个黑客攻击、浏览器漏洞或恶意软件。如果你在公共 Wi-Fi 网络上进行大量浏览， [你更容易受到这些类型的攻击](https://lifehacker.com/do-i-really-need-to-worry-about-security-when-i-m-using-5906233)。以安全为中心的 Linux 发行版会有所帮助。对于我们大多数人来说，这里的用例非常简单。

如果你需要在咖啡店或图书馆使用公共 Wi-Fi 网络，那么这些发行版之一可以隐藏你的流量，防止有人试图偷看。同样，如果你担心有人追踪你的位置——无论是一个令人毛骨悚然的跟踪者还是更糟糕的东西——随机化和匿名化你的流量会让你安全。显然你并不总是需要这个，但是如果你正在检查银行对账单，上传文件到工作服务器，甚至只是购物，安全总比后悔好。

所有这些发行版都可以在虚拟机上运行，也可以从实时 CD/USB 上运行。这意味着你可以把它们放在口袋里，需要的时候穿上它们，不会给自己带来太多麻烦。

### Tails 通过匿名提供安全性

[Tails](https://tails.boum.org/) 是一个基于 Debian 的实时操作系统，它使用 [Tor](https://torproject.org/) 来处理所有的互联网流量。它的主要目标是通过匿名 给你 [的安全感。有了它，你可以通过加密连接匿名浏览网页。](https://lifehacker.com/browse-like-bond-use-any-computer-without-leaving-a-tr-5916551)

尾巴以多种方式保护你。首先，因为你所有的流量都是通过 Tor 传送的，所以很难追踪你的物理位置或者查看你访问了哪些网站。Tails 不使用电脑的硬盘，所以你做的任何事情都不会保存到运行它的电脑上。相反，你所做的一切都存储在内存中，当你关机时就会被删除。这意味着您正在处理的任何敏感文档都不会被永久存储。因此，当你在公共计算机或网络上时，Tails 是一个非常好的操作系统。

Tails 还打包了一堆基本的加密工具。如果你用 u 盘运行 Tails，它是用加密的。你所有的上网流量都用 [HTTPS Everywhere](https://www.eff.org/https-everywhere) 加密，你的 IM 对话用 [OTR](https://en.wikipedia.org/wiki/Off-the-Record_Messaging) 加密，你的邮件和文档用 [OpenPGP](https://en.wikipedia.org/wiki/OpenPGP) 加密。

尾巴的关键是匿名。虽然它有加密工具，但它的主要目的是匿名化你在网上的一切。这对大多数人来说很棒，但这并没有给你做傻事的自由。如果你用真实姓名 登录你的 [脸书账户，你的身份仍然会很明显，在网络社区保持匿名比看起来](http://lifehacker.com/facebook-unveils-a-tor-friendly-onion-address-for-ano-1654081929) 要难得多。

**优点:**通过 Tor 路由你的所有流量，附带一吨开源软件，有一个[【Windows 伪装】](https://tails.boum.org/doc/first_steps/startup_options/windows_camouflage/index.en.html) 模式，让它看起来更像 Windows 8。

缺点:不能在本地保存文件，速度慢，通过 Tor 加载网站需要很长时间。

**最适合谁:**燕尾服最适合在旅途中使用。如果你发现自己经常在咖啡店或公共图书馆使用互联网，那么 Tails 对你来说再合适不过了。匿名就是游戏，所以如果你厌倦了每个人都在追踪你在做什么，Tails 很好，但要记住，除非你在网上到处使用假名，否则它也是没用的。

### 卡莉是进攻安全的化身

Tails 与匿名有关，Kali 主要面向 [安全测试](https://lifehacker.com/how-to-hack-your-own-network-and-beef-up-its-security-w-1649785071) 。Kali 是建立在 Debian 上的，由进攻性安全有限公司维护。你可以运行 Kali 的活光盘，USB 驱动器，或在一个虚拟机。

Kali 的主要关注点是笔测试，这意味着它非常适合在您自己的网络中探索安全性，但不是为一般用途而构建的。也就是说，它确实有一些基本的软件包，包括用于浏览网页的 [Iceweasel](https://wiki.debian.org/Iceweasel) 以及运行安全服务器所需的一切，包括 SSH、FTP 等等。同样地，Kali 配备了工具 [隐藏你的位置并设置 VPN](http://null-byte.wonderhowto.com/how-to/mask-your-ip-address-and-remain-anonymous-with-openvpn-for-linux-0131031/)，所以它完全有能力让你匿名。

Kali 有大约 300 种测试网络安全的工具，所以很难真正跟踪其中包括什么，但 Kali 最受欢迎的事情是 [破解 Wi-Fi 密码](https://lifehacker.com/how-to-crack-a-wi-fi-password-5953047) 。Kali 的格言坚持“最好的防御就是最好的进攻”，因此它旨在帮助您测试整个网络的安全性，而不仅仅是让您在一台机器上安全。不过，如果你使用 Kali Linux，它不会在你运行它的系统上留下任何东西，所以它本身是相当安全的。

除了 Live CD，Kali 还可以在大量的 ARM 设备上运行，包括树莓 Pi、、几款 Chromebooks，甚至 Galaxy Note 10.1。

**优点:**测试网络所需的一切都包含在发行版中，相对容易使用，既可以在 Live CD 上运行，也可以在虚拟机上运行。

**缺点:**不包含太多日常使用的工具，不包含 Tails 所包含的加密工具。

**最适合谁:** Kali 最适合希望测试网络安全漏洞的 It 管理员和爱好者。虽然它本身是安全的，但它没有我们大多数人从操作系统中需要的基本日常使用的东西。

### Qubes 通过隔离提供安全性

Qubes 是一个基于 Fedora 的桌面环境，通过隔离来保证安全性。Qubes 认为不可能有一个真正安全的操作系统，所以它在虚拟机内部运行一切。这确保了如果您是恶意攻击的受害者，它不会蔓延到整个操作系统。

使用 Qubes，您可以为您的每个环境创建虚拟机。例如，您可以创建一个包含 Firefox 和 Thunderbird 的“工作”虚拟机，一个仅包含 Firefox 的“购物”虚拟机，以及您需要的任何其他虚拟机。这样，当您在“购物”虚拟机中瞎折腾时，它会与您的“工作”虚拟机隔离开来，以防出现问题。您可以创建 Windows 和 Linux 的虚拟机。您还可以为一次性操作创建可处置的虚拟机。这些虚拟机中发生的任何事情都是孤立的，但并不安全。如果你运行一个漏洞百出的网络浏览器，Qubes 并不能阻止这种利用。

架构本身也是为了保护您而建立的。您的网络连接会自动获得自己的虚拟机，您可以设置代理服务器以获得更高的安全性。同样，存储也有自己的虚拟机，硬盘上的所有内容都会自动加密。

Qubes 的主要缺点是你需要手动完成所有的事情。设置虚拟机可以从整体上保护您的系统，但是在实际使用它们时，您必须积极主动。如果你想让你的数据保持安全，你必须把它和其他东西分开。

优点:隔离技术可以确保如果你下载了恶意软件，你的整个系统不会被感染。Qubes 在 [各种各样的硬件](https://qubes-os.org/wiki/HCL) 上工作，很容易在虚拟机之间安全地共享剪贴板数据。

**缺点:** Qubes 要求你采取措施创建虚拟机，因此没有一种安全措施是万无一失的。它仍然完全容易受到恶意软件或其他攻击，但它感染整个系统的可能性较小。

**最适合谁:** Qubes 最适合那些主动型的人，他们不介意做一些工作来建立一个安全的环境。如果你正在做一些你不想让别人知道的事情，写下一堆个人信息，或者你只是把你的电脑交给一个喜欢点击恶意网站的朋友，那么虚拟机是一个保持安全的简单方法。像 Tails 这样的东西为你做开箱即用的一切，Qubes 需要一点时间来设置和开始工作。Qubes [用户手册相当庞大](https://qubes-os.org/wiki/UserDoc) 所以你必须愿意花一些时间去学习它。

### 其余的:Ubuntu Privacy Remix、JonDo 和 IprediaOS

Tails、Kali 和 Qubes 肯定不是唯一关注安全性的操作系统。让我们快速看一下其他几个流行的选项。

*   [Ubuntu Privacy Remix](https://www.privacy-cd.org/en):顾名思义，Ubuntu Privacy Remix 是一个建立在 Ubuntu 之上的隐私聚焦分发。它是离线的，所以基本上任何人都不可能黑进去。操作系统是只读的，因此无法更改，您只能将数据存储在加密的可移动介质上。它还有一些其他的锦囊妙计，包括阻止第三方激活你的网络连接的系统和 TrueCrypt 加密。
*   [【JonDO】](https://anonymous-proxy-servers.net/en/jondo-live-cd.html'):JonDO 是一个基于 Debian 的直播 DVD，包含代理客户端，一个预配置的匿名冲浪浏览器，以及一些基本级别的安全工具。它类似于 Tails，但是更加简单和陌生。
*   [IprediaOS](http://www.ipredia.org/) :和尾巴一样，IprediaOS 也是匿名的。IprediaOS 不是通过 Tor 路由流量，而是通过 [I2P](http://en.wikipedia.org/wiki/I2P) 路由流量。

当然，这些操作系统都不是日常使用的理想选择。当你匿名化你的流量，隐藏它，或者把它从你的操作系统中隔离出来，你倾向于占用系统资源来减慢速度。同样，带宽成本意味着你的大部分网页浏览都很糟糕。尽管如此，当你在公共 Wi-Fi 上，使用公共电脑，或者当你只是需要使用朋友的电脑，而你又不想留下你的私人数据时，这些浏览器是非常棒的。

它们都足够安全，可以通过我们的一般行为来保护我们大多数人，所以请选择最适合您特定需求的一种。

<small>*照片由*</small>[<small>*yyang*</small>](http://www.shutterstock.com/pic.mhtml?id=203790493&src=id)<small>*。*T15】</small>