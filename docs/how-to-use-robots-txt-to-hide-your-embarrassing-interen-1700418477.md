# 如何使用 Robots.txt 隐藏你的哑博客

> 原文:[https://gizmodo . com/how-to-use-robots-txt-hide-your-hanging-interen-1700418477](https://gizmodo.com/how-to-use-robots-txt-to-hide-your-embarrassing-interen-1700418477)

完全从网上删除一些东西 就像把喝醉的野鹅放出来关在笼子里:几乎不可能。但是有办法隐藏你不想让任何人看到的网页内容。你可以用搜索引擎的“禁止入内”标志隐藏各种网页:一个叫做 robots.txt 的特殊文件。

Watch

robots.txt 文件充当快捷方式，将内容埋藏得很深，很难挖掘出来。正如 BuzzFeed 最近展示的 [一样，当它试图隐藏被删除的批评其广告商](http://tktk.gawker.com/buzzfeed-deleted-anti-hasbro-post-after-inking-deal-wit-1697044663#_ga=1.139442096.2070985228.1428681399) 属性的帖子时，robots.txt 是一个相当有效的掩盖工具。如果你想逃避你发表的东西的责任，这个文件会部分隐藏你的踪迹。互联网的记忆是长的，robots.txt 是遗忘协议。

BuzzFeed 使用 robots.txt 让人们更难找到一些关于 Dove 和 Monopoly [的帖子，因为编辑失误，BuzzFeed 删除了](http://tktk.gawker.com/buzzfeed-deleted-anti-hasbro-post-after-inking-deal-wit-1697044663) 。通过在 robots.txt 目录中添加这些幽灵帖子的网址，它阻止了旧版本出现在在线搜索中。这并不意味着帖子完全消失了。人们总是可以通过挖掘你的 robots.txt 文件来查看你隐藏了什么，所以完全删除你的帖子是无效的。但它让联合利华的高管无法找到被删除的 Dove 评论，除非他们专门翻遍 BuzzFeed 的 robots.txt 目录。

那么它是如何工作的呢？像 Google、Bing 和 Yahoo 这样的搜索引擎通常会缓存旧版本的网页，这意味着很容易就能找到已删除帖子的副本。互联网档案馆的回溯机也将已逝帖子的副本存档，保存数字记录。总的来说，这种保存的习惯对于保护数字历史是一个福音。但是当你想忘记一些事情时，这种记录的倾向就成了一个问题。

然而，Google、Bing、Yahoo、Wayback Machine 和其他各种搜索机器人会听从你的命令而不做记录。搜索引擎使用的大多数机器人会立即查找 robots.txt 文件的存在，并会遵守指令来排除内容。

对于一个专业媒体公司来说，自我审查是见不得光的，但是亲爱的读者，也许你有更好的理由。制作一个 robots.txt 文件来隐藏你可耻的功勋 [非常容易](http://seoroi.com/seo-faq/robotstxt-what-it-is-why-its-used-and-how-to-write-it/) 。您打开一个文本编辑器，键入以下内容:

> <small>用户代理:</small>
> 
> <small>不允许:</small>

然后用您想要禁止的内容对其进行自定义，并将其保存为. txt 文件。使用小写字母表示“机器人”并为每个排除使用单独的“不允许:”命令是很重要的。

例如，对于 Wayback 机器来说，你写这个 [，它会回溯性地清理你的页面](http://archive.org/about/exclude.php) :

> 用户代理:ia_archiver
> 
> 不允许:/

之后，你把文件上传到你的域的根目录(必须是主目录)。如果您不能直接访问该目录，请联系您的网站管理员。您还可以设置只隐藏一个特定帖子的命令，或阻止多个爬网程序搜索的命令。

这不仅有助于隐藏博客中令人尴尬的冒险，也有助于隐藏受密码保护的页面和敏感信息。电子商务服务可以使用 robots.txt 来隐藏包含客户个人数据的数据库。

一些网站的 robots.txt 文件很有创意——Yelp[包括指令](http://yelp.com/robots.txt) 作为一个内部笑话，机器人变得有知觉的可能性很小。网站管理员可能会在 robots.txt 中包含方向，以帮助他们的网站更快地被抓取，因此它既是一个告诉机器人不要插手的工具，也是一个引导机器人的工具。

大多数时候，人们试图让他们的互联网内容被发现。但是自 1994 年就出现的 robots.txt 强调了一种持久的愿望，即控制我们放在网上的东西如何传播。当媒体公司收回他们发布的内容时，它会引起人们对这个工具如何被用于掩盖真相的关注。然而，人们希望有机会限制受众的原因有很多，而一种工具的存在让制作者在网上发现和记住什么方面拥有更大的权力是一件好事。

【[SEO ROI](http://seoroi.com/seo-faq/robotstxt-what-it-is-why-its-used-and-how-to-write-it/)||[Yoast](https://yoast.com/wordpress-robots-txt-example/)||[认知 SEO](http://cognitiveseo.com/blog/7052/critical-mistakes-in-your-robots-txt-will-break-your-rankings-and-you-wont-even-know-it/)||[Google](https://support.google.com/webmasters/answer/6062596?hl=en)

吉姆·库克的插图

* * *

<small>*联系作者在*</small>[<small></small>](mailto:kate.knibbs@gizmodo.com)*<small>*。*</small>
[<small>*公共 PGP 密钥*</small>](https://pgp.mit.edu/pks/lookup?op=get&search=0x8C129478EE0710CD)
<small>*PGP 指纹:FF8F 0D7A AB19 6d 71 C967 9576 8c 12 9478 EE07 10C*</small>*