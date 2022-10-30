# 我想写 iOS 应用。我从哪里开始？

> 原文:[https://life hacker . com/I-want-to-write-IOs-apps-where-do-I-start-1644802175](https://lifehacker.com/i-want-to-write-ios-apps-where-do-i-start-1644802175)

亲爱的 Lifehacker，
我有一点编码的背景，但是我想做一个 iOS 的 app。我只是不确定从哪里开始或者我需要什么工具。我从哪里开始？

Watch

真诚地，
App Store 业余爱好者

亲爱的 ASA，
学习 iOS 开发是一个双管齐下的过程。如果你完全不知道如何编码，你可以在这里 找到大量的 [资源。如果你精通编码，你需要熟悉苹果的开发工具*和*它们的指导方针。众所周知，苹果会限制各种应用程序，所以在开始之前知道你能做什么和不能做什么是很好的。](http://lifehacker.com/the-best-resources-to-learn-to-code-1517844722)

我们不会带你经历制作一个应用的整个过程，对于这篇文章来说这是太多的信息了。然而，我们会让你建立编码环境，给你苹果的指导方针，给你一些资源来帮助你学习苹果 iOS 的不同语言。

### Xcode、Swift 和 iOS SDK

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-9WXUug6Z8gQ&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-9WXUug6Z8gQ&start=0) 

苹果用于 Mac 和 iOS 应用的 IDE(集成开发环境)是 Xcode。它是免费的，你可以从苹果的 [网站](https://developer.apple.com/xcode/downloads/) 下载。Xcode 是您将用来编写应用程序的图形界面。它还包括你用苹果新的 [Swift 编程语言](https://developer.apple.com/swift/) 为 iOS 8 编写代码所需的一切。它也只适用于 Mac，所以如果你打算开发 iOS 应用，你需要运行 OS X。

虽然苹果公司最近一直在大力推广 Swift，但你可以用任何语言编写 iOS，包括 Objective-C。你决定用哪种语言真的取决于你，但这里有一些指南、课程和教程可以帮助你入门:

*   [**今天开始开发 iOS 应用**](https://developer.apple.com/library/ios/referencelibrary/GettingStarted/RoadMapiOS/index.html#//apple_ref/doc/uid/TP40011343) :这是苹果官方的入门指南。它会带你设置 Xcode，构建你的应用程序，实现所有功能，并提交给 App Store。
*   [**介绍 Swift**](https://developer.apple.com/swift/) :苹果新的编程语言 Swift，是专门为 iOS 和 MAC 制作的。它应该更容易操作和使用，所以如果你完全不熟悉 iOS 开发，这是一个很好的起点。它与 Objective-C(如果您愿意，也可以使用它)一起工作，并且类似于 Objective-C。
*   [**苹果的开发视频**](https://developer.apple.com/videos/) :苹果包括大量来自 WWDC 的视频，教你开发的各个部分。它们是学习行业技巧和了解您正在使用的基本工具集的绝佳资源。
*   [**雷·文德里希的教程**](http://www.raywenderlich.com/tutorials) :如果你想制作游戏，雷·文德里希的教程是一个很好的起点。他也涵盖了游戏之外的各种东西，所以你一定会学到一些关于 Swift 和 Objective-C 的东西，即使你更喜欢做一个生产力应用程序。
*   [**苹果的 API 功能**](https://developer.apple.com/ios8/#submit) :苹果有大量不同的 API 来访问应用扩展、触控 ID、照片、健康工具包等等。熟悉这些功能，以便将更多高级功能集成到您的应用中。
*   [**码校的 iOS App 开发课**](https://www.codeschool.com/courses/try-ios) :通过码校的入门课，可以免费掌握 iOS 开发的基础知识。
*   [**斯坦福的 iOS 开发班**](https://itunes.apple.com/us/course/developing-ios-7-apps-for/id733644550) :斯坦福有一套学习 iOS 开发的免费班。它仍然只适用于 iOS 7，但你学到的大多数东西应该可以很好地转移到 iOS 8。在不久的将来，他们可能会有一个 iOS 8 的升级版。

这应该能让你设置好你的开发工具，并让你很好地理解 iOS 上的工作方式。

### 苹果应用商店审查指南

众所周知， [苹果的应用商店审核指南](https://developer.apple.com/app-store/review/guidelines/) 非常具体。苹果对商店中允许哪些应用程序有非常具体的看法，所以在你尝试制作你的应用程序之前了解他们的规则是有用的。如果你不这样做，你可能会花时间做一些苹果不允许进入应用商店的东西。

当你完成你的应用程序时，你将把它提交到 App Store，它将根据内容、设计(在下一节中有更多的介绍)和技术细节进行审查。于是，前往 [复习指导页](https://developer.apple.com/app-store/review/guidelines/) 开始阅读。苹果还列出了 [应用被拒绝的常见原因](https://developer.apple.com/app-store/review/rejections/) 。通常情况下，这是因为崩溃，断开链接，广告，或不完整的信息。众所周知，苹果还会屏蔽包含任何类型的 [成人](https://kotaku.com/apple-wont-allow-masturbation-game-on-app-store-1577611591) 或 [政治内容](http://www.theguardian.com/technology/appsblog/2013/jan/08/endgame-syria-apple-rejection) 的应用。

同样，苹果的许多 API 都有自己的一套评审指南。因此，如果你打算将你的应用程序与 HealthKit 或 Apple Pay 集成，了解这些也是很好的。他们在这里:

*   [**Apple Pay 指南**](https://developer.apple.com/apple-pay/Apple-Pay-Identity-Guidelines.pdf)
*   [**App 扩展**](https://developer.apple.com/app-store/review/guidelines/#extensions)
*   [](https://developer.apple.com/app-store/review/guidelines/#healthkit)
*   **[**home kit**](https://developer.apple.com/app-store/review/guidelines/#homekit)T5】**

**请记住，苹果在应用审查过程中往往非常保守。很有可能，如果你正在做一个哪怕是很低级的东西，它都会被拒绝，所以在你开始做你的应用之前要注意这一点。**

### **苹果的设计准则**

**除了苹果的审核指南，他们还有一套设计和界面指南。苹果希望他们商店中的所有应用程序都有某种类型的一致性，虽然这不一定意味着好的设计，但这确实意味着应用程序使用相同的基本 UI 元素。**

**为了更好地理解这一点，请查看苹果的人机界面指南页面 。在这里，你可以找到他们在应用程序和图标设计中所寻求的基础知识。他们也有一套 [该做的和不该做的](https://developer.apple.com/design/tips/) 来提炼大量的指南，这样更容易开始。**

**谢天谢地，苹果没有让你完全不知道如何制作一个设计良好的应用程序。这里有一些资源可以帮助你设计出有价值的东西:**

*   **[**设计伟大的应用**](https://developer.apple.com/design/tips/) :苹果收集了一些 WWDC 关于设计的最佳演讲，帮助你开始设计界面。**
*   **[**设计用户界面**](https://developer.apple.com/library/ios/referencelibrary/GettingStarted/RoadMapiOS/DesigningaUserInterface.html) :苹果利用 Xcode 的内置工具整理出了一份在 iOS 8 中设计界面的指南。**

**你也可以在网上找到大量的 [资源来帮助提高你的设计水平，](http://www.invisionapp.com/tethr) 或 [看看我们的指南](https://lifehacker.com/learn-the-basics-of-design-this-weekend-5739492) 。**

### ****注册 GitHub 和试飞****

**除非你是某种超级天才，否则你可能不想在泡沫中创建你的应用程序。相反，让其他人看看你的代码并邀请测试人员来试用你的应用程序是很好的。**

**[GitHub](https://lifehacker.com/how-the-heck-do-i-use-github-5983680) 是软件版本控制和协同工作的首选。一旦你注册了 GitHub， [，将 Xcode](https://developer.apple.com/library/ios/documentation/ides/conceptual/xcode_guide-continuous_integration/PublishYourCodetoaSourceRepository/PublishYourCodetoaSourceRepository.html) 链接到它就非常容易了，所以你做的一切都会被保存下来，供你团队中的其他人访问。如果你需要一点帮助来设置 GitHub， [他们的指南](https://guides.github.com/) 会带你完成整个过程。**

**同样，iOS 8 中的测试版测试也非常简单。使用 TestFlight ，你可以简单地邀请用户加入你的团队，这样他们就可以测试你的应用了。他们只需要下载 [试飞应用](https://itunes.apple.com/us/app/testflight/id899247664?mt=8) 。**

**为 iOS 开发实际上就是让自己熟悉 Xcode。一旦你适应了，你就可以用多种语言编写你的应用程序，或者尝试学习 Swift。当你开始实际编写这个应用程序时，你肯定需要挖掘更多具体问题的答案，但是上面的工具会让你走上正确的道路。**

**祝你好运，Lifehacker**