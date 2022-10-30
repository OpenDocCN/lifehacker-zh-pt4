# 创建一个 USB 密码窃取器，看看你的信息到底有多安全

> 原文:[https://life hacker . com/create-a-USB-password-stealter-to-see-how-secure-your-I-1650354166](https://lifehacker.com/create-a-usb-password-stealer-to-see-how-secure-your-i-1650354166)

在密码安全上的松懈会带来可怕的后果。即便如此，还是很容易忘记有多少人容易受到攻击。只需几个文件，你就可以从受害者的 Windows PC 上几乎任何地方窃取密码，包括你自己的，只是为了看看它们到底有多安全。

Watch

*这篇文章是我们 Lifehacker 的* [*邪恶周*](https://lifehacker.com/welcome-to-lifehackers-fifth-annual-evil-week-1647621043) *系列的一部分，在这里我们看到了做事的阴暗面。知道邪恶意味着知道如何打败它，所以你可以用你的邪恶力量做好事。想要更多吗？查看我们的* [*恶周标签页*](http://lifehacker.com/tag/evilweek) *。*

一个很好的经验法则是，如果你在你的电脑上存储了一个密码，你就让其他人有可能用一个 USB 闪存驱动器和一个点击脚本这样简单的东西来窃取。这包括您保存在浏览器 中的从 [无线网络密钥](https://lifehacker.com/how-to-hack-your-own-network-and-beef-up-its-security-w-1649785071) 到 [密码的所有内容。](http://lifehacker.com/easily-reveal-hidden-passwords-in-any-browser-5946529) [《黑客手册》](http://hackershandbook.org/tutorials/usb-password-stealer) 对更有经验的用户来说是一个很好的指南，但是我们将在这里对初学者进行分解:

## **第一步:收集你的工具**

NirSoft 开发了很多我们喜欢的工具 ，他们有一套非常好的安全工具。我们将使用一些恢复密码的工具来创建我们的终极 USB 工具。

插入 USB 驱动器，创建一个名为“实用工具”的文件夹。然后，从 [NirSoft 密码恢复实用程序页面](http://www.nirsoft.net/utils/index.html#password_utils) 下载以下 zip 文件(不是自安装的可执行文件)到 u 盘上，解压文件后，将所有的。实用程序文件夹中的 exe 文件:

*   密码恢复
*   邮件通行证视图
*   受保护的存储通行证视图
*   拨号通道
*   BulletsPassView
*   网络密码恢复
*   密码嗅探器
*   RouterPassView
*   PST 密码
*   密码查看器
*   无线网络密
*   远程桌面通行证视图
*   VNCPassView

这些可执行文件中的每一个都从计算机上的特定位置恢复密码。例如，WirelessKeyView.exe 拔出你的无线钥匙，WebBrowserPassView.exe 获取你浏览器中存储的所有密码。如果你想详细了解每一个的功能，可以查看上面链接的 NirSoft 页面。如果你看到任何其他你想尝试的密码恢复工具，也下载它们，但是我们这里有一个很好的起点。

## **第二步:自动化工具，一键操作(仅限 XP 和 Vista】**

接下来，我们将设置一个脚本，一次运行所有这些实用程序，让您只需单击一下就可以获取存储密码的巨大缓存(虽然它只能在 Windows XP 和 Vista 上正常工作，所以如果您只在 Windows 7 和更高版本上使用它，可以跳过这一步)。打开文本编辑器，对于下载的每个文件，在一个文本文件中写入以下代码行:

```
start filename /stext filename.txt 
```

将“文件名”替换为您刚刚下载的可执行文件的名称，包括文件扩展名。当您在斜杠后替换“filename”时，您将更改。文件扩展名为. txt。这是可执行文件将为您创建的密码日志。完成的脚本应该是这样的:

```
start mspass.exe /stext mspass.txt start mailpv.exe /stext mailpv.txt<br>start pspv.exe /stext pspv.txt start Dialupass.exe /stext Dialupass.txt start BulletsPassView.exe /stext BulletsPassView.txt start netpass.exe /stext netpass.txt start sniffpass.exe /stext sniffpass.txt start RouterPassView.exe /stext RouterPassView.txt start PstPassword.exe /stext PstPassword.txt start WebBrowserPassView.exe /stext WebBrowserPassView.txt start WirelessKeyView.exe /stext WirelessKeyView.txt start rdpv.exe /stext rdpv.txt start VNCPassView.exe /stext VNCPassView.txt 
```

编写完脚本后，将文件保存为您创建的 Utilities 文件夹中的 Launch.bat。

## **第三步:测试你的新密码窃取者**

现在，您将能够从这些程序中恢复用户名和密码。他们会创建详细的日志，向您显示密码、用户名和来源(如网络名称或网站 URL)，这是您真正需要进行破坏的所有内容。还有密码的创建日期、密码强度和其他取决于程序的信息。以下是如何测试你的新密码窃贼，看看你有多少密码留在你的电脑上易受攻击。

#### **XP 和 Vista:运行脚本**

单击刚才创建的 launch.bat 文件来启动它。密码日志将在实用程序文件夹中显示为。txt 文件以及原始的可执行文件。每个都将与。exe 文件。例如:ChromePass.txt 文件将有一个 ChromePass.txt 文件，其中包含所有恢复的密码和用户名。你要做的就是打开。txt 文件，你会看到你所有的密码。

#### **Windows 7 及以上版本:单独运行每个密码恢复应用**

如果你使用的是 Windows 7 或更高版本，这个脚本对很多应用程序都不起作用，所以你需要单独打开它们。双击每个程序，密码列表将在一个窗口中弹出。选择您想要保存的所有内容，转到文件菜单，将日志作为. txt 文件保存在您在闪存驱动器上创建的原始实用程序文件夹中。

使用这些日志来看看你的系统中有多少密码是易受攻击的。找到并拿走它们非常容易！

## **第四步:保护自己**

现在你知道你的信息是多么的脆弱，开始认真保护你自己吧。采取以下预防措施:

*   如果您的电脑启用了自动运行，请选择 [禁用](http://lifehacker.com/disable-autorun-to-stop-50-of-windows-malware-threats-30802685) 。只需要几行代码就可以设置。bat 文件在闪存盘插入时自动启动，用户甚至看不到发生了什么。
*   采取一些措施，比如不要让你的浏览器记住你的密码，或者至少是像手机银行这样重要的密码。相反，使用加密的密码管理器，如 [LastPass](http://lifehacker.com/the-intermediate-guide-to-mastering-passwords-with-last-5645162) 或 [另一个好的密码管理器](http://lifehacker.com/the-five-best-password-managers-5529133) 来安全地存储你所有的密码。
*   一有机会就使用 [双因素认证](http://lifehacker.com/please-turn-on-two-factor-authentication-5932700) 。如果黑客想得到你的信息，他们有很多方法。第二个因素——你所拥有的东西——可能最终会拯救你。
*   显而易见的是:尽可能保持对电脑的物理控制。永远不要让你的电脑无人看管 给任何人，尤其是使用 u 盘的人。事实上，当朋友问他们是否可以用你的电脑时，尽可能多地主动提出自己做这项工作不会有什么坏处。

强密码不是你需要的所有保护。了解你的信息到底有多脆弱，建立一个 [近乎防黑客攻击的密码系统](https://lifehacker.com/how-to-build-a-nearly-hack-proof-password-system-with-5879117) 来保证安全。

*<small>照片由</small>*[*<small>SamahR</small>*](https://flic.kr/p/61iZ19)*<small></small>*<small>[*Chris Yarzab*](https://flic.kr/p/cXCmnm)*，以及*[*<small>Ervins Strauhmanis</small>*](https://flic.kr/p/nTqdJf)<small>*。*</small></small>

<small></small>