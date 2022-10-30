# 使用不可信的 USB 驱动器有什么危险？

> 原文:[https://life hacker . com/what-is-the-dangers-of-use-an-trusted-USB-drive-1533523741](https://lifehacker.com/what-are-the-dangers-of-using-an-untrusted-usb-drive-1533523741)

u 盘、笔驱动、记忆棒——它们不一定像你想象的那样无害。在你插入一个你不是 100%信任的之前，想想可能会出什么问题(提示:很多)。超级用户在 [*栈交换*](http://superuser.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-107) *列举了几个非常现实的 USB 噩梦场景。*

Watch

假设有人想让我把一些文件拷贝到他们的 u 盘里。我运行的是打满补丁的 Windows 7 x64，禁用了自动运行(通过组策略)。我插入 USB 驱动器，在 Windows 资源管理器中打开它，并将一些文件复制到其中。我不运行或查看任何现有文件。如果我这么做，会发生什么不好的事情？如果我在 Linux(比如说 Ubuntu)上这么做呢？

*见原问题* [*此处*](http://superuser.com/q/709275/112560?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-107) *。*

#### 当心大拇指( [西尔瓦伊努尔](http://superuser.com/a/709659/36310?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-107)回答)

不太令人印象深刻的是，您的 GUI 文件浏览器通常会浏览文件来创建缩略图。在您的系统上运行的任何基于 pdf、基于 ttf(在此插入支持图灵的文件类型)的漏洞利用都有可能通过丢弃文件并等待缩略图渲染器扫描来被动启动。我所知道的大多数漏洞都是针对 Windows 的，但是不要低估了 libjpeg 的更新。

#### 真的是 USB 吗？( [由泰尔登](http://superuser.com/a/709302/151431?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-107) 回答)

可能发生的最坏情况只受攻击者想象力的限制。如果你有妄想症，那么将几乎任何设备物理连接到你的系统都意味着它可能会受到威胁。如果这个设备看起来像一个简单的 u 盘，就更是如此。

如果是这个呢？

上图是臭名昭著的 USB [橡皮鸭](http://www.usbrubberducky.com/) ，一个看起来像普通笔式驱动器但可以向你的电脑发送任意按键的小设备。基本上，它可以随心所欲，因为它将自己注册为一个键盘，然后输入它想要的任何顺序的键。有了那种访问权限，它就可以做 [各种龌龊的事情](https://forums.hak5.org/index.php?/topic/29959-payloads-duck-toolkit/) (这还只是我在谷歌上找到的第一个命中)。事情是可以脚本化的，所以前途无量。

#### 文件系统驱动不是没有 Bug 的( [由咱 Lynx](http://superuser.com/a/709393/4642?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-107) 回答)

另一个危险是 Linux 会尝试挂载任何东西(此处禁止开玩笑)。一些文件系统驱动程序不是没有错误的。这意味着黑客可能会在 squashfs、minix、befs、cramfs 或 udf 中找到漏洞。然后，黑客可以创建一个文件系统，利用该错误接管 Linux 内核，并将其放在 USB 驱动器上。这在理论上也可能发生在 Windows 上。FAT 或 NTFS 或 CDFS 或 UDF 驱动程序中的一个错误可能会为接管打开窗口。

#### 你确定不是自动运行的吗？( [由史蒂夫](http://superuser.com/a/709278/90061?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-107)回答)

有几个安全软件包允许我为 Linux 或 Windows 设置一个自动运行脚本，只要你一插入它，就会自动执行我的恶意软件。最好不要插入不信任的设备！

请记住，我可以将恶意软件附加到我想要的几乎任何类型的可执行文件中，并且适用于几乎任何操作系统。随着自动运行被禁用，你*应该*是安全的，但同样，我不信任我甚至有点怀疑的设备。

关于什么可以做到这一点的例子，请查看社会工程师工具包 (SET)。真正安全的*唯一的*方法是在拔掉硬盘的情况下启动一个实时 Linux 发行版。装上 u 盘，看一看。除此之外，你在掷骰子。正如所建议的，您必须禁用网络。如果你的硬盘是安全的，你的整个网络都受到威胁，那也没用。

*<small>不同意上面的一个答案？在</small>* [*<small>原问题</small>*](http://superuser.com/q/709275/112560?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-107) *<small>留下自己的答案或提交评论。更多问题请看</small>* [*<small>超级用户</small>*](http://superuser.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-107) *<small>，一个电脑爱好者和超级用户的问答网站。如果你有自己的电脑问题需要解决，请</small>* [*<small>提问</small>*](http://superuser.com/questions/ask?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-107) *<small>。你会得到答案的。(而且是免费的。)</small>*