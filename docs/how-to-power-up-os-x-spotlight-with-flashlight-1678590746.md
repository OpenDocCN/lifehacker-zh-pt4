# 如何用手电筒打开 OS X 的聚光灯

> 原文:[https://life hacker . com/how-to-power-up-OS-x-spot light-with-手电筒-1678590746](https://lifehacker.com/how-to-power-up-os-x-spotlight-with-flashlight-1678590746)

当我们第一次谈到 [手电筒的时候，它还在测试版](https://lifehacker.com/flashlight-adds-more-search-results-to-spotlight-1657873283) 。即便如此，在 OS X Yosemite 中用更多的搜索结果来增强 Spotlight 还是很有希望的。现在，这款应用更加成熟，有了一堆插件，功能强大得令人难以置信。让我们来看看如何设置它，并找到一些最有用的插件。

Watch

### 手电筒是什么？

[手电筒](http://flashlight.nateparrott.com/) 从表面上看是一个非常简单的应用程序:它允许你在优胜美地的内置聚光灯搜索中添加自定义搜索插件。在很多方面，它的工作方式类似于 Alfred 的 [，](https://lifehacker.com/a-beginners-guide-to-mouseless-computing-with-alfred-1596198655) 免费版本，但由于它与*Spotlight 一起工作，而不是取代它，你仍然可以获得 spot light 搜索的所有好处，包括难以置信的快速结果，原生搜索功能，等等。*

然而，手电筒的症结在于它的插件。你只需点击几下就可以下载并安装手电筒，但是如果你真的想让它变得有用，你需要找到合适的插件并学习如何使用它们。

你可以用三种不同的方式安装新的插件。你可以去手电筒网站 [搜索出](http://flashlight.nateparrott.com/browse) 然后从那里安装。你也可以打开手电筒应用程序来搜索批准的插件。如果您愿意，也可以通过拖动。将文件捆绑到 `~/Library/FlashlightPlugins`中。如果你对 Python 有所了解，你也可以轻松的 [制作自己的插件。](https://github.com/nate-parrott/Flashlight/wiki/Creating-a-Plugin)

你有大量的插件可供选择，所以让我们来看看一些我们最喜欢的。

### 关闭、重启或睡眠您的 Mac

关机和你想象的差不多。你可以在 Spotlight 中输入“关机”“重启”“注销”“睡眠”“锁定”或“屏幕保护”来触发这些命令。为这些选项调出一个菜单并不困难，但是从键盘上访问它们是很好的。

### 撰写 iMessage

[iMessage](http://flashlight.nateparrott.com/plugin/imessage) 是一个插件，可以让你从 Spotlight 快速撰写 iMessage。只需输入“文本[人]，[您的消息]”。确保您在其中包含逗号，否则它不知道名称的终止位置和消息的开始位置。

### 搜索特定的表情符号或 Unicode

[表情符号搜索](http://flashlight.nateparrott.com/plugin/emoji) 和 [Unicode 搜索](http://flashlight.nateparrott.com/plugin/unicode) 都比在字符菜单中搜索 Unicode 或表情符号容易得多。只需输入“表情符号[查询]”或“unicode[查询]”，当你想要的结果弹出时，点击 Enter 将其复制到剪贴板。

### 发送电子邮件

就像前面提到的 iMessage 插件一样， [发送电子邮件](http://flashlight.nateparrott.com/plugin/send_email) 插件可以让你在 Spotlight 上快速撰写电子邮件。您可以输入“向[姓名]发送电子邮件，说明[您的消息]”或“向[电子邮件地址]发送电子邮件，主题[您的主题]说明[您的消息]。”

### 获取四天的天气预报

顾名思义， [天气](http://flashlight.nateparrott.com/plugin/weather) 在聚光灯下显示天气预报。只需输入“天气[城市名称]”即可获得四天的天气预报。

### 将项目添加到提醒事项中

[提醒我](http://flashlight.nateparrott.com/plugin/remind-me) 允许你轻松地将待办事项添加到提醒应用程序中，只需输入你在提醒中输入的相同内容。您可以键入类似“提醒我在 1 月 11 日上午 11:30 和 Bob 一起去吃午饭”或“提醒我明天五点吃晚饭”的内容

### 搜索谷歌

[谷歌搜索](http://flashlight.nateparrott.com/plugin/googlesearch) 在 Spotlight 中显示谷歌搜索的结果，这比 Spotlight 的内置选项要方便得多。只需输入“谷歌[查询]”甚至只是“g[查询]”，就可以搜索你想要的任何内容。如果这还不够，你还可以抓取用于搜索的插件 [谷歌地图](http://flashlight.nateparrott.com/plugin/googlemaps) ， [谷歌图片](http://flashlight.nateparrott.com/plugin/googleimages) ，或者 [谷歌翻译](http://flashlight.nateparrott.com/plugin/googletranslate) 。单击任何结果，在默认浏览器中打开它。

### 运行终端命令

[终端](http://flashlight.nateparrott.com/plugin/terminal) 允许您从 Spotlight 在终端中运行命令。只需键入您想要的任何命令，终端就会打开并运行该命令。

### 搜索生活黑客

我决定继续做几个不同的插件来搜索 Lifehacker 上的文章。 [这个使用了我们网站的](http://edge-cache.lifehacker.com/lifehacker/Flashlight/lifehackersearchkinja.zip) (不可否认并不伟大)内置搜索引擎。 [这一款使用特定网站的谷歌搜索](http://edge-cache.lifehacker.com/lifehacker/Flashlight/lifehackersearchgoogle.bundle.zip) 。这两种情况都只需要输入“lifehacker [query]”或者“lh [query]”。您需要手动安装这些插件。将文件打包到您的`~/Library/FlashlightPlugins`目录中。不要同时安装两者，否则你会有一些问题。