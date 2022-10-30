# 五个最好的文件加密工具

> 原文:[https://life hacker . com/five-best-file-encryption-tools-5677725](https://lifehacker.com/five-best-file-encryption-tools-5677725)

保证你个人数据的安全并不一定很难——只要你把敏感的东西加密并且在你的控制之下。这就是为什么本周我们来看看五个最好的文件加密工具，你可以用它们来加密你的本地数据，这样只有你才有密钥。

Watch

本周早些时候，我们向你询问了你最喜欢的文件加密工具，你给了我们很多很棒的提名，但和往常一样，我们只有前五名的位置。

就我们的综述而言，我们将重点放在桌面文件加密工具上——你在自己的电脑上用来加密自己的私人数据的工具，而不是承诺加密你的数据的云服务，或声称提供加密的商业服务。这里的目标是找到您可以用来锁定您的敏感文件的最佳工具，无论它们是照片、财务文档、个人备份还是其他任何东西，并保持锁定，这样只有您拥有钥匙。对于那些不熟悉这个话题的人，我们有 [一个关于加密如何工作的伟大指南](https://lifehacker.com/a-beginners-guide-to-encryption-what-it-is-and-how-to-1508196946) ，以及你如何使用它来保护你自己的数据安全。

抛开这些不谈，以下是你的前五名，排名不分先后:

### [VeraCrypt](https://veracrypt.codeplex.com/)(Windows/OS X/Linux)

VeraCrypt 是 TrueCrypt 的一个分支，也是它的继承者，TrueCrypt 于去年停止了开发(稍后将详细介绍)。)开发团队声称，他们已经解决了 TrueCrypt 初始安全审计期间提出的一些问题，而且像最初一样，它是免费的，有适用于 Windows、OS X 和 Linux 的版本。如果你正在寻找一个文件加密工具，它的工作方式和 TrueCrypt 类似，但又不是真正的 TrueCrypt，这就是你要找的。VeraCrypt 支持 AES(最常用的)、TwoFish 和 Serpent 加密密码，支持在其他卷内创建隐藏的加密卷。它的代码可供审查，尽管它不是严格意义上的开源(因为它的大部分代码都来自 TrueCrypt。)该工具也在不断开发中，定期进行安全更新，并在规划阶段进行独立审计(据开发者称。)

那些提名 VeraCrypt 的人称赞它是一个即时加密工具，因为你的文件只有在需要时才被解密，其他时间都是加密的，最值得一提的是它是 TrueCrypt 的精神(如果不是字面上的)继承者。你们中的许多人称赞它们是一个强大的工具，简单易用，切中要害，即使它缺乏好看的界面或大量的花哨功能。您还注意到，VeraCrypt 可能不支持 TrueCrypt 文件和容器，但是可以将它们转换成自己的格式，这使得移植变得容易。更多 [可以在](http://lifehacker.com/vote-veracrypt-why-essentially-the-same-as-truecrypt-1683931320) 的提名帖中阅读。

* * *

### [AxCrypt](http://www.axantum.com/AxCrypt/) (Windows)

AxCrypt 是一个免费的、开源的、GNU GPL 许可的 Windows 加密工具，它以简单、高效和易于使用而自豪。它与 Windows shell 很好地集成在一起，所以您可以右键单击一个文件对其进行加密，甚至可以配置“定时的”可执行加密，这样文件就被锁定了一段特定的时间，以后会自行解密，或者当它的目标接收者得到它时。使用 AxCrypt 的文件可以按需解密或在使用时保持解密，然后在修改或关闭时自动重新加密。它的速度也很快，允许你选择整个文件夹或一大组文件，只需点击一下就可以全部加密。然而，它完全是一个文件加密工具，这意味着创建加密的卷或驱动器超出了它的能力。它仅支持 128 位 AES 加密，提供针对暴力破解尝试的保护，并且非常轻量级(小于 1MB。)

提名 AxCrypt 的人注意到，由于它的 shell 支持，它真的很容易使用，也很容易集成到您的工作流中。如果你渴望更多的选项，它也有大量的命令行选项，所以你可以在 Windows 中启动命令提示符，执行更复杂的操作——或者一次执行多个操作。它可能不支持可用的最强或最多样的加密方法，但如果你想让你的数据免受大多数威胁，它是一个简单的工具，可以提供一点安全性，让你的数据——比如存储在 Dropbox 或 iCloud 上的云文件——同时安全*和*方便访问。更多 [你可以在此处](http://lifehacker.com/vote-axcrypt-why-it-is-a-free-and-open-source-program-1684045012) 和 [此处](http://lifehacker.com/vote-axcrypt-why-easy-to-use-ui-plus-command-line-int-1683947844) 阅读这个提名线程。

* * *

### (Windows)

BitLocker 是一种全磁盘加密工具，内置于 Windows Vista 和 Windows 7(旗舰版和企业版)、Windows 8(专业版和企业版)以及 Windows Server (2008 及更高版本)中。它支持 AES (128 和 256 位)加密，虽然它主要用于整个磁盘加密，但它也支持加密其他卷或虚拟驱动器，可以像电脑上的任何其他驱动器一样打开和访问。它支持多种认证机制，包括传统的密码和 pin 码、USB“密钥”，以及更具争议的 [可信平台模块](http://en.wikipedia.org/wiki/Trusted_Platform_Module) (TPM)技术(使用硬件将密钥集成到设备中)，该技术使加密和解密对用户透明，但也带来了许多自身的问题。无论如何，BitLocker 与 Windows(特别是 Windows 8 Pro)的集成使许多人都可以访问它，对于希望在笔记本电脑或硬盘丢失或被盗的情况下保护数据的个人或希望在现场保护数据的企业来说，BitLocker 是一种可行的磁盘加密工具。

当然，不言而喻，BitLocker 是一个有争议的提名。你们中的许多人吹捧 BitLocker 的可访问性和易用性，你们中的许多人甚至称赞它的加密强大而难以破解。你们中的许多人注意到，在 TrueCrypt 的开发者建议之后，你们改用了 BitLocker。然而，其他人提出了隐私倡导者的断言，即 BitLocker 受到了威胁，并为政府安全机构(来自多个国家)提供了后门来解密你的数据。虽然微软官方表示这不是真的，并坚称 BitLocker 没有后门(同时保持代码为封闭源代码，但可供其合作伙伴(包括这些机构)审查)，但这一说法足以让很多人回避。你可以在上面的维基百科链接中阅读更多关于批评和争议的内容，或者在提名主题 中阅读 [。](http://lifehacker.com/vote-bitlocker-why-its-been-built-in-to-windows-since-1683931763)

* * *

### [GNU 隐私卫士](http://www.gnupg.org/) (Windows/OS X/Linux)

GNU 隐私卫士(GnuPG)实际上是 [相当不错的隐私](http://en.wikipedia.org/wiki/Pretty_Good_Privacy) (PGP)的开源实现。虽然你可以在一些操作系统上安装命令行版本，但大多数人会从 [几十个前端和图形界面](https://www.gnupg.org/related_software/frontends.html) 中选择，包括官方发布的可以加密从电子邮件到普通文件到整卷文件的一切。所有 GnuPG 工具都支持多种加密类型和密码，并且通常能够一次加密一个单独的文件、磁盘映像和卷，或者外部驱动器和连接的介质。你们中的一些人在不同的线程中指定了特定的 GnuPG 前端，比如 Windows[gpg 4 win](http://www.gpg4win.org/)，它使用 Kleopatra 作为证书管理器。

那些提名 GnuPG 的人称赞它是开源的，可以通过几十种不同的客户端和工具访问，所有这些都可以提供文件加密以及其他形式的加密， [例如健壮的电子邮件加密](https://lifehacker.com/how-to-encrypt-your-email-and-keep-your-conversations-p-1133495744) 。然而，关键是找到一个前端或客户端来做你需要它做的事情，并与你的工作流程很好地合作。上面的截图是使用 [GPGTools](https://gpgtools.org/gpgsuite.html) 拍摄的，这是一个一体化的 GnuPG 解决方案，为 OS X 提供钥匙串管理以及文件、电子邮件和磁盘加密。你可以在这里 的提名线程中阅读更多 [。](http://lifehacker.com/gnupg-is-a-complete-and-free-implementation-of-the-open-1683952225)

* * *

### [7-Zip](http://www.7-zip.org/)(Windows/OS X/Linux)

7-Zip 实际上是一个轻量级的文件归档器——也是我们最喜欢的用于 Windows 的归档工具。尽管它在压缩和组织文件以便于存储或通过互联网发送方面令人惊叹，但它也是一种强大的文件加密工具，能够将单个文件或整个卷转换为只有您拥有密钥的加密卷。它完全免费，即使用于商业用途，支持 256 位 AES 加密，虽然官方下载仅适用于 Windows，但也有针对 Linux 和 OS X 系统的非官方版本。7-Zip 的大部分代码都是 GNU LGPL 许可的，并且可以公开审查。压缩加密. 7z(或者。zip，如果你喜欢的话)存档是易于携带和安全的，可以用密码加密，并转换成可执行文件，当它们到达预定的接收者时会自动解密。7-Zip 还与您正在使用的操作系统的外壳集成在一起，使它通常只需点击一下就可以使用。它也是一个强大的命令行工具。

提名它的人注意到它可能没有最健壮的用户界面，但它完成了工作，而且你们中的许多人已经安装了它，特别是因为它健壮的文件压缩和解压缩功能。您注意到它快速、灵活、免费且易于使用，虽然它可能不是最快的文件加密工具(并且它不能进行全卷或磁盘加密)，但它可以完成工作，尤其是对于加密您需要发送给其他人的文件，并且实际上让他们能够访问而无需经过太多的麻烦。你们中的一些人注意到 7-Zip 的加密卷是灵活的——也许太灵活了，因为添加到加密存档中的新文件是不加密的(你必须将它们全部提取出来，并为此创建一个新的存档),但这只是一个小问题。更多 [可以在](http://lifehacker.com/7-zip-windows-free-light-and-useful-for-some-users-1683940374) 的提名帖中阅读。

* * *

现在您已经看到了前五名，是时候让他们全力以赴投票决定社区的最爱了。

* * *

#### 荣誉奖

本周我们有两项荣誉奖。首当其冲的就是 [**磁盘实用程序**](http://en.wikipedia.org/wiki/Disk_Utility) (OS X)，这是 OS X 捆绑的一个磁盘修复和管理工具。“磁盘工具”还可以加密驱动器和宗卷，由于 OS X 只需右键单击一个文件、一系列文件或一个文件夹并选择“压缩”，就可以创建压缩宗卷，“磁盘工具”使加密任何您想要的东西变得极其容易。此外，它内置于 OS X，所以你不需要安装任何其他东西。你可以在 [这里](http://lifehacker.com/vote-disk-utility-why-its-always-available-and-integr-1683940571) 阅读更多关于它的提名线索。

其次，我们应该向德高望重的老[**【TrueCrypt】**](http://en.wikipedia.org/wiki/TrueCrypt)致敬，我们的老冠军，它实际上在竞争者线程的调用中获得了许多提名。当 TrueCrypt 崩溃时，我们报道了它，开发者突然放弃了这个项目，声称它不再安全，在他们独立的安全审计中。开发人员建议改用 BitLocker，并推出了一个被广泛认为是折衷的新版本。然而，更老的版本 7.1a 仍然被广泛认为是安全的，尽管对它的开发已经被放弃，并且该工具从那时起就没有安全更新。即便如此，安全分析师在是否应该信任 TrueCrypt 或转向另一种加密工具的问题上存在分歧。许多人袖手旁观它，即使它是一个死项目，其他人已经在它的基础上构建了自己的项目(参见前面提到的 VeraCrypt)，其他人继续使用上一个安全版本。我们自己不能再推荐 TrueCrypt 了，但是你可以在这里 的提名帖中阅读更多的 [，以及在](http://lifehacker.com/vote-truecrypt-why-still-awesome-see-steve-gibsons-t-1683996272) [Steve Gibson 关于 TrueCrypt 的页面这里](https://www.grc.com/misc/truecrypt/truecrypt.htm) 。

对其中一个竞争者有什么要说的吗？想为你的个人最爱辩护吗，即使它不在列表中？*记住，前五名是基于本周早些时候*的 [*你最受欢迎的提名。不要只抱怨前五名，在下面的讨论中让我们知道你更喜欢的选择是什么——并提出你的理由。*](https://lifehacker.com/whats-the-best-file-encryption-tool-1683834660)

*<small>《蜂巢 5》基于读者提名。与大多数 Hive Five 帖子一样，如果你最喜欢的帖子被遗漏了，它就没有获得呼吁竞争者帖子中所需的提名，从而进入前五名。我们知道这有点像人气竞赛。对蜂巢五有什么建议？发送邮件至</small>*[*<small>tips+hivefive@lifehacker.com</small>*](mailto:tips+hivefive@lifehacker.com)*<small>！</small>T15】*

*<small>标题照片由</small>*[*<small>andrey _ l</small>*](http://www.shutterstock.com/pic-148619159/stock-photo-key-with-password.html?src=id&ws=1)*<small>(Shutterstock)。</small>T15】*