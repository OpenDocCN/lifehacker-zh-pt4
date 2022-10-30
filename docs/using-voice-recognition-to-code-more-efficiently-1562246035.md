# 我可以使用语音识别更有效地编码吗？

> 原文：<https://lifehacker.com/using-voice-recognition-to-code-more-efficiently-1562246035>

语音识别正在变得越来越好，它越来越多地不仅仅用于提醒和电子邮件。但是你能用它来帮助你编码吗？也许吧。贫嘴的编码员在 [*栈交换*](http://productivity.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=productivity-113) *处插话。*

Watch

我正在寻找用另一种输入形式来增强鼠标和键盘控制的方法。有没有办法用类似 [**龙**](http://www.nuance.com/dragon/index.htm) **的东西来触发宏展开？例如，我可以创建一个语音命令来编写一个循环模板吗？**

*见原问题* [*此处*](http://productivity.stackexchange.com/q/3605/2476?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=productivity-113) *。*

### 使用蜻蜓( [由亚历克斯](http://productivity.stackexchange.com/a/8321/6421?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=productivity-113)回答)

我使用由 [塔维斯·鲁德](https://github.com/tavisrudd) 创建的类似方法编写了一个系统，他是 [使用语音编码](http://ergoemacs.org/emacs/using_voice_to_code.html) 的强烈支持者，我现在已经使用它几个星期了。基本上，它在一个虚拟机中运行 Dragon 和 NatLink 以及蜻蜓，并在我的 Linux 系统上执行操作。这肯定还是胶带编码，但我对初步结果相当满意。可以在 [GitHub](https://github.com/calmofthestorm/aenea) 上查看。那里的大部分代码只需稍加修改，就可以在 Windows 上与蜻蜓一起使用。

那么它起作用了吗？我听写的速度不比输入代码快。但是我用语音和键盘的组合速度更快，无论如何，我花了足够的时间停下来思考，因为语音而导致的代码输入速度的小幅下降对整体生产率没有太大影响。我相信通过更多的努力，我可以提高。

特里斯坦·海菲尔德最近也在组上发布了关于 [一个类似项目](https://github.com/TristenHayfield/damselfly) 。

你可能也想看看 [声码](http://sourceforge.net/projects/voicecode/) 。我玩了一会儿，虽然这不是我真正想要的，但这是一个非常有趣的项目。

肯定有很多有前途的东西在流传，但是现在你需要准备做一些你自己的实质性定制和修改，以便得到一个你会满意的系统。

### 声音并不总是最好的( [由 asfallows](http://productivity.stackexchange.com/a/3614/778?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=productivity-113) 回答)

我认为语音激活工具的力量和潜力在于使用口语来触发动作和事件，而不是取代打字。

例如，如果您可以配置一个语音识别包来触发诸如“打开”、“保存”、“构建”、“运行”等命令。，这样你就可以节省浏览菜单或输入热键的时间。

然而，我不建议花太多精力使用语音识别来逐个关键字地生成源代码。除非你是一个说话很快的人或者打字很慢的人，否则你可能无法通过这种方法来提高你的速度、准确性或者整体效率。想象一下，每当您需要特殊的标记字符时，就不得不说“点”、“左括号”、“分号”等等，这些字符在编程中比在散文中普遍得多。如果没有高度专业化的方法(这将比像 NaturallySpeaking 一样调整软件包花费更多的精力)，我怀疑您是否会提高效率。

然而，作为程序员，提高效率的最有希望的领域之一是避免上下文转换。例如，通过使用热键而不是鼠标，尽可能不要将手从键盘上移开，这有助于程序员保持专注和高效。如果语音激活系统*减少了使用鼠标和退出活动程序的时间，它可能会有效，但试图用说话代替打字听起来不太可能使编码变得更容易。*

### 掌握你现有的工具来代替( [由戴夫·牛顿](http://productivity.stackexchange.com/a/3606/1731?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=productivity-113)回答)

在我看来，编程的语音输入很可能比打字效率低得多，尤其是在一个拥有良好的宏和模板工具的像样的编辑器中。我认为你最好弄清楚你通常工作的领域，你已经可以使用或者可以创建什么代码生成工具，并且确定你能找到的每一个可能的键盘和模板效率。

编程词汇表是专门化的，它关注的是一组不同于普通语音的终端。上下文敏感和语言敏感的编辑器可以访问您正在使用的任何语言、环境和框架的抽象语法树，而 Dragon 和其他这样的语音输入软件则不能。

这是我十多年来每隔几年都会玩的东西，很少会超过一两个小时就放弃。我们作为开发人员处理的抽象概念不能很好地映射到英语词汇中。即使使用语音宏，我个人还没有看到一个系统，或系统的组合，不会让我想打我的显示器的脸。

<small>*不同意以上答案？在*</small> [<small>*原问题*</small>](http://productivity.stackexchange.com/q/3605/2476?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=productivity-113) <small>*留下自己的答案或提交评论。在*</small> [<small>*个人生产力栈交流*</small>](http://productivity.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=productivity-113) <small>*看更多喜欢的问题，一个为想活得更有效率的人而设的问答网站。如果你有自己的问题需要解决，请询问*</small>[<small></small>](http://productivity.stackexchange.com/questions/ask?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=productivity-113)*<small>*。你会得到答案的。(而且是免费的。)*</small>*

*<small>*图片混搭自*</small> [<small>*马克西姆卡巴口*</small>](http://www.shutterstock.com/pic.mhtml?id=127646540&src=id)<small>*(Shutterstock)和*</small> [<small>*柳普科夫斯基*</small>](http://www.shutterstock.com/pic.mhtml?id=155251616&src=id)<small>*(Shutterstock)。*</small>*