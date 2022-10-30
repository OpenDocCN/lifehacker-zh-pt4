# iPhone 有哪些加密选项？

> 原文:[https://life hacker . com/what-are-some-encryption-options-for-iphone-1487231923](https://lifehacker.com/what-are-some-encryption-options-for-iphone-1487231923)

你可以在 iPhone 上用你的标准邮件应用或应用商店的应用加密电子邮件，不需要越狱。苹果专家在 [*栈交换*](http://apple.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-97) *提供一些小技巧。*

Watch

最近，我开始更加认真地对待安全问题。现在，我有电子邮件自动签名和加密，我有他们的密钥。以前我只在必要的时候这样做，但我正试图培养一种改变的意识。我对 GPG 在雷鸟、Outlook 或安卓系统上使用 K9 邮件和 APG 没有意见，但我不知道如何在[**iOS**](https://lifehacker.com/how-to-jailbreak-your-iphone-the-always-up-to-date-gui-5771943)**上处理 GPG。**

我不能接受没有办法的说法——这似乎很荒谬，或者也许我处理问题的方式不对，有比 GPG 更合适的路线？

*见* [*原问题*](http://apple.stackexchange.com/q/99935/55778?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-97) *。*

#### 试试 S/MIME ( [由 zigg](http://apple.stackexchange.com/a/99947/21050?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-97) 回答)

PGP 是一个很棒的标准，有很多用途和很好的实现，但是如果你想简单地签名和加密电子邮件，我想你会发现 S/MIME 更受支持。许多邮件客户端(包括 iOS 和 OS X 上的股票邮件应用程序，以及其他流行的客户端，如微软 Outlook)可以处理 S/MIME [开箱即用](http://apple.stackexchange.com/questions/99935/email-encryption-options-on-an-iphone/99947#99947) ，无需任何附加组件。电子邮件证书由 CA 认证，就像 web 的 SSL 证书一样，而不是要求您依赖 PGP 可信 web 来认证其他人的证书并让他们认证您的证书。

可以从 [StartSSL](https://www.startssl.com/) 获得免费的 S/MIME 证书。一旦你创建了它，你可以从你的浏览器中导出它(确保使用密码！)，用电子邮件发给自己，然后在 iOS mail 应用程序中打开安装。然后，您的邮件帐户设置将提供选项来使用安装的证书对您的邮件进行签名和/或加密。(除了作为一个满意的非付费客户，我与 StartSSL 没有任何关系。)

#### 几个 PGP 选项(由 [吉尔比](http://apple.stackexchange.com/a/100201/43889?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-97) 和 [戴夫](http://apple.stackexchange.com/a/99936/46950?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-97) 回答)

试试 [iPGMail](http://ipgmail.com/) 。根据 iTunes 的描述:“iPGMail 是一个实现 OpenPGP 标准(RFC 4880)的应用程序，允许用户创建和管理公共和私有(RSA 和 DSA) PGP 密钥，并发送和接收 PGP 加密的邮件。”

另一个选项是 [oPenGP](https://itunes.apple.com/us/app/opengp/id414003727?mt=8) 。oPenGP 是一个在 iOS 设备上支持 OpenPGP 标准(RFC 4880)的解决方案。

<small>*编者按:这些答案都是从它们最初的形式中浓缩出来的。*T3】</small>

#### 一个另类( [由芝诺波博维奇](http://apple.stackexchange.com/a/100462/54779?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-97)回答)

做加密不一定需要程序。是的，如果你想要 PGP，你需要上面的一个程序。如果你想进行简单的签名和加密，只需获得一个证书(免费电子邮件证书可从 [科莫多](http://www.comodo.com/) 获得)并上传到手机上。

添加后，验证标记将出现在相应电子邮件地址的联系人卡片中。现在，您可以进入邮件帐户设置，并启用加密和签名。唯一的缺点是，你不能激活/停用每条消息。一旦激活/停用签名或加密，您必须重新启动邮件应用程序。如果你有一台 Mac/OSX，并且使用的是原生邮件应用程序，过程也是一样的。

<small>*不同意以上答案？有自己的专长可以贡献？查看*</small> [<small>*原帖*</small>](http://apple.stackexchange.com/q/99935/55778?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-97) <small>*，在*</small> [<small>*问不同的*</small>](http://apple.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-97) <small>*这是一个面向苹果爱好者和超级用户的问答网站。如果你有自己的苹果问题需要解决，请*</small> [<small>*提问*</small>](http://apple.stackexchange.com/questions/ask?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-97) <small>*。你会得到答案的。(而且是免费的。)*T39*T41】*</small>