# 如何在 Mac OS X 上安全擦除固态硬盘

> 原文：<https://lifehacker.com/how-to-securely-erase-a-solid-state-drive-on-mac-os-x-1580603733>

你的电脑有固态硬盘吗？所有新的苹果笔记本电脑都配有固态硬盘，如果你想擦除它，你最好小心点。“已清除”的内存实际上并未被清除；敏感信息可能会被窃取。苹果专家在 [*栈交换*](http://apple.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-119) *提供安全提示。*

Watch

我是 SSD 技术的新手，所以我不知道在安全擦除硬盘数据方面，它与硬盘相比如何。运行“磁盘工具”并使用“用零覆盖”选项抹掉驱动器就足够了吗，还是这只适用于硬盘驱动器？还有其他应该采取的行动吗？

我并不寻求 NSA 级别的安全性，但如果出售我的 Mac，我希望是安全的。

*见全文原问题* [*此处*](http://apple.stackexchange.com/q/6278/2184?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-119) *。*

### 全面的固态硬盘安全并不容易( [戈登·戴维孙](http://apple.stackexchange.com/a/6287/427?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-119) 回答)

不幸的是没有简单的答案，这真的取决于你的偏执程度。由于固态硬盘处理写入数据的方式，在固态硬盘上执行零一次并不像在硬盘上那样是一种好的删除数据的方法。

当您在硬盘上写入特定数据页时，新数据只是简单地覆盖旧数据，将其替换。如果你在整个磁盘上写零，所有的旧数据都将消失。另一方面，SSD 不能简单地覆盖单个页面。为了替换一个页面上的数据，必须先擦除旧数据，固态硬盘无法擦除单个页面；他们必须擦除由许多页组成的整个块。

因此，当您要求 SSD 覆盖(比如说)第 5 页时，SSD 会保留第 5 页上的数据，但将其标记为无效，分配另一个当前空白的页(比如说#2305)，将新数据写入第 2305 页，并记下下次操作系统请求第 5 页时，它应该得到#2305。原始的第 5 页数据会一直保留在那里，直到稍后驱动器需要更多空间时，才会将剩余的有效页从数据块中移出，并将其擦除。详见 [本次 AnandTech 综述](http://www.anandtech.com/show/2738) 。

最终结果是，如果您在“整个”驱动器上写入零，您实际上并没有覆盖所有的旧数据。你*已经*更新了控制器的转换表，所以它永远不会向操作系统返回任何旧数据，因为那些页面都被标记为无效。但是，如果有人有足够的兴趣绕过控制器，他们可以得到你的一些数据回来。

覆盖两次可能会有效，但这取决于控制器的分配策略。用随机数据(`diskutil randomDisk 2 /dev/diskN`)覆盖两次的可能性稍微大一点，但仍然不能保证。这两者都有一些不好的副作用:它们可能会稍微缩短驱动器的寿命，还会增加 SSD 上的逻辑碎片，降低其写入性能。

请注意，由于上述原因，OS X 图形磁盘工具的最新版本禁用了固态硬盘上的安全擦除选项，但命令行版本仍然允许它们。我也看到了一些通过将固态硬盘转换为加密格式来安全擦除固态硬盘的建议，但这(如果有的话)比用随机数据覆盖稍微不太安全。

安全擦除 SSD 的最佳方式是调用控制器的内置安全擦除功能。如果控制器设计者完成了他们的工作，这将真正擦除所有块，并且还具有重置逻辑页映射的副作用，实质上是对其进行碎片整理并恢复其原始性能。不幸的是，我见过的大多数这样做的工具(例如 [CMRR 的 HDDErase](http://cmrr.ucsd.edu/people/Hughes/Secure-Erase.html) )都在 DOS 下运行，在 Mac 上无法启动。一些用户 [MacRumors](http://forums.macrumors.com/showthread.php?t=841182) 提供了一些相当复杂的从 GParted 引导光盘进行安全擦除的指令。也有可能 [从](http://www.cnet.com/how-to/how-to-securely-erase-an-ssd-drive/) [可引导闪存盘](http://www.cnet.com/how-to/what-to-do-with-your-usb-flash-drive-maintain-windows/) 中使用 Parted Magic 。

UCSD 非易失性系统实验室的研究人员测试了各种消毒固态硬盘的方法，通过“擦除”驱动器，然后将其拆卸以绕过控制器，并检查残余数据(你可以阅读 [摘要](http://nvsl.ucsd.edu/sanitize/) 或 [全文](http://cseweb.ucsd.edu/users/swanson/papers/Fast2011SecErase.pdf) )。他们的结果与我上面所说的基本一致，同时也表明内置的安全擦除命令并不总是能正确执行:

> 我们的结果得出三个结论:第一，内置命令是有效的，但制造商有时会错误地实现它们。其次，覆盖 SSD 的整个可见地址空间两次通常(但并不总是)足以清理驱动器。第三，现有的面向硬盘驱动器的单个文件清理技术在 SSD 上都无效。

所以你有它；对大多数人来说，重写整个驱动器两次可能已经足够安全了，但是绝对的安全可能需要一些额外的努力。

* * *

从何而来有更多的答案。在 [<small>*原帖*</small>](http://apple.stackexchange.com/q/6278/2184?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-119) <small>*处查看或自行留下。在*</small> [<small>*问不同的*</small>](http://apple.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-119) <small>*找到更多喜欢的问题，一个面向苹果爱好者和超级用户的问答社区。如果你有自己的问题需要解决，请询问*</small>[<small></small>](http://apple.stackexchange.com/questions/ask?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=apple-119)*<small>*。你会得到答案的。(而且是免费的。)*</small>*

**<small>照片由</small>* [*<small>土田丰</small>*](https://www.flickr.com/photos/ivyfield/7072709381) *<small>。</small>**