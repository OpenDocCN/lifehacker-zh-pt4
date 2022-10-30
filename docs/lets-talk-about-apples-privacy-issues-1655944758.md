# 我们来谈谈 OS X Yosemite 的隐私问题

> 原文：<https://lifehacker.com/lets-talk-about-apples-privacy-issues-1655944758>

自从 Yosemite 发布以来，用户发现操作系统在你不知情的情况下将所有 [种数据发送给苹果](https://lifehacker.com/safari-and-spotlight-can-send-data-to-apple-heres-how-1648453540)[保存文档](http://arstechnica.com/security/2014/11/critics-chafe-as-macs-send-sensitive-docs-to-icloud-without-warning/) 。从表面上看，这是对隐私的严重侵犯。让我们来看看到底发生了什么。



### 隐私和聚光灯搜索

约塞米蒂隐私问题的最初争议是在主流媒体上引发的，当时《华盛顿邮报》发表了一篇文章 ，详细介绍了约塞米蒂如何记录你的位置以及你用 Spotlight 和 Safari 进行的搜索。本质上，当你在 Spotlight 中输入一个搜索查询时，Yosemite 会拨入苹果，然后伪装成使用数据发送过来。如果你也在使用定位服务，这些信息也会被发送出去。

Yosemite 会转发您的位置、您使用的设备类型、应用程序、您的语言设置以及您最近使用的应用程序。这听起来乍一看很吓人，但是让我们想想它为什么要这样做。如果你在搜索任何与地图相关的东西，包括当地的商店、餐馆或电影放映时间，它需要你的位置。当你开始输入时，它不知道你在搜索什么，所以它总是连接到互联网，以防你需要什么。需要知道你用的是什么应用程序，你用的是什么设备，你的语言设置是不言自明的。就最近的应用程序而言，这只是 Spotlight 的一个基本功能，但发送到苹果的数据也可以包括你电脑上任何文档的文本。

不仅仅是聚光灯和 Safari。使用网络监视器， [用户发现](https://github.com/fix-macosx/yosemite-phone-home) 有无数的统计数据被发送到苹果公司。这包括关于此 Mac 信息、邮件的域信息，甚至是通过 Safari 上的 DuckDuckGo 路由的搜索查询。

在苹果这边，你发送的数据被归在一个匿名 ID 下，这个 ID 每 15 分钟重置一次，所以很难追踪到你。同样，所有数据都是通过 HTTPS 传输的，因此在通过管道传输时应该是安全的。

苹果有一个 [隐私政策为功能](http://go.redirectingat.com/?id=66960X1514734&site=theverge.com&xs=1&isjs=1&url=http%3A%2F%2Fwww.apple.com%2Fprivacy%2Fprivacy-built-in%2F&xguid=e91dddc793f95cad9cab246359d4ea05&xcreo=0&xed=0&sref=http%3A%2F%2Fwww.theverge.com%2F2014%2F10%2F20%2F7022881%2Fapple-yosemite-spotlight-privacy-concerns&pref=http%3A%2F%2Fdaringfireball.net%2Flinked%2F2014%2F10%2F20%2Fyosemite-spotlight-privacy&xtz=480&abp=1) 准备，并以一个声明 回应 [:](http://www.theverge.com/2014/10/20/7022881/apple-yosemite-spotlight-privacy-concerns)

> 我们绝对致力于保护用户的隐私，并在我们的产品中加入了隐私权。对于 Spotlight 建议，我们尽量减少发送给苹果的信息量。苹果不会保留用户设备的 IP 地址。Spotlight 会模糊设备上的位置，因此它永远不会向苹果发送准确的位置。Spotlight 不使用持久标识符，因此苹果或其他任何人都无法创建用户的搜索历史。Apple 设备仅在 15 分钟内使用临时匿名会话 ID，然后该 ID 会被丢弃。
> 
> 我们还与微软密切合作，保护用户的隐私。苹果只将常用搜索项和城市级位置信息转发给必应。微软不存储搜索查询或接收用户的 IP 地址。
> 
> *您还可以轻松退出 Spotlight 建议、Bing 或 Spotlight 定位服务。*

因此，虽然数据收集在这里是有意义的，但主要的争议不是 Yosemite 向苹果发送了什么，而是大多数用户并不知道这一事实。传统上，苹果公司在隐私方面一直是一家选择加入的公司，所以这一功能在默认情况下是启用的。

### iCloud 数据隐私

也许是因为围绕 Spotlight 和 Safari 的争议，更多的人开始在 Yosemite 闲逛，看看还有什么可能被发送到苹果。最终，安全研究员 Jeffrey Paul [发现，即使不明确保存，正在进行的文档也会保存到 iCloud Drive](https://datavibe.net/~sneak/20141023/wtf-icloud/) 中。自从他的博客文章 [以来，其他用户在各种使用 iCloud Drive 的应用程序中发现了类似的行为](https://gist.github.com/landonf/c498562213286d778ac9) 。

在 Yosemite 之前，进行中的文件会自动存储在本地硬盘上，直到您明确地将它们存储在其他地方。您可以在“文本编辑”中键入您想要的任何内容，但是在您点按“存储”按钮并将其上传到 iCloud Drive 之前，它会存储在您的电脑上，而不会存储在其他地方。Yosemite 引入了一个新功能，每隔几秒自动保存这些文档。这很好，但它们会在你打开文档的第二秒自动保存，所以即使你没有明确点击保存按钮，数据仍然会上传到 iCloud。如果你不希望你的数据在云中，这是一个问题。

[这是优胜美地的一大特色，叫做](https://www.apple.com/ios/whats-new/continuity/) 。您可以在一台 Apple 设备上开始一个文稿，然后在另一台设备上轻松地选取它。苹果甚至有一个 [页面描述它是如何工作的](http://support.apple.com/en-us/TS4372) 。这就是它的全部意义。

争议来自于这样一个事实，你可能没有意识到那些未保存的草稿被上传到了 iCloud，因为苹果从来没有让这一点变得明显。 [说起石板](http://www.slate.com/blogs/future_tense/2014/11/03/filevault_2_mac_users_unsaved_files_and_screenshots_are_automatically_uploaded.html) ，研究教授马修·婷·格林说:

> 这是没人预料到的行为。我可以接受那些我没有保存在硬盘上的东西。我没意见。我认为这是一个很好的功能。但是我没有明确放在云端的东西被偷偷放到云端是一个奇怪的特性。

乍一看，他的抗议似乎是有道理的。然而，如果不这样做，Yosemite 的功能就不会工作。连续性还能如何工作？文档在保存之前就开始自动保存是不符合常规的，但是在这种情况下这是非常有意义的。这是该特性的基本要求。

因此，如果你使用任何支持连续性和 iCloud Drive 的应用程序作为快速转储私人信息的地方，包括社会安全号码、电子邮件地址或信用卡号码，那么如果你不想将这些数据上传到云中，你需要调整一些设置。

### 你能做些什么

谢天谢地，你可以很容易地解决这些隐私问题。对于 Spotlight 和 Safari，您只需切换几个设置:

*   停用 Spotlight 建议和 Bing Web 搜索。进入系统偏好设置> Spotlight >搜索结果，取消选中这两个框。
*   停用 Safari 的 Spotlight 建议。前往 Safari >偏好设置>搜索，取消选中 Spotlight 建议。

如果你担心泄露数据，禁用位置信息也是一个好主意。至于自动保存和连续性，您有几个选项。

若要逐个应用停用它，请进入“系统偏好设置”>“I cloud”>“iCloud Drive”>“选项”,然后取消选中任何不想使用 I cloud Drive 的应用。或者，您可以使用终端命令来停用所有应用程序的 iCloud 默认存储功能:

`defaults write NSGlobalDomain NSDocumentSaveNewDocumentsToCloud -bool false`

一旦启用，您将首先在本地保存文件。你必须手动选择将它们保存到 iCloud Drive。

这可能看起来很复杂，但底线很简单:苹果收集你的使用数据，但应该是匿名的。该数据是其操作系统的基本功能所必需的。同样，为了让某些功能发挥作用，私人文档需要上传到 iCloud，这样你就可以在其他设备上访问它们。

你可以禁用这两个功能，但隐私倡导者认为它们应该被默认禁用。到目前为止，我们看到的反应当然是合理的，但它们有点言过其实。