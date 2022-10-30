# 你可以用 Adblock Plus 做的一切(不仅仅是阻止广告)

> 原文:[https://life hacker . com/everything-you-can-do-with-adblock-plus-than-is-t-jus-1469861264](https://lifehacker.com/everything-you-can-do-with-adblock-plus-that-isn-t-jus-1469861264)

[【Adblock Plus】](https://adblockplus.org/)是最强大的浏览器扩展之一，虽然与其同名是其最常用的功能，但它不仅仅是阻止广告。事实上，你可以用它做各种事情，包括清理脸书的界面，确保网站不会跟踪你。

Watch

屏蔽广告不支持像我们这样创建免费内容的网站，所以在 Adblock Plus 中将你真正喜欢的网站列入白名单总是一个好主意。这是一个 [的简单过程](https://adblockplus.org/en/acceptable-ads) ，只需要几秒钟。

### 清理脸书丑陋、混乱的界面

脸书杂乱无章，很难读懂。这在很大程度上是因为屏幕右侧令人讨厌的侧边栏，但事实上，游戏、广告、电视节目收视率和其他无意义的内容被添加到你的新闻提要中，这意味着无论如何都很难阅读脸书。

值得庆幸的是，Adblock Plus 允许您通过三个简单的设置来切断与脸书的联系。你可以屏蔽来自你的新闻源和/或侧边栏的烦恼。你所需要做的就是安装了 Adblock Plus 的 [到这里](http://facebook.adblockplus.me/) ，选择最适合你的选项。一旦你做出选择，点击“+添加”按钮，你的脸书饲料将一如既往地干净。当然，如果这对你来说还不够，你可以随时 [用 Social Fixer](https://lifehacker.com/how-to-make-facebook-infinitely-better-with-one-browser-5892826) 定制脸书，真正获得你想要的体验。

### 给 YouTube 一个最小的改造

YouTube 非常难看，屏幕上有太多不同的选项，通常很难找到你想要的。如果你厌倦了令人讨厌的侧边栏、可怕的评论区和社交整合，Adblock Plus 可以摆脱它们。

你需要做的就是点击 进入 [YouTube 定制页面。然后你可以选择你想在 YouTube 上屏蔽什么类型的内容:只是评论、建议、视频注释或一切。它基本上把 YouTube 变成了一个漂亮的、最小的视频播放器，不会让你陷入相关内容的兔子洞。](http://youtube.adblockplus.me/en/)

### 隐藏 Twitter 图片预览

Twitter 最近开始自动在推文中包含图片。这包括你所关注的人的图片和视频以及广告。这实际上很好，但如果你喜欢更薄的纯文本布局， [Adblock 增加了一种阻止那些图像的方法](https://adblockplus.org/blog/how-to-get-rid-of-the-new-photo-preview-feature-on-twitter) 。

你需要做的就是添加几个自定义过滤器(右击 ABP 标志，选择选项>添加你自己的过滤器):

**块图像:**

```
twitter.com ##.tweet .media > .media-thumbnail.is-preview > img<br>
```

**屏蔽视频:**

```
twitter.com##.js-stream-tweet > .content > .expanded-content > .tweet-details-fixer > .js-media-container[data-card2-name="player"]
```

现在，那些讨厌的图像和视频将再次被隐藏起来。

### 阻止网站跟踪您

众所周知，几乎所有的网站都在试图追踪你的活动 。无论是为广告收集信息，收集人口统计信息，还是其他任何东西，我们都在自由地给出多少信息，这令人不安。值得庆幸的是，如果你花时间启用某个功能，Adblock 会让这些网站更难追踪到你。

只是 [头这里](https://adblockplus.org/en/features#tracking) 装了 Adblock Plus。单击“添加”按钮，Adblock Plus 现在将保护您免受跟踪。

不过，这并不是停止 Adblock Plus 跟踪的唯一方法。脸书和 Twitter 等社交媒体按钮也用于跟踪你的浏览习惯，但 Adblock Plus 也可以禁用这些功能。只需 [点此处](https://adblockplus.org/en/features#socialmedia) ，点击“添加”按钮，即可添加停止社交媒体追踪的过滤器。

### 保护自己免受恶意软件、广告软件、病毒和其他垃圾邮件的侵害

病毒、恶意软件、广告软件、特洛伊木马、间谍软件和所有其他垃圾通过各种不同的方法潜入您的浏览器。其中一种方法是通过受感染的网站，但 Adblock Plus 实际上可以配置为阻止这些网站，这样您就不会意外感染一些讨厌的东西。

你所需要做的就是 [点击这里](https://adblockplus.org/en/features#malware) 安装 Adblock Plus，然后点击“添加”按钮安装一个过滤器，保护你免受已知传播恶意软件网站的攻击。这是一个简单，容易的方法来确保您的计算机不会被感染，你几乎不需要做任何事情。

### 阻止任何你想要的内容

你也可以使用 Adblock Plus 来屏蔽互联网上任何你不喜欢的内容。你所要做的就是去任何一个有你不喜欢的图片、视频或歌曲的网站，右击它，然后选择“屏蔽元素”这将自动创建一个过滤器来阻止来自该 URL 的图像，如果您对网站的徽标有着根深蒂固的仇恨，这将是一个很好的选择。

当然，如果你愿意，你可以走得更远。用 [自定义过滤器](https://adblockplus.org/en/filters) ，可以屏蔽网上各种东西。这个 [可能是 Twitter 上的页脚页面，](http://howdoitknow.net/tutorials/how-to-hide-who-to-follow-section-on-twitter/) [脸书](https://www.facebook.com/adblockplus/posts/458004530907639) 上的游戏建议，甚至是 [要求你关闭 Adblock](http://origin1tech.wordpress.com/2013/08/06/adblock-custom-filters-nfl-sites-nag/) 的弹出窗口。

### 屏蔽所有闪光灯以延长笔记本电脑的电池寿命

Adobe Flash 是电池杀手，如果你在笔记本电脑上，这几乎是你最不想要的东西。令人欣慰的是，仅使用 Adblock Plus 就能轻松阻止 Flash。你所需要做的就是进入 Adblock 的设置，点击“添加你自己的过滤器”,并将其添加到你的列表中:

```
*.swf
```

同样，你可以更进一步，屏蔽一切可能会消耗你电池的东西，以获得真正最低限度的浏览体验。为此，只需添加:

```
*$object
```

上述过滤器将使它没有多媒体内容通过，从 Java 到 Windows Media 文件。如果你想在一个站点上启用它，只需在你的浏览器中点击 ABP 标志，并取消选中“为此站点启用”按钮来禁用它。如果您愿意，还可以通过在代码前添加 URL 来将它限制为一个站点。例如:

```
forbes.com$object
```

这确保了福布斯网站上没有加载任何媒体内容，这意味着视频、音乐和所有其他内容——不仅仅是广告。当你制作一个为慢速互联网连接 优化的 [浏览器时，这是很棒的。](https://lifehacker.com/how-and-why-to-set-up-a-secondary-browser-optimized-f-5791586)

### 绕过付费墙或登录限制

有时，如果有问题的网站以特定方式阻止内容，Adblock Plus 可用于绕过付费墙或网站登录。这是一个很好的个案基础，所以你通常需要在谷歌上搜索你正在寻找的网站的提示，但一个例子是 [Quora](https://www.quora.com/) ，它让你用一个帐户登录以查看内容。你可以用 Adblock Plus 过滤器来避开这个限制，它隐藏了 Quora 用来隐藏其内容的元素。

要在不登录的情况下查看 Quora，你只需要创建一个 Adblock 过滤器。进入 Adblock 的设置，选择“添加您自己的过滤器”，并将它们添加到您的列表中:

```
quora.com##.modal_signup_background
```

```
quora.com##DIV[id$="_modal_signup_wrapper"]
```

```
quora.com##.blurred_para
```

这样你就可以不用创建账户就能阅读 Quora 了。这个基本前提适用于任何通过覆盖图片来屏蔽内容的网站。在 Quora 的例子中，它是上面列出的三个元素，但它也可以只是一张掩盖内容的图片。如果你想自己绕过这些限制，只要右击你选择的网站上阻止内容的东西，然后选择“阻止元素”在大多数情况下，这会让你去你想去的地方。