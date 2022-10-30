# 如何让您的联网家庭安全无虞

> 原文：<https://lifehacker.com/how-to-keep-your-internet-connected-home-safe-and-secur-1677537047>

从 [像 Nest](https://lifehacker.com/what-can-a-smart-thermostat-do-that-mine-can-t-already-472975733) 这样的智能恒温器到 [永远开启的安全摄像头](http://lifehacker.com/psa-change-your-ip-webcams-default-password-if-you-ha-1656886609) ，每年我们都会给家里增加更多连接互联网的电器和小工具。有些提供远程监控等强大功能，有些则利用数据来帮助您优化家居环境并节省资金。即便如此，任何连接到互联网的东西都有被黑客攻击的风险。以下是如何保证所有新装备安全的方法。



您可能没有想到，恒温器、NAS 设备、电视、厨房电器和家庭自动化系统等持续连接的设备无时无刻不在与互联网交换数据。我们称所有这些设备为“物联网”，但像其他联网设备一样，它们很容易受到世界其他地方的影响。这意味着在设置它们之前，您需要采取一些预防措施。

### 切勿在没有防火墙的情况下将您的设备连接到互联网

我们大多数人家里都有一个路由器，它通过执行 [网络地址转换](http://en.wikipedia.org/wiki/Network_address_translation) (NAT)来充当防火墙。简而言之，路由器将发往某个设备的流量发送到该设备，并丢弃不期望的、不想要的或特别恶意的流量。我们大多数人都无法想象，如果没有路由器的保护，或者至少有某种防火墙来阻止恶意流量和端口扫描，我们的计算机会直接连接到互联网。你没有理由认为你的新设备中的微型电脑有什么不同。它可能不会存储敏感或个人信息，但如果它也在您的家庭网络上，那么没有理由不将它放在您的家庭路由器或防火墙后面。

一些设备，如 IP 安全摄像头，试图通过建议您将它们暴露在互联网上来简化设置。他们通常依靠密码保护和独立的网页来保持安全。不幸的是，我们已经了解到 [与](http://lifehacker.com/psa-change-your-ip-webcams-default-password-if-you-ha-1656886609) 相差甚远。对于这些设备，你肯定应该使用强密码，但你仍然应该将它们锁定在防火墙后面，最好配置有 [端口转发](https://lifehacker.com/know-your-network-lesson-4-access-your-home-computers-5831841) ，这样你就可以在需要时从外部访问它们，它们也可以在必要时呼叫总部。

### 定期检查固件和安全更新

打开包装并插入新的联网设备时，您应该做的第一件事是检查固件更新。就像任何外围设备一样，它与最新版本的软件一起放在架子上的盒子里的几率非常低。可能有一个更新提供了安全更新和功能改进，甚至可能包含一些在线安全使用它所必需的关键补丁。访问制造商的网站，寻找连接和更新设备的说明。即使没有更新，至少你会知道如何做，你可以定期查看何时发布了安全更新。

当我们谈到像 Shellshock 和 Heartbleed 这样的[bug 的严重性时，我们发现的一个大问题是，许多联网设备从未被监控或更新。它们可能是执行特定功能的“嵌入式”系统(除非它们坏掉，否则没有人会检查它们)，或者它们可能在人们意识不到已经连接的设备中。学习如何定期检查更新——即使您的设备没有为您检查更新——将确保您的投资安全并保持最佳性能。](https://lifehacker.com/are-bugs-like-shellshock-and-heartbleed-really-serious-1641177186)

### 考虑为远程访问部署您自己的 VPN

VPN，或称 [虚拟专用网](http://en.wikipedia.org/wiki/Virtual_private_network) ，让你能够安全地远程连接到你的家庭网络。我们已经讨论了 [在](https://lifehacker.com/why-you-should-be-using-a-vpn-and-how-to-choose-one-5940565) 之前 VPN 是如何工作的，当它们对进出你的设备的信息进行加密时，你也可以使用它在你和一个受信任的网络(在这种情况下，你的家庭网络)之间创建一个私人连接，这样你就可以检查安全摄像头，打开或关闭恒温器，或者从你的 NAS 上抓取文件，而不用担心互联网的其他部分会做同样的事情。这样，您可以将您的设备开放到您的家庭网络，而不是整个互联网，但仍然可以通过您的 VPN 登录到您的家庭网络，从任何地方访问它们。

你可以使用高级 VPN 服务，如 [一些我们最喜欢的](http://lifehacker.com/five-best-vpn-service-providers-5935863) 来完成这项工作，或者你可以 [用树莓派和 OpenVPN](https://lifehacker.com/roll-your-own-vpn-with-a-raspberry-pi-and-openvpn-1563401069) 来部署你自己的 VPN，或者只是在你的家庭路由器、NAS 甚至你放在家里的旧电脑上使用 [OpenVPN](https://openvpn.net/) 。无论您选择的工具是什么，您都可以使用 VPN 来保护您连接的设备的安全，在您的家庭防火墙之后，并且只有当您连接回您的家庭网络时才能从外部访问。如果这些设备出于自己的目的需要互联网，如更新或功能改进，您仍然需要设置端口转发。然而，如果你只是需要远程访问，VPN 是控制谁可以在什么时候连接中的*的好方法。然后，当这些设备需要手动调用*输出*时，您可以对其进行监控。*

### 保护您的家庭网络

当然，只有在家庭网络安全的情况下，将所有这些设备放在防火墙或路由器后面才会有所帮助。花点时间 [了解一下你的家庭网络](https://lifehacker.com/know-your-network-the-complete-guide-5833254) ，正确设置， [确保你路由器的安全设置达到标准](http://lifehacker.com/the-most-important-security-settings-to-change-on-your-1573958554) 。如果您的家庭网络配置不佳，则您试图屏蔽的设备不会受到太多保护。如果你真的想探索这些设备是如何通信的，制作一张网络图并利用你的网络会有一些好处。

除了确保您的路由器的密码是唯一的和强大的，您的固件是最新的，请确保您的路由器正在使用强大的 Wi-Fi 加密(最好是 WPA 或 WPA2，禁用 WPS)，并且您的路由器的管理页面无法访问互联网。您还需要确保您的所有其他设备都受到您的路由器或其他防火墙的保护——您网络的一个入口点可能会暴露所有其他联网设备。最后，确保你在电脑上运行的是可靠的、更新的防病毒和反恶意软件工具 。

### 自学

最后，一定要记住，安全链中最薄弱的环节总是最终用户。也就是说你。如果您不花时间自学如何保护您的数据和设备，您将在家庭网络中留下漏洞，从而导致身份盗窃、欺诈或恶意用户出于自己的目的使用您的设备。这可能意味着你的电脑在 DDOS 攻击中变成了僵尸，或者在不知情的情况下成为了比特币挖矿操作的一员，你的 IP 摄像头被贴在互联网上供所有人观看，或者你的恒温器成为了脚本小子想要恶作剧的对象。一些值得查看的资源:

*   FCC 的 [保护家庭网络指南](http://www.fcc.gov/guides/protecting-your-wireless-network)
*   US-CERT 的 [家庭网络安全指南](https://www.us-cert.gov/Home-Network-Security)
*   国家网络安全联盟的 [网络安全指南](http://www.staysafeonline.org/stay-safe-online/keep-a-clean-machine/securing-your-home-network)
*   我们的 [知道你的网络夜校](https://lifehacker.com/know-your-network-the-complete-guide-5833254)

无论是哪种情况，无论后果是严重还是令人讨厌，一点点深谋远虑和一点点教育都有助于确保您所有的新互联网连接设备-以及您的旧设备，如个人电脑和游戏机-都能按照您希望的方式运行。

<small>*照片由*</small>[<small>*erocsid*</small>](https://www.flickr.com/photos/erocsid/15315681843)<small></small>*[<small>*沃伦·罗纳*</small>](https://www.flickr.com/photos/warrenski/5094412728) <small>*，以及*</small> [<small>*二进制考拉*</small>](https://www.flickr.com/photos/binary_koala/3037508563)<small></small>*