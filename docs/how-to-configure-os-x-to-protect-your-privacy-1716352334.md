# 如何配置 OS X 来保护您的隐私

> 原文:[https://life hacker . com/how-to-configure-OS-x-to-protect-your-privacy-1716352334](https://lifehacker.com/how-to-configure-os-x-to-protect-your-privacy-1716352334)

安装一台新电脑已经够难的了，但是如果你很注重隐私，事情就更复杂了。Mac 电脑尤其如此，它把各种各样的东西都藏在幕后。无论你是在设置新系统还是安装新版本的 OS X，现在都是检查你的隐私设置的好时机。

Watch

我们都需要 [保护我们的私人数据](http://lifehacker.com/why-your-privacy-matters-even-if-youre-not-doing-anyt-1645884650#_ga=1.11571764.1835303237.1411253018) 。但是当 [你在处理敏感文件、图片和你的密码](https://lifehacker.com/from-saucy-pics-to-passwords-how-to-share-sensitive-in-5910408) 时，你要确保其他人不能轻易获取。除此之外，在 Mac 电脑上，如果你不小心的话，甚至像你的短信这样简单的事情也会突然出现在别人的面前。对于我们中的一些人来说，这可能感觉像是一个巨大的隐私问题，但谢天谢地，OS X 有大量的设置，你可以调整以锁定你的数据，搜索结果等。

### 审核 OS X 的系统设置

默认情况下，OS X 是所有关于易用性。这很好，但这意味着你的私人数据是公开的，任何人(或任何应用程序)都可以找到。在 OS X，很多默认行为都是为了让你的事情变得更简单，但这也意味着如果有人坐在你的电脑前，他们可能会无意中看到一大堆你可能不想让他们看到的东西。以下是一些值得调整的常规设置:

*   调整你的隐私系统偏好: OS X 有一个内置的隐私工具，值得定制..前往系统偏好设置>安全&隐私，选择隐私选项卡。在这里，您可以设置哪些应用程序可以访问您的位置数据、iCloud 数据，以及哪些应用程序可以访问深层系统内容(这列在可访问性下，但主要包括应用程序启动器和文本扩展程序等应用程序)。您可以在此批量禁用应用程序访问，也可以逐个应用程序禁用。
*   **打开 FileVault:** OS X 自带 [内置加密软件，名为 FileVault](http://lifehacker.com/a-beginners-guide-to-encryption-what-it-is-and-how-to-1508196946#_ga=1.123818122.1835303237.1411253018) 。当您打开它时，您需要登录密码或恢复密钥才能查看电脑上的任何数据。转至系统首选项>安全性&隐私，然后选择 FileVault 选项卡。打开它，它会加密你的整个驱动器。这个密码保护所有的东西，这使得没有你的密码，偷窥者很难访问你的数据。这也意味着你需要你的密码在任何时候，所以不要丢失它！
*   **不要用钥匙扣:**钥匙扣是苹果内置的密码系统。你必须用它来登录，但不要用它来浏览你的数据。只需您的登录密码，其他人就可以访问您电脑上储存的所有其他密码、网络驱动器、加密文件、应用程序密码等。相反，使用一个 [密码管理器，如 LastPass 或 1Password](http://lifehacker.com/lifehacker-faceoff-the-best-password-managers-compare-1682443320) ，它需要一个主密码(超出您的登录密码)才能使用。
*   **管理您的 iCloud 设置:** iCloud 是 OS X 的一大卖点，它与 iOS 的集成。iCloud 会同步您设备上的所有照片、文件和其他所有内容。如果您在共享电脑上，您可能想要完全停用 iCloud。只需进入系统偏好设置> iCloud，点击“注销”按钮。它会停止同步一切(这不太方便)，但至少你的数据不会那么容易被访问。也就是说，如果你还真的想用 iCloud，至少要确保你有 [双因素认证开启](http://lifehacker.com/apple-adds-two-factor-authentication-to-icloud-1598495741) 。
*   **禁用 iMessage 和 Facetime:** “连续性”是苹果的一大卖点。从 Mac 上，您可以发送和接收与 iPhone 同步的通话和文本。一个潜在的问题是，当其他人正在使用你的电脑(或从你的肩膀上偷看)时，你收到了一条你不想让他们看到的短信。除了查看带有信息的通知之外，他们还可以访问“信息”中的整个对话。如果这让你感到不安，你会想要禁用消息。打开“信息”,选择“信息”>偏好设置，然后注销您的 Apple ID。你也可以用 Facetime 打电话。
*   **禁用 Spotlight 网络搜索:**为了让 Spotlight 工作，它需要将你的搜索数据发送到谷歌、苹果和必应(无论你当时用的是哪一个。)没关系，但任何时候你用 Spotlight 搜索什么东西， [苹果也会收集这些数据。](http://lifehacker.com/safari-and-spotlight-can-send-data-to-apple-heres-how-1648453540) 。虽然苹果声称这是匿名的，但它仍然感觉有点令人毛骨悚然..要关闭它，进入系统偏好设置> Spotlight >搜索结果，取消 Spotlight 建议和 Bing 网络搜索的复选框。如果你仍然想要聚光灯的力量而不感到毛骨悚然， [我们推荐阿尔弗雷德](https://lifehacker.com/a-beginners-guide-to-mouseless-computing-with-alfred-1596198655) 。
*   **对 Spotlight 隐藏文件:**说到 Spotlight，您可能还想自定义它可以在哪里搜索文件。如果有人坐在您的电脑旁边，他们可以轻按 Command+Space 来搜索您电脑上的任何文件(也可以搜索文件内部)。当你自己在寻找某样东西时，这很棒，但也很容易让任何人窥探你。幸运的是，您可以定制这是如何工作的。前往系统偏好设置>聚光灯。在这里，您可以取消选中任何您不希望 Spotlight 显示的搜索结果的复选框。Spotlight 仍将索引这些文件，但它们不会显示在搜索结果中。您也可以点击隐私选项卡，添加您*不想让 Spotlight 索引的任何文件夹。这样，它们根本不会出现在搜索结果中。*

一旦所有这些设置都被调整，OS X 就完全被锁定了。。你会失去一些让 OS X 变得方便的功能，但至少你不会把私人数据交给坐在你电脑前的任何人(或任何应用程序)。

### 保护您的应用和数据

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-Lvem1Z66C7Q&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-Lvem1Z66C7Q&start=0) 

OS X 不会保护你下载的应用程序的数据，所以你需要自己保护。苹果确实试图确保你不会不假思索地安装任何东西，并有工具来限制你安装未签名的应用程序——但一旦它们被安装，OS X 认为你知道你在做什么。关心你的网上隐私是确保你这样做的一大步 ，但是你也可以做一些其他的事情。

*   下载保护隐私的浏览器扩展:你可能会花很多时间上网，所以锁定你的浏览习惯是值得的。安装浏览器扩展，如 [AdBlock Plus](https://adblockplus.org/) 、 [Disconnect](https://disconnect.me/) 、 [其他隐私保护扩展](http://lifehacker.com/the-best-browser-extensions-that-protect-your-privacy-479408034#_ga=1.88429406.431406394.1415821409) 来保护您的数据安全。
*   **使用 VPN** :虚拟专用网络 [有助于保护你的隐私](http://lifehacker.com/why-you-should-be-using-a-vpn-and-how-to-choose-one-5940565#_ga=1.92313560.431406394.1415821409) 。设置 VPN 可以确保你的浏览流量被加密，如果你用的是 MacBook，并且在咖啡店或其他有不安全 Wi-Fi 网络的地方工作，这一点尤为重要。
*   **仅允许批准的应用:**互联网上充斥着数十亿个应用，其中一些可能会带有恶意软件、间谍软件或其他恶意代码。[MAC 和](http://lifehacker.com/bundled-crapware-has-come-to-macs-so-hone-your-bs-dete-1688207772) 没什么不同。苹果确实提供了只安装已经提交、审核并添加到 Mac App Store 的可信应用的选项，但如果你关闭了这个选项，你需要特别小心。要启用此功能，请转至系统首选项>安全性&隐私，然后选择常规选项卡。您会看到一个选项“允许从以下位置下载应用程序”选中 Mac App Store 旁边的复选框。这意味着只能安装经过批准和签名的应用程序。如果你认为自己比这更聪明一点，你也可以选择“Mac 应用商店和确定的开发者”选项。

当然，这只是你能做的最起码的事情。某些注重隐私的网络浏览器也很有用 [，因为隐名模式](http://lifehacker.com/dont-trust-private-browsing-modes-for-true-privacy-5608123#_ga=1.122509006.431406394.1415821409) 对隐私来说并不是最好的。你也可以远离谷歌，将你的默认搜索引擎 改为类似于 [DuckDuckGo](https://duckduckgo.com/) 的搜索引擎，这样有助于让你的浏览更加私密。安装 [一个杀毒 app 也是个好主意](https://lifehacker.com/the-best-antivirus-app-for-mac-488021445) 。尽管我们都被告知 MAC 电脑没有病毒问题，但你仍然面临跨平台浏览器和基于网络的漏洞(例如，在 Flash 和 Java 中)，你也不想无意中通过共享文件或附件传播 Windows 恶意软件，所以最好是安全的。

### 锁定对您计算机的物理访问

锁定你电脑上的数据只是成功的一半。苹果最受欢迎的电脑是笔记本电脑，这意味着封锁对你电脑的物理访问也是至关重要的。

*   **启用锁屏**:进入系统首选项>安全&隐私，选择常规选项卡。选中“需要密码”和“停用自动登录”旁边的复选框，以确保需要密码才能访问您的电脑。
*   **隐藏用户账户**:默认情况下，当你进入锁屏时，你会看到系统上不同用户账户的选项。理论上有人可以坐在那里，一遍又一遍地猜测你的密码，如果他们愿意的话。如果你想要另一层安全，你可以隐藏它，这样你必须输入用户名*和*密码才能登录。一旦你启用了这个，你将不得不每次都登录。从终端输入:`sudo dscl . create /Users/hiddenuser IsHidden 1`
*   **创建一个访客账户**:当你需要把电脑交给朋友使用时，最好创建一个访客账户，这样他们就不会无意中窥探你的东西。进入系统首选项>用户&组，点击访客用户选项。选中“允许客人登录到这台电脑”旁边的框如果您启用了 FileVault，客人只能访问 Safari，这可能是他们真正需要的。
*   **保护你的 Wi-Fi** :最后，你还需要确保你家里的 Wi-Fi 是安全的，这样邻居和路人就无法窥探你的数据。保持你的 [Wi-Fi 安全很容易](https://lifehacker.com/the-most-important-security-settings-to-change-on-your-1573958554) ，一旦你设置好了，你真的不需要再考虑它。

有了这些，你的电脑应该既安全又能保护你的大部分数据。当然，没有绝对安全的，但至少你让人们更难访问你的数据。或者，在 OS X 的情况下，你让一些随机的路人或不可信的应用程序不只是偶然偷听你。

[Open *kinja-labs.com*](http://kinja-labs.com/related-widget/?posts=1582572323,1688207772,1645884650&title=Rethink Your Privacy Policy)