# 如何查看您的 VPN 是否泄露了您的 IP 地址(以及如何阻止它)

> 原文：<https://lifehacker.com/how-to-see-if-your-vpn-is-leaking-your-ip-address-and-1685180082>

VPN 在安全性方面很棒，但是许多人使用 VPN 的一个重要原因是掩盖或改变他们的 IP 地址。这可以让您避开基于位置的内容限制，或者检查您的提供商是否正在限制您的连接。不幸的是，一个新的安全漏洞会暴露你的真实 IP 地址，即使你使用的是 VPN，这也很容易被利用。这就是它的工作原理，以及你能做些什么。



### 这是什么？我的数据有风险吗？

让我们后退一点。虚拟专用网络，或 VPN， [对加密你的数据和提高安全性很有用](https://lifehacker.com/why-you-should-be-using-a-vpn-and-how-to-choose-one-5940565) ，但它也有助于掩盖你的 IP 地址。您的 IP 地址是由您的服务提供商分配给您的互联网连接的，它可以揭示您的服务提供商是谁，以及(一般而言)您的位置。如果你曾经访问 YouTube 并看到“对不起，这个视频在你的国家不可用”，或者试图注册一个新的服务，却发现你的国家不支持，他们是如何知道你的 IP 地址的。

很多人使用 VPN 专门为了 [绕开那些位置限制](https://lifehacker.com/the-always-up-to-date-guide-to-streaming-blocked-conten-5983904) 。当您登录 VPN 时，通常您可以选择一个“出口服务器”，或者一个您的 VPN 将“假装”您实际所在的位置。通常这足以让一个服务机构相信你在一个受支持的国家。

然而， [最近发现的一个安全漏洞](http://torrentfreak.com/huge-security-flaw-leaks-vpn-users-real-ip-addresses-150130/) 允许远程站点利用 WebRTC ( [Web 实时通信](http://en.wikipedia.org/wiki/WebRTC) ，这是大多数浏览器内置的一个功能)来泄露用户的真实 IP 地址，即使他们连接到 VPN。据我们所知，网站还没有利用这个漏洞，但考虑到 Hulu、Spotify、网飞和其他服务正在采取措施识别和锁定 VPN 用户，不难假设他们会开始这样做。

只需几行代码，就可以解除使用 VPN 获得的位置保护，并找出您的实际位置以及您的互联网服务提供商是谁(谁可以将您的地址与您联系起来)。)虽然该漏洞目前主要是基于浏览器的，但任何可以渲染网页(并使用 WebRTC)的应用程序都会受到影响，这意味着任何人都可以越过您的 VPN 看到您的真实位置和真实身份。广告商、数据经纪人和政府可以用它来窥视你的 VPN，找出你的连接真正来自哪里。如果你使用 BitTorrent 之类的服务，拥有 Roku 之类的机顶盒，或者只是通过你所在国家不可用的网站在你的电脑上播放音乐或电影(或者你是一名外籍人士，住在国外)，你使用的应用程序和服务可能会突然停止工作。

### 如何检查我的 VPN 是否受到影响？

该漏洞是由 GitHub 的开发者 [丹尼尔·罗斯勒](https://daylightpirates.org/) 超过 [记录的。罗斯勒解释了这一过程的工作原理:](https://github.com/diafygi/webrtc-ips)

> Firefox 和 Chrome 实现了 WebRTC，允许向 [STUN](http://en.wikipedia.org/wiki/STUN) 服务器发出请求，返回用户的本地和公共 IP 地址。javascript 可以获得这些请求结果，所以现在可以在 javascript 中获得用户的本地和公共 IP 地址。这个演示就是这样一个实现的例子。
> 
> 此外，这些 STUN 请求是在正常的 XMLHttpRequest 过程之外发出的，因此它们在开发人员控制台中不可见，或者能够被插件(如 AdBlockPlus 或 Ghostery)阻止。如果广告客户设置了带有通配符域的 STUN 服务器，这使得这些类型的请求可用于在线跟踪。

要查看您的 VPN 是否受到影响:

1.  访问像 [我的 IP 地址是什么](http://whatismyipaddress.com/) 这样的网站，记下你实际的 ISP 提供的 IP 地址。
2.  登录到您的 VPN，选择另一个国家的出口服务器(或使用您喜欢的任何出口服务器)并验证您已连接。
3.  回到 [我的 IP 地址是什么](http://whatismyipaddress.com/) 再次检查你的 IP 地址。您应该会看到一个新地址，一个与您的 VPN 和您选择的国家相对应的地址。
4.  访问罗塞勒的 [WebRTC 测试页面](https://diafygi.github.io/webrtc-ips/) ，注意页面上显示的 IP 地址。

如果这两个工具都显示你的 VPN 的 IP 地址，那么你是清白的。但是，如果“我的 IP 地址是什么”显示了您的 VPN，而 WebRTC 测试显示了您的正常 IP 地址，那么您的浏览器正在向全世界泄露您的 ISP 提供的地址。

当 [TorrentFreak 与 VPN 提供商](http://torrentfreak.com/huge-security-flaw-leaks-vpn-users-real-ip-addresses-150130/) 谈论这个问题时，包括 [我们最喜欢的](https://lifehacker.com/five-best-vpn-service-providers-5935863) 、 [私人互联网接入](https://www.privateinternetaccess.com/pages/buy-vpn/lifehacker) ，他们指出他们可以复制这个问题，但他们不确定他们如何才能阻止他们这边的漏洞。由于 IP 检查直接发生在用户和他们所连接的网站之间，因此很难阻止。即便如此，他们 [发表了一篇博客文章警告用户](https://www.privateinternetaccess.com/forum/discussion/8204/how-to-stop-webrtc-local-ip-address-leaks-on-google-chrome-and-mozilla-firefox-while-using-private-i#latest) 关于这个问题。 [TorGuard](http://torguard.net/) ，另一个我们喜欢的提供商， [也向他们的用户发出了警告](https://torguard.net/blog/browser-security-vulnerability-may-allow-real-ip-leak/) 。这些警告还说，这个问题似乎只影响 Windows 用户，但事实不一定如此——许多评论(和我们自己的测试)指出，根据你的 VPN 及其配置，即使你使用 Mac 或 Linux 系统，你的 IP 地址也可能被泄露。

### 我该如何保护自己？

幸运的是，你不必等待 VPN 提供商解决他们的问题来保护你自己。现在您可以做很多事情，其中大多数就像安装一个插件或在浏览器中禁用 WebRTC 一样简单。

#### 最简单的方法:在浏览器中禁用 WebRTC

Chrome、Firefox 和 Opera(以及基于它们的浏览器)通常默认启用 WebRTC。Safari 和 Internet Explorer 则不会，因此不会受到影响(除非您特别启用了 WebRTC。)不管怎样，如果上面的测试在你的浏览器上有效，你就会受到影响。您可以随时切换到没有启用 WebRTC 的浏览器，但是因为我们大多数人都喜欢我们使用的浏览器，所以应该这样做:

*   **Chrome 和 Opera** :从 Chrome 网上商店安装 [ScriptSafe](https://chrome.google.com/webstore/detail/scriptsafe/oiigbmnaadbkfbmpbfijlflahbdbdgdf?hl=en) 扩展。这有点过了，但是它会在你的浏览器中禁用 WebRTC。Opera 用户也可以使用这个插件，你只需要先通过一些关卡。
*   火狐浏览器:你有两个选择。你可以从 Mozilla 附加组件中安装 [禁用 WebRTC 附加组件](https://addons.mozilla.org/en-US/firefox/addon/happy-bonobo-disable-webrtc/)(h/t to[@ yourannonews](https://twitter.com/YourAnonNews/status/564500853286252544)获取链接)，或者打开一个选项卡，进入地址栏的“about:config”直接禁用 WebRTC。查找并设置“media.peerconnection.enabled”设置为 false。(你也可以安装 [NoScript](https://addons.mozilla.org/en-US/firefox/addon/noscript/) ，它很像 ScriptSafe，但是就像我们提到的，它可能有些矫枉过正。)

虽然罗塞勒指出 [隐私保护浏览器扩展](https://lifehacker.com/the-best-browser-extensions-that-protect-your-privacy-479408034) 像 AdBlock、uBlock、Ghostery 和 Disconnect 都不能阻止这种行为，但这些方法肯定能完成任务。我们已经对它们进行了测试，以确保它们能够工作，并保持警惕——您最喜欢的广告拦截器或隐私插件可能会在不久的将来更新以阻止 WebRTC。

我们应该注意，禁用 WebRTC 可能会中断一些 webapps 和服务。例如，使用你的麦克风和摄像头(如一些聊天网站或 Google Hangouts)或自动知道你的位置(如送餐网站)的基于浏览器的应用程序将停止工作，直到你重新启用它。

#### 更好的方法是:在路由器上配置 VPN

***更新*** *:我们已经和安全社区的许多人讨论过这个问题，在那些谈话之后，我们不确定在路由器级别配置你的 VPN 是否比在浏览器阻止 WebRTC 更有效(或者说，非常有效)。虽然我们仍然建议在路由器级别设置您的 VPN，原因如下所述，但就这个问题而言，现在我们建议您使用上面提到的浏览器插件，同时我们会对根本原因进行更多的研究，并对其进行万无一失的补救。*

如果你想有一个更可靠的方法来保护自己，而不是每次安装或更新时都安装附加组件并调整浏览器，有一个更持久的方法。在路由器上运行 VPN，而不是直接在计算机上运行。

这种方法有许多好处。首先，它可以保护家庭网络中的所有设备，即使它们不容易受到这个特定缺陷的攻击。它还为您的所有设备(如智能手机、平板电脑、机顶盒和智能设备)提供了与 VPN 为您的桌面提供的保护和加密相同的保护和加密。

不过，也有一些警告。首先，如果你是那种喜欢经常更换出口服务器的人(例如，有一天你想像在日本一样浏览，另一天在冰岛，另一天在美国)，这意味着每次你想切换位置时，你都必须调整你的路由器设置。类似地，如果您只需要有时连接，而不需要其他时候连接——就像您在工作中使用 VPN 而不是在流式传输网飞时，您将需要在每次需要切换时启用或禁用路由器上的 VPN。这个过程可能简单，也可能复杂，取决于您的路由器和 VPN。

许多 VPN 服务提供商建议您在路由器级别设置您的 VPN。有些甚至出售预先配置好使用其服务的特定路由器，但你也可以使用现有的路由器(只要它不是由你的互联网服务提供商提供的)。登录路由器的管理页面，检查您的“安全”或“连接”选项。根据您的型号，您会看到 VPN 部分，您可以在其中键入您正在连接的 VPN 提供商的名称、他们的服务器主机名以及您的用户名和密码。启用后，您的所有流量都将被加密。

如果你看不到它，一切都没有失去。请咨询您的 VPN 提供商，让他们知道您的路由器类型。他们可能会指导你完成这个过程。如果没有，看看你的路由器是否支持类似 [DD-WRT](http://www.dd-wrt.com/site/index) ( [在此搜索支持的设备](http://www.dd-wrt.com/site/support/router-database) )， [打开 WRT](https://openwrt.org/) ( [在此查看支持的设备](http://wiki.openwrt.org/toh/start) )，或者[番茄](http://www.polarcloud.com/tomato) ( [在此查看支持的设备](http://www.polarcloud.com/tomatofaq#what_will_this_run_on) )。我们之前已经向你展示了如何安装和设置 DD-WRT 和 [配置番茄](http://lifehacker.com/turn-your-60-router-into-a-user-friendly-super-router-344765) ，所以如果你是新手，就从我们的指南开始吧。所有这些定制的固件将允许你在路由器级别设置你的 VPN。

* * *

这种脆弱性是严重的，但从好的方面来看，它很容易减轻。如果有的话，这是一个提醒，永远不要认为你的隐私是理所当然的，即使你使用所有正确的工具来保护它。当我们谈论 [如何保护自己免受 DNS 泄露](https://lifehacker.com/how-to-boost-your-internet-security-with-dnscrypt-510386189) 时，我们提出了同样的观点:盲目信任隐私工具，因为它说正确的事情是一个坏主意。信任，但要核实，将您的隐私和安全掌握在自己手中。

<small>*标题照片制作使用*</small>[<small>*Nemo*</small>](http://pixabay.com/en/padlock-black-lock-locked-closed-294535/)<small>*。附加照片由*</small> [<small>*【李中清】*</small>](https://www.flickr.com/photos/jronaldlee/5996590138)<small></small>*[<small>*保罗约瑟夫*</small>](https://www.flickr.com/photos/sashafatcat/3424567565) <small>*，以及*</small> [<small>*华特石匠*</small>](https://www.flickr.com/photos/waltstoneburner/2864394686) <small>*组成。*T51】</small>*