# 路由器上需要更改的最重要的安全设置

> 原文:[https://life hacker . com/the-most-important-security-settings-to-change-on-your-1573958554](https://lifehacker.com/the-most-important-security-settings-to-change-on-your-1573958554)

您的路由器是抵御黑客试图访问您家中所有联网设备的第一道防线。可悲的是， [很多顶级的 Wi-Fi 路由器很容易被黑掉](http://www.cnet.com/news/top-wi-fi-routers-easy-to-hack-says-study/) 。你应该关心一下——还要确保你的路由器设置正确。

Watch

我们之前已经讨论过 [你应该在你的路由器上改变](https://lifehacker.com/what-settings-should-i-change-on-my-wi-fi-router-5553789) 的基本设置——这些仍然适用。

概括一下:

*   如果可能，更改默认管理员密码和用户名
*   更改 SSID(或您的无线网络的名称)，这样您的设备就不会总是连接到类似名称的网络(例如“linksys”)，也不会让黑客对您的路由器型号有更多的线索(例如“linksys”)
*   将无线安全模式设置为 WPA2，并为其选择一个好的长密码

希望您已经完成了这些安全性更改。然而，除了这些基础知识，在这个黑客攻击日益猖獗的时代，你还可以做更多的事情来锁定你的网络安全。

### 如果你的路由器支持，安装 DD-WRT 或番茄

除了为你的路由器 [增加额外功能](http://lifehacker.com/turn-your-60-router-into-a-600-router-178132) 之外，开源路由器固件 [DD-WRT](http://www.dd-wrt.com/site/index) 和 [番茄](http://www.polarcloud.com/tomato) 可能比你的路由器自带的普通固件更安全。DD-WRT 和番茄往往不容易受到许多路由器 中发现的 [漏洞的影响，例如](http://www.securityevaluators.com/knowledge/case_studies/routers/soho_router_hacks.php) [WPS (Wi-Fi 保护设置)](http://lifehacker.com/how-to-crack-a-wi-fi-networks-wpa-password-with-reaver-5873407) 中一直流行的问题。它们还会更定期地更新，提供更多的安全选项(如高级日志记录或使用 DNSCrypt 对 DNS 进行加密)，并让您更好地控制您的硬件。安全专家布莱恩·克雷布斯 [说](http://krebsonsecurity.com/2014/02/time-to-harden-your-hardware/) :

> 大多数库存路由器固件相当笨重和准系统，否则包括未记录的“功能”或限制。
> 
> 通常在升级路由器固件时，我倾向于引导人们远离制造商的固件，转向替代的开源替代产品，如 [DD-WRT](http://www.dd-wrt.com/site/index) 或 [番茄](http://www.polarcloud.com/tomato) 。我长期以来一直依赖 DD-WRT，因为它提供了你在路由器固件中可能想要的所有铃声、哨声和选项，但它通常会默认关闭这些功能，除非你打开它们。

查看 [DD-WRT](http://www.dd-wrt.com/wiki/index.php/Supported_Devices) 和 [番茄](http://en.wikibooks.org/wiki/Tomato_Firmware#Supported_devices) 的支持设备页面，看看它们是否适合你。番茄对用户更友好，但是 DD-WRT 有更多的设置。

### 定期更新您的固件

无论您使用的是普通固件还是第三方固件，保持固件最新都很重要，因为新的漏洞总是会被发现(比如让远程用户无需登录即可访问管理控制台的 [Linksys bug](http://news.dice.com/2014/02/18/home-routers-pose-biggest-consumer-cyberthreat/) ，或者一些流行路由器内置的后门)。

更新固件的实际步骤可能因路由器而异，但大多数步骤都允许您从路由器控制面板检查新固件。在浏览器中，输入路由器的 IP 地址，登录，然后查看高级设置或管理部分。或者，您可以查看路由器制造商的支持网站，了解是否有新的固件可用。

一些路由器还提供自动更新到最新固件的能力，但是您可能更喜欢检查更新提供了什么并手动安装。

### 关闭远程管理

在许多路由器上，这在默认情况下是关闭的，但是，为了以防万一，请检查远程管理(也称为远程管理或从 WAN 启用 web 访问)是否被禁用。远程管理允许从家庭网络外部访问路由器的控制面板，因此您可以看到为什么会有问题。同样，该设置可能在您的高级或管理部分下。

### 禁用 UPnP

UPnP，即通用即插即用，旨在使网络设备更容易被路由器发现。不幸的是，这个协议也充满了严重的安全漏洞，UPnP 的错误和糟糕的实现影响了数百万在线连接的设备。最大的问题是 UPnP 没有任何种类的认证(它认为每个设备和用户都是值得信任的)。How-To Geek 解释了 UPnP 的一些 [问题，如果它在您的路由器上启用，其中包括恶意应用程序将流量重新路由到本地网络以外的不同 IP 地址的可能性。](http://www.howtogeek.com/122487/htg-explains-is-upnp-a-security-risk/)

[GRC 的 UPnP 测试](https://www.grc.com/su/UPnP-Rejected.htm) 可以告诉你你的设备是否不安全，是否暴露在公共互联网中，在这种情况下你应该断开它们。(注意:点击页面右上方的红丝带运行实际测试；你通过链接登陆的页面只是一个例子。)

要关闭路由器上的 UPnP，请进入管理控制台并查找 UPnP 设置(在许多路由器上，在管理部分下)。如果可用，也禁用“允许用户配置 UPnP”选项。请记住，这不会影响你的能力，比如说， [通过 UPnP](http://lifehacker.com/what-is-upnp-and-how-do-i-use-it-to-stream-media-to-my-5803975) 在你的网络上传输视频——它只会影响你网络以外的东西。这确实意味着你可能必须 [手动设置端口转发](https://lifehacker.com/know-your-network-lesson-4-access-your-home-computers-5831841) 才能让 BitTorrent 这样的东西以最佳方式工作。

### 其他可能不值得麻烦的设置

你可能也听说过其他设置，比如打开 MAC 过滤或者隐藏你的网络 SSID，但是尽管它们很麻烦，它们并没有增加太多的安全性。

#### SSID 隐藏

乍一看，隐藏路由器的 SSID 听起来是个好主意，但它实际上可能会降低你的安全性。Wi-Fi 安全专家约书亚·赖特 [在 Tech Republic](http://www.techrepublic.com/blog/mobile-enterprise/wi-fi-security-is-always-one-step-behind/#.) 上解释道:

> **问题:** Joshua，请告诉我你对禁用广播路由器 SSID 的想法。
> 
> 约书亚·赖特:这是个坏主意。我知道 PCI 规范要求您这样做，我已经告诉他们需要从规范中删除这一要求。想象你是一个政府基地，你不告诉你的代理人你在哪里。他们不得不走来走去，不停地问“你是政府基地吗？”敬每一个遇见的人。最终，一些老谋深算的黑客或坏人会说“我是你的基地，进来和我分享你的秘密吧。”这基本上就是 SSID 伪装所发生的事情，您必须询问您遇到的每个 AP 他们想要的 SSID 是否可用，从而允许攻击者在机场、咖啡店、飞机上等地冒充您的 SSID。简而言之，不要掩盖你的 SSID，但也不要让你的 SSID 像“sexyhackertargethere”一样。

隐藏你的路由器 SSID 可能会阻止你的邻居 [试图在你的网络](http://lifehacker.com/how-can-i-find-out-if-someone-s-stealing-my-wi-fi-5738123) 上免费下载，但这不会阻止有能力的黑客，甚至可以作为一个响亮的信号告诉他们，“嘿，我在试图隐藏。”此外，如果你想让你的邻居不免费，只要确保你有一个安全的密码。

#### MAC 过滤

类似地，MAC 过滤将网络访问限制在你允许的设备上，这听起来很棒，可以为普通的免费用户提供额外的保护，但 MAC 地址很容易被欺骗。栈交换用户 sysadmin1138 [这样总结](http://security.stackexchange.com/questions/1606/are-mac-address-filtering-and-ssid-hiding-still-worthwhile) :

> 对于特别想要你的网络的人来说，加密(尤其是未破解的加密)将提供更好的安全性。如今，在大多数适配器中，MAC 欺骗是微不足道的，当您将网络破解到可以监控传输中的数据包时，您可以获得有效 MAC 地址的列表。SSID 在这一点上也是微不足道的。由于可用工具集的自动化特性，MAC 过滤和 SSID 隐藏真的不值得再花力气了。在我看来。

也就是说，如果你不介意麻烦，打开 MAC 过滤不会有什么坏处*。*只需知道它并没有看起来那么强大的安全功能——如果您有了新设备，或者有朋友来访，这将是一件非常麻烦的事情。*T3】*

#### 静态 IP 地址

最后，还有一个设置你可以考虑改变:关闭 DHCP，它会自动分配网络地址给连接到你路由器的设备。相反，您可以为所有设备分配静态 IP 地址。理论是，如果 DHCP 被禁用，未知的机器将不会得到一个地址。

但是，DHCP 和静态 IP 都有风险和缺点，正如 [这篇关于栈交换](http://security.stackexchange.com/questions/1925/dhcp-vs-static-ip-addressing) 的讨论所指出的；静态 IP 容易受到欺骗攻击，而通过 DHCP 获得 IP 的设备可能会受到来自恶意 DHCP 服务器的中间人攻击。对于哪一种更安全还没有一致的意见(尽管微软社区 [的一些人说这没有任何区别](http://answers.microsoft.com/en-us/windows/forum/windows_7-networking/which-is-more-secure-static-ip-address-or-dynamic/6eee9598-ad27-4473-926d-11ef609e9441) )。

如果您已经完全掌握了以上几节中提到的安全设置，那么您就可以安心地休息了，因为您知道您很可能会尽最大努力来保护您的家庭网络。