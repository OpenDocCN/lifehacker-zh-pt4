# TextExpander 综合指南

> 原文：<https://lifehacker.com/a-comprehensive-guide-to-textexpander-1616374942>

当你发现自己在重复输入相同的信息时，文本扩展应用程序 是节省时间的好方法，但它们能做的远不止这些。我们最喜欢的是 Mac 上的 TextExpander，一旦你学会如何使用它，它就是一个强大的工具。



[Thanh 最近在我们的网站上写了](http://www.asianefficiency.com/technology/textexpander-review/) 关于 TextExpander 的基本特性和他如何在日常生活中使用它，在这篇文章中，我想更深入地向你展示如何使用 TextExpander 中可用的不同宏类型来创建你自己的(和更复杂的)“片段”

***本帖原载于*** [***亚洲效率***](http://www.asianefficiency.com/technology/comprehensive-textexpander-guide/) ***。**T15】*

在 TextExpander 术语中，当您键入指定的 TextExpander 缩写时，会显示一个“片段”。例如，像“tyvm”这样的缩写可以扩展为“非常感谢”这样的片段。我经常用这个来引用。例如，我有一个缩写“xplan”，它扩展为我最喜欢的一句名言的片段，“那些没有计划的人，计划失败。”因此，就其核心而言，TextExpander 就像它听起来的那样——一个扩展文本的程序。如果这是你使用 TextExpander 的唯一方式，这个应用程序将仍然值得 35 美元的标价，因为它仍然会节省你大量的时间。

然而，很多时候你最终重复输入的文本有可变的或可选的内容。这就是我们将在本文中讨论的宏真正派上用场的地方。

### 宏简介

TextExpander 中有几种不同类型的宏。请记住，您实际上不需要记住这些宏，因为它们都可以使用 TextExpander 中的“插入”菜单来插入:

以下是 TextExpander 中可用的不同类型的宏:

*   日期/时间
*   片段
*   钥匙
*   剪贴板
*   画
*   光标
*   填充符

我将逐个分解这些宏，并在附带的视频中讨论它们。

### 使用日期和时间

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-il3PLArX8m4&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-il3PLArX8m4&start=0) 

TextExpander 宏的一个最实际的应用是用于日期和时间戳。您可以使用 TextExpander 输入时间和日期，对不同的格式选项使用不同的宏。以下是显示日期和时间信息的所有不同宏选项:

| 巨 | 扩展文本 |
| --- | --- |
| %Y | 4 位数年份数字(“2014”) |
| %y | 两位数的年份数字(“14”) |
| %B | 完整拼写的月份名称(“八月”) |
| %b | 缩写月份名称(“Aug”) |
| %m | 2 位数月份数字(“08”) |
| %1m | 月份号(“8”) |
| %d | 两位数的日期数字(“08”) |
| %e | 天数(“8”) |
| %A | 完整拼写的日期名称(“星期五”) |
| %a | 缩写的日名(“Fri”) |
| %I | 两位 12 小时制时钟数字(“02”代表凌晨 2 点或下午 2 点) |
| %H | 两位 24 小时制数字(“02”代表凌晨 2 点，“14”代表下午 2 点) |
| %1H | 修剪后的 12 小时时钟数字(“2”代表凌晨 2 点或下午 2 点) |
| %1I | 修剪后的 24 小时制数字(“2”代表凌晨 2 点，“14”代表下午 2 点) |
| %M | 2 位数分钟数(“05”) |
| %1M | 微调分钟数(“5”) |
| %S | 2 位数秒数字(“03”) |
| %1S | 微调秒数(“3”) |
| %p | 扩展到上午或下午 |

例如，将扩展到 2014 年 8 月 8 日星期五的**-下午 2:05:03**的片段将被编写为:

`%A, %B %e %Y - %1I:%M:%S %p`

但是，您不需要记住这些宏，您实际上可以从“插入”菜单中选择它们。

以下是几个可以添加到 TextExpander 的标准日期和时间格式片段的示例:

| 巨 | 示例文本 |
| --- | --- |
| %m-%Y | 08–2014 |
| %m-%d-%Y | 08–08–2014 |
| %m/%d/%Y | 08/08/2014 |
| %d %b %y | 14 年 8 月 8 日 |
| %d %b %Y | 2014 年 8 月 8 日 |
| %B %e，%Y | 2014 年 8 月 8 日 |

像这样在你的笔记和信息中添加日期和时间戳是非常有用的。我们最近写了一篇关于 [约会的重要性](http://www.asianefficiency.com/habits/get-habit-dating-everything/) 关于亚洲效率的文章。以下是几个可以从日期/时间戳中获益的例子:

*   [期刊](http://www.asianefficiency.com/organization/journal-entries/) 条目
*   会议笔记
*   任何形式的电子通信
*   文件名(尤其是当 [变成无纸](http://www.asianefficiency.com/organization/going-paperless-with-your-iphone-and-evernote/) 时)

您也可以做日期/时间数学来增加或减少文本扩展器中的时间单位。为此，只需将日期/时间数学前缀放在您想要修改的时间单位之前(您也可以通过插入菜单来完成此操作，请参见视频示例)。日期/时间数学宏以“%@”开头，后跟“+”或“-”，然后是您想要加减的时间单位(例如，“D”代表天)。例如，*“确保您在%@+14D%B %e，%Y 之前提交会议的费用报告”*将从当前日期起增加 14 天。

### 在代码片段中嵌套代码片段

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-SBVJml_2CJs&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-SBVJml_2CJs&start=0) 

您知道吗，您可以将片段*放入片段*中？这被称为*嵌套片段*，它允许你在不止一个地方使用一个片段，而不需要再次输入(甚至是缩写)。要在代码片段中添加代码片段，只需使用 TextExpander 中的“插入”下拉菜单并选择“代码片段”，或者使用宏**% Snippet:(snippet_abbrev)**从您的代码片段文件夹中选择它，其中(Snippet _ abbrev)是您要使用的代码片段的缩写。

当您想要在标准电子邮件中使用报价时，这很有用。例如，之前我告诉过你我为我最喜欢的一句名言“未能计划”创作的一个片段，它说“那些未能计划的人，计划失败”，这是通过使用缩写“xplan”扩展的。我可以将这个片段嵌套在提醒电子邮件中，提醒我的团队成员提交他们对某个特定项目的贡献，内容如下所示:

> 只是提醒一下，目前的冲刺本周即将结束，我们仍然没有收到所有团队的贡献。没有所有需要的部分，就不可能制定这个项目的路线图，我担心会落后于我们的目标日期。记住， **%snippet:xplan。**

### 模拟按键

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-QgXNqQ6GLos&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-QgXNqQ6GLos&start=0) 

这个宏模拟按键。有四个选项可供选择:*回车、退出、返回、*或*标签*。这在填写表单时很有用，可以从一个字段切换到另一个字段，而不必实际触摸键盘——让 TextExpander 为您完成！您可以通过在 TextExpander 的“插入”菜单中选择“Key”或使用宏 **%key:(key name)** 来完成此操作，其中(key name)是键的名称。

例如，您可以创建一个代码片段来填写您的电话号码，并通过创建如下代码片段来自动跳转到下一个用于填写 web 表单的字段:

`555-555-5555%key:tab%`

然而，我们**强烈**建议您不要使用这种方法设置在线密码。首先，TextExpander 不能处理安全的输入字段，但更重要的是，它会将您的密码和帐户凭证暴露给任何可能访问您的代码片段集合的人。例如，如果您使用 Dropbox 同步您的片段，并且您的 Dropbox 凭据被泄露，则您的所有片段(以纯文本形式存储)都是可访问的。相反，使用类似于 1Password 的 [来安全地存储您的密码！](https://lifehacker.com/which-password-manager-is-the-most-secure-5944969)

### 插入剪贴板的内容

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-d60I3wVyzhg&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-d60I3wVyzhg&start=0) 

这个宏将剪贴板的内容放到代码段的指定区域。当您向多个收件人发送电子邮件(如聚会邀请)时，如果您希望他们的名字在整个电子邮件中出现多次，您可以使用此选项。您可以从邀请列表中复制他们的名字，然后让它出现在任何出现 **%clipboard** 的地方。您也可以从“插入”菜单中插入此宏。

这里有一个例子:

> 嗨%剪贴板！下周六我将在全食超市为我们的朋友 Thanh 举办一个生日派对(他真的很喜欢那个地方)，我真的希望你能来。我知道如果你能来，对他来说意义重大。请回复我，这样我们就知道会有多少人。希望尽快见到您，%剪贴板！

假设我们在输入代码片段之前将姓名“Zachary”复制到剪贴板上，它看起来会是这样的:

> 你好，扎克里！
> 
> 下周六，我将在全食超市为我们的朋友 Thanh 举办一个生日派对(他非常喜欢那个地方)，我真的希望你能来。我知道如果你能来，对 Thanh 来说意义重大。请告诉我，这样我们就知道会有多少人。
> 
> 希望很快见到你，扎卡里！
> 
> *麦克*

下面是一些可以与 *%clipboard* 片段一起使用的其他东西:

*   名称
*   电话号码
*   电子邮件地址

### 插入带有“图片”的图像

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-9lC6--1EHAQ&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-9lC6--1EHAQ&start=0) 

你知道 TextExpander 不仅仅用于文本吗？你也可以用它来放置图片。这对于一个公司徽标来说可能很有用——例如，当我键入“aelogo”时，它会扩展成我们网站的徽标。

这也可用于存储:

*   逻各斯圣语
*   信息图表
*   动画 gif

### 将光标放在你需要的地方

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-AKutsdfCxGc&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-AKutsdfCxGc&start=0) 

您可以使用该宏将光标移动到代码片段中的某个位置(称为“插入点”)。您可以通过从“插入”菜单中选择“光标–>将光标置于此处”或通过键入 **⌘|** (命令+竖线字符)来添加该宏。

这在就一个共同话题向多人发送电子邮件时会很有用，但你仍然需要定制每条消息，比如告诉人们在计划聚会时应该带些什么。例如:

> 谢谢你同意帮我为 Thanh 办一个惊喜派对。只是提醒一下，聚会是在本周六下午 4 点，我需要你带⌘|来参加聚会。我真的很感谢你的帮助！

这对代码片段也非常有用。例如，我可以制作一个如下所示的代码片段:

`<div id="⌘|">`

通过将用于移动光标(⌘|)的宏放在引号之间，在代码片段展开后，光标将自动移动到那个位置，我只需输入值:

您也可以将光标向上、向下、向左或向右移动到插入点。这些分别以←、→、↑、或↓ (⌘ 、⌘^、或⌘v).为代表例如，如果您想在代码片段的末尾将光标下移两行，您可以通过键入 **⌘v⌘v** 来完成。

### 填充符

填充是非常强大的宏，允许你用 TextExpander 做一些疯狂的事情。有 4 种类型的填充宏可供选择:

#### 1.单行字段

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-ttNl4h_UcGU&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-ttNl4h_UcGU&start=0) 

该宏有一个特定的字段，您可以在其中键入想要显示的文本。例如，您可以有一个名为“名字”的单行字段，它会随着称呼展开，还有一个字段，您可以在其中键入收件人的名字。这是个性化表单电子邮件模板的好方法。您可以通过从 TextExpander 的“插入”菜单中选择“填充–>单行字段”来添加单行字段填充。

单行字段的宏是 **%filltext%** ，带有字段名、默认值和宽度的其他选项。因此，如果您想使用单行字段填充来定制电子邮件模板的顶部，它看起来会像这样:

`Hi %filltext:name=First Name%,`

该宏将扩展为如下所示:

下面是单行字段填充可能有用的几个其他示例:

*   标题
*   作者
*   类型

#### **2。多行字段**

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-sHrLofKk18Q&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-sHrLofKk18Q&start=0) 

这个宏就像单行字段，除了你得到一个可以填写的文本框，有点像许多 web 表单中的“消息”或“附加注释”字段。这对于短列表来说非常有用，与单行字段相比，多行字段的优点是允许更多的文本。

多行字段的宏是 **%fillarea%** ，带有字段名、默认值、宽度和高度的其他选项。因此，如果您想在代码片段中使用这个宏来为 web 开发创建段落标记文本，它看起来应该是这样的:

`<p>%fillarea:name=Paragraph Text%</p>`

要设置它，将光标放在段落标签之间，并从 TextExpander 的“插入”菜单中选择“填充>多行字段”。确保将*放在段落标签*之间，将“段落文本”放在“区域名称”中，暂时保留默认值、宽度和高度。

在视频示例中，我将这个片段命名为“p tag ”,并将其缩写为“xptag”。现在，当我切换到我的文本编辑器时，我可以键入“xptag ”,代码片段就会启动，允许我以适合 web 的格式键入我的段落文本。

以下是多行字段填充可能有用的几个其他示例:

*   信息
*   摘要
*   会议议程

#### **3\. Popup Menu**

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video--oF6vaJmLJM&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video--oF6vaJmLJM&start=0) 

该宏打开一个弹出菜单，其中有几个预填充的选项供您选择。您可以在发送约会提醒时使用它来选择约会的代表，或者从有限的变量中进行选择，比如在跟进客户最近的购买时选择一种产品。

弹出菜单的宏是 **%fillpopup%** ，带有弹出名称、弹出菜单项和默认设置的其他选项。因此，如果我想创建一个标准的代码片段，以便在跟进客户时使用，我可以创建这样一个代码片段:

`%fillpopup:name=Product:OmniFocus Premium Posts:default=Productivity Blueprint:Asian Efficiency Primer:Premium Newsletters:Better Sleep`

为此，我将从“插入”菜单中选择“填充>弹出菜单”，将弹出菜单命名为“AE 产品”，然后填写产品选项作为我的弹出菜单项——“AE 入门、高级简讯、更好的睡眠、OmniFocus 高级帖子和生产力蓝图”。您还可以更改默认选择的选项(我将选择 OmniFocus Premium 帖子)。

在视频示例中，我将这个片段命名为“AE Products ”,并将其缩写为“xprod”。现在，当我切换到我的邮件应用程序，想要向客户发送跟进消息时，我可以键入“xprod”，从弹出菜单中选择适当的产品，点击“OK”，适当的文本就会粘贴到我的电子邮件消息的正文中。

这里有几个弹出菜单有用的例子:

*   日期选择
*   选择团队成员
*   选择产品或服务

#### **4。可选选择**

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-ZaxpdYRkb_o&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-ZaxpdYRkb_o&start=0) 

此宏包含一段文本，您可以通过选择复选框来包含这段文本。如果你有时会在合同协议中加入一个条款，或者你有时会在标准邮件回复的末尾加入某些信息，你就可以使用。

可选选定内容的宏是 **%fillpart%(可选文本)%fillpartend%** ，其中(可选文本)是要包含在可选选定内容中的文本。*可选零件名称*还有其他选项，以及是否默认包含。

因此，如果我想创建一个代码片段来跟进对最近的博客帖子发表评论的人，我可以创建一个如下所示的代码片段:

> 感谢您阅读亚洲效率博客。% fillpart %既然你似乎喜欢 Omnifocus，你可能想看看 Omnifocus premium 帖子的更新。%fillpartend%

变成了:

现在，并不是每个阅读亚洲效率博客的人都对 OmniFocus 感兴趣(我知道这很难相信)，所以我们可能不想一直包含最后一部分，但它经常出现，我们也不想手动键入它。在我们的 TextExpander 代码片段中使用一个可选选项，可以让我们保持亚洲人的效率，而不会让我们的非 OmniFocus 用户感到厌烦。

以下是可选选项有用的几个其他示例:

*   客户支持链接
*   客户参考
*   电话会议信息

### 齐心协力

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-AszzmpYSd2M&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-AszzmpYSd2M&start=0) 

关于 TextExpander 代码片段的最好的部分是，您不仅仅局限于每个代码片段中的一个宏。实际上，您可以将它们链接在一起，组合起来做一些非常疯狂的事情，从通过将所有电子邮件模板存储在 TextExpander 中来提高您的电子邮件生产率，到通过为开发人员重用代码片段来加快您的开发时间。

下面是一个相当复杂的电子邮件片段的例子:

> *嗨% fill text:Name = First Name:default = First Name %，*
> 
> *感谢您抽出时间与我交谈% fill popup:name = Webinar:yesterday:default = today:几天前%。正如我们讨论过的，我为你准备了一份提案。要查看提案，请使用以下 URL: %clipboard*
> 
> *% fill part:name = Trial %如果您想享受我们的免费试用优惠，请访问我们的网站-*[*www.notarealsite.com/trial.*](http://www.notarealsite.com/trial.)
> 
> *% fillpartend % % fillpart:name = Portfolio %如果您想查看或下载样本报告，您可以使用此链接:*[](http://www.notareallink.com/portfolio)
> 
> **% fillpartend % % fillpart:name = Purchase %如果您想试用该计划并购买一些点数，请使用此 URL:*[*【www.notarealsite.com/buystuff】*](http://www.notarealsite.com/buystuff)*
> 
> **% fillpartend % % fillpart:name = Reference %如果您想与目前正在使用我们产品的人交谈，您可以联系以下推荐人:**
> 
> **范青*
> *亚洲效率*
> *123 不真实街道*
> *加州某地 12345*
> *(555)555–5555 x 1**
> 
> **麦克施密茨*
> T3】亚洲效率 T5*123 大街*
> *别的地方，FL*
> *【555】555–5555 x 2**
> 
> **%fillpartend%I 将与您跟进% fillpupup:name = Follow Up:在几天内:default =下周:在几周内%以确保您得到所有信息，并查看您是否有任何问题。如果你在那之前需要任何东西，请随时联系我。**

*下面是我输入缩写时的样子:*

*你会注意到有几个我可以定制的填充。一个是名字，一个是网上研讨会实际发生时间的弹出窗口，一个是我经常包括但不是每次都包括的信息的可选选项，还有一个是我下次联系时的弹出窗口。还有一个剪贴板引用，我可以从剪贴板中提取提案的链接。*

*使用这个片段，一旦我选择并填写了我想要包含的所有信息，我只需点击“确定”,我的整个电子邮件就为我写好了。*

### *还有一件事:Applescript*

 *[https://lifehacker.com/embed/inset/iframe?id=youtube-video-LK2gibEe8Bo&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-LK2gibEe8Bo&start=0)* 

*您知道您甚至可以通过 TextExpander 运行 Applescript 吗？例如，您可以让 Applescript 片段在 Chrome 而不是 Safari 中打开当前 URL。Chrome 有内置的 Flash 支持，所以如果你想避免的话，这是在你的电脑上安装 Flash 插件的一种方法。*

*充分披露:我不知道 Applescript，这个例子来自于 [Smile 软件博客](http://smilesoftware.com/blog/entry/a-few-snippets-more) 。这一切都归功于他们。下面是设置它的方法:*

1.  *设置标签“在 Chrome 中打开 URL”。*
2.  *设置缩写(即“cchrome”)。*
3.  *创建内容类型为“Applescript”的新片段。*
4.  *将 Applescript 粘贴到 TextExpander 窗口中。以下是 Applescript:*

> **属性 theURL : ""*
> *告诉应用程序" Safari"*
> *将 theURL 设置为窗口 1 当前标签页的 URL*
> *结束告诉*
> *如果应用程序正在运行(" Google Chrome ") 然后*
> *告诉应用程序“Google Chrome”*
> *制作新窗口*
> *设置窗口 0 的活动标签的 URL 为 URL*
> *激活*
> *结束告诉*
> *否则*
> *告诉应用程序“Google Chrome”*
> *做 shell 脚本“open-a”Google Chrome”* 激活
> *end tell*
> *end if*
> *on appIsRunning【appName】*
> *tell application“系统事件”to(进程名称)包含 appName*
> *end appIsRunning**

*现在只需转到当前打开的 Safari 标签页或窗口，键入“cchrome”。Chrome 将打开，并显示当前选项卡。*

*这对于用 OmniFocus 运行 Applescript 非常有用，OmniFocus 有很好的 Applescript 支持。*

### *将它投入使用*

*正如你(希望)从这篇文章中看到的，TextExpander 有很多可能的用途。这是一个非常有用的工具，可以节省你很多时间，但是像任何工具一样，只有正确使用它，它才会有效。除了我们在这篇文章中提到的例子之外，在你将 TextExpander 应用到你的个人工作流程中时，这里还有一些你需要记住的最佳实践:*

#### ***同步您的片段***

*你可以通过 Dropbox 同步你的片段，这允许你通过 TextExpander touch 和 iOS 设备上其他支持的应用程序来访问它们。为此，你必须进入“设置”，点击“同步”，然后选择“Dropbox”。*

*有不少 app 支持 TextExpander touch API。这里有一个 [完整列表](http://smilesoftware.com/apps/) ，以防你想知道你最喜欢的应用程序是否受支持。*

#### ***使用标准前缀***

*Thanh 在 [这篇文章](http://www.asianefficiency.com/technology/textexpander-guide/) 中谈到了他为不同类型的代码片段使用的不同前缀(这是一种组织您的 TextExpander 代码片段集合的非常逻辑的方式)，但我倾向于对所有内容使用前缀“x”。这有几个原因:*

*   *我无法想象我会键入一个以 x 开头的实际单词，而这个单词会与我的代码片段发生冲突。*
*   *我知道当我键入“x_”时，它肯定是一个 TextExpander 片段。*
*   *“x”字符在 iOS 键盘上很容易访问(用于通过 TextExpander touch 扩展片段)。*

**注意:*在 TextExpander 中，确实没有一种“正确的方式”来组织您的代码片段。重要的是一致性。你只需要找到对你有意义的，容易记住的东西。*

#### ***思考实际用途***

*在将任何工具添加到您的工作流程之前，您应该问自己这样的问题“这个工具将帮助我解决什么问题？”每件事都需要有一个角色和目的。在 TextExpander 的例子中，它解决的问题是重复输入你常用的单词和短语所花费的时间。但是如果你不注意，并且发现自己一直在重复一些事情，你就会陷入盲目的走过场，一遍又一遍地重复同样的事情。*

*相反，你应该有自知之明:每当你发现自己不止一次地做某件事时，问问自己“我怎样才能自动化这件事？”有了 TextExpander，事情就简单了——只需输入你经常输入的文本，剩下的就交给它了。但是，如果没有自己开发的代码片段库，TextExpander 的强大功能不会给你带来太多好处。*

*希望这篇关于 TextExpander 的指南为你指出了正确的方向，告诉你如何使用这个无比强大的 Mac 工具，但是这只是皮毛。我们很想知道你是如何使用 TextExpander 的！*

*[text expander](http://www.asianefficiency.com/technology/comprehensive-textexpander-guide/)T3【亚洲效率】综合视频指南*

* * *

*亚洲效率是由两个朋友发起的，他们(不出所料)都是亚洲人。我们看到，世界上有太多的人因为过着没有产出的生活而不快乐。通过创办这个网站，我们(无论是 [<small>*亚伦琳*</small>](http://www.asianefficiency.com/author/aaron/) <small>*和*</small> [<small>*范成范*</small>](http://www.asianefficiency.com/author/thanh/) <small>*)想告诉你如何通过更有成效地生活来最大限度地过你的生活，这样你就可以追求你生命中想要的东西。*</small>
<small>*T32】*</small>*

**<small>*图片改编自*</small>[<small>*OpenIcons*</small>](http://pixabay.com/en/full-screen-resize-enlarge-expand-97639/)<small>*(pix abay)*</small>[<small>*PublicDomainPictures*</small>](http://pixabay.com/en/scrabble-word-letter-letters-help-15546/)<small>*(pix abay)，以及*</small>[<small>*Wikicommons*</small>](http://en.wikipedia.org/wiki/Command_key)**

**<small>*想看看你在 Lifehacker 上的作品？邮箱*</small> [<small>*安迪*</small>](mailto:andy@lifehacker.com) <small>*。*T15】</small>**