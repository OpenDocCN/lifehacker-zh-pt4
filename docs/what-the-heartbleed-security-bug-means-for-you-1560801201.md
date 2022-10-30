# “心脏出血”安全漏洞对您意味着什么

> 原文：<https://lifehacker.com/what-the-heartbleed-security-bug-means-for-you-1560801201>

安全研究人员在 OpenSSL 中发现了一个严重的漏洞，OpenSSL 是一个保护互联网上许多网站的加密软件库。这对于普通用户来说意味着什么。



这里有很多技术信息和细微差别，但我们会尽量让它简单易懂。如果你更精通技术，我强烈推荐你在 这里阅读 [Heartbleed FAQ，它提供了关于这个问题的更多信息。](http://heartbleed.com/)

### 什么是 OpenSSL 和 Heartbleed？

OpenSSL 是 SSL 和 TLS 的开源实现，这两种协议可以保护你在网上看到的的大部分内容。最近，在 OpenSSL 中发现了一个已经存在两年多的严重错误，它可能允许互联网上的任何人发现您发送到一个看似安全的网站的名称、密码和内容。你可以想象，这是一件大事。(如果你对这个 bug 是如何工作的很好奇，看看我们的姐妹网站 Gizmodo 的 [这篇文章)。](https://gizmodo.com/how-heartbleed-works-the-code-behind-the-internets-se-1561341209)

### 哪些网站和服务受到影响？

众所周知，Heartbleed bug 会影响任何运行特定版本 OpenSSL (1.0.1 到 1.0.1f)的站点和服务。许多站点可能运行不容易受到攻击的旧版本 OpenSSL，并且许多站点可能已经更新到了一个固定版本。此外，并不是所有的网站和服务都使用 OpenSSL。例如，1Password 通过不同方式保护他们的信息。LastPass 使用 OpenSSL，容易受到攻击(直到今天早上)，但是由于在你的机器上发生的额外加密， [LastPass 说你的数据仍然是安全的](http://blog.lastpass.com/2014/04/lastpass-and-heartbleed-bug.html) 。

据估计，超过 66%的网站使用 OpenSSL，因此网站的很大一部分可能容易受到攻击。您可以使用 [这个工具](http://filippo.io/Heartbleed/) 来测试某些站点，尽管它不会回答一个站点在过去的任何时候是否容易受到攻击。你可以在这里 [找到受影响网站的列表](https://lifehacker.com/this-list-reveals-the-heartbleed-affected-passwords-to-1561755048) (更多信息见下文)。

### 我这个普通用户能怎么办？

不幸的是，你对此无能为力。解决这个问题的唯一方法是让易受攻击的站点更新 OpenSSL 并重新颁发它们的安全证书。

如果可能的话，尽量避免连接到易受攻击的站点和服务，直到它们通知您修复。在网站修复错误之前，更改密码不会有任何帮助，所以在更改密码之前，请等待您最喜欢的网站的确认。如果您得到确认， [照常审核并更新您的密码](https://lifehacker.com/how-to-audit-and-update-your-passwords-after-a-service-5712907) 。如果一个网站不是易受攻击的，但没有发布声明，请更改您的密码，以防它们在过去易受攻击。毕竟伤不了人。*更新:LastPass* [*现在有一个工具*](http://lifehacker.com/lastpass-now-tells-you-which-heartbleed-affected-passwo-1561522244) *可以让你知道什么时候要修改什么密码。Mashable 也有* [*一个好的服务列表*](https://lifehacker.com/this-list-reveals-the-heartbleed-affected-passwords-to-1561755048) *供检查。厉害！*

这只是对正在发生的事情以及它如何影响你的一个非常基本的概述。就像我们说的，如果你有点技术头脑， [这个 Heartbleed FAQ](http://heartbleed.com/) 有一些关于正在发生的事情的更多技术信息。除此之外，我们用户能做的最好的事情就是等待并保持警惕。