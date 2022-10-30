# 我想写安卓应用。我从哪里开始？

> 原文：<https://lifehacker.com/i-want-to-write-android-apps-where-do-i-start-1643818268>

亲爱的 Lifehacker，
我有一些编码方面的背景，但之前从未接触过 Android 开发。我想要开始，但是我不完全确定我需要什么。我本身不需要“学习编码”，但是我可以使用一些关于从哪里开始使用 Android 的指导。你能帮忙吗？

Watch

真诚地，
梦想着电动绵羊

亲爱的 K. Dick 先生，
你可能知道，为 Android 编写应用不仅仅是学习代码语法。如果你从未学过编码，你可以查看大量的资源 [这里](https://lifehacker.com/the-best-resources-to-learn-to-code-1517844722) 。然而，仍然有一大堆你可能不熟悉的工具和资源，你可能需要它们来制作 Android 应用。

注意:这并不意味着是对这些应用程序和资源的每个细节的全面指导。事实上，这样的指南可以更准确地描述为一本书。但是，我们将向您概述您可以使用的不同工具，以及在哪里可以找到更多信息。这些工具需要不同层次的经验，如果你以前从未接触过代码，你可能想看看上面链接的指南。然而，首先如果你准备从理论和语法转向实际的开发，这里是你需要的。

### **Android 软件开发包(或 SDK)**

Android 软件开发工具包(SDK)实际上是一个工具集，可以帮助你开发 Android 应用程序。我们将讨论 SDK 之外的更多内容，但这里有一些 SDK 中最有用的工具:

#### **Eclipse/Android Studio**

Android 有两个主要的集成开发环境(IDE)。IDE 是编写代码和组装应用程序的主程序。它可以帮助您组织和编辑应用程序中的各种文件，管理应用程序需要的包和支持库，并在真实设备或仿真器上进行测试。

Android 的默认 IDE 是 Eclipse。Eclipse 允许您修改 Java 和 XML 文件，组织应用程序的各个部分，以及许多其他任务。你从谷歌获得的版本还包括一个包管理器，一旦谷歌发布了 Android 工具，你就可以更新到最新版本。

主要的替代品是 Android Studio，目前由谷歌直接制作。像许多谷歌项目一样，Android Studio 是一个长期测试版的一部分。长期目标是让 Android Studio 取代 Eclipse，成为 Android 开发的主要 IDE。这并不一定意味着它适合所有人。例如，如果您需要使用游戏等应用程序的原生开发工具包(提示:如果您需要它，您可能已经知道您需要它)，Eclipse 是强制性的。然而，如果你想对未来有一个跳跃性的开始，并且你愿意容忍一些可能的错误，Android Studio 是一个不错的选择。

无论你选择哪种 IDE，使用它都有点像 Photoshop:它可以做很多很酷的事情，但你可能只会在需要的时候学习个别的工具。然而，这也是开始学习 Android 开发的一些基础知识的好地方。这里有一些很棒的教程和资源可以帮助你开始学习:

*   [**Udacity -开发 Android 应用**](https://www.udacity.com/course/ud853) **:** 这个为期 8 周的在线课程有大量免费内容，由谷歌工程师直接教授。本课程不仅仅是复制粘贴代码，还会帮助你学习一些你需要的核心概念和特性。
*   [**Android 开发者培训**](https://developer.android.com/training/index.html) **:** 谷歌的部分文档包括如何使用其工具的培训教程。这些文档将带您了解 IDE 的基本功能。如果你没有太多开发应用程序的经验，这可能不会让你成为一个开发高手，但它会帮助你学习工具。
*   [**沃盖拉**](http://www.vogella.com/tutorials/Android/article.html) **:** 值得一提的是这里几乎每一节的沃盖拉教程。这套庞大的教程涵盖了你能涵盖的所有内容。如果你有一个上面没有提到的基本问题，可以去问沃盖拉。

#### **亚行**

我们之前从普通用户的角度谈论过 ADB，但是这个工具的主要目的实际上是帮助开发。因此，它包含在 Android SDK 中。当它插入电脑时，您可以使用它来加载软件或对您的设备进行更改。这里有一些 [你可以在亚行使用的基本工具](http://lifehacker.com/the-most-useful-things-you-can-do-with-adb-and-fastboot-1590337225) ，但是如果你想作为一名开发人员了解更多，请查看这些:

*   [**亚行文档**](http://developer.android.com/tools/help/adb.html) **:** 这是来自谷歌的关于亚行是什么以及它如何运作的主要资源。你可以在这里找到亚行的大部分能力。
*   [**Vogella——使用 Android 调试桥**](http://www.vogella.com/tutorials/AndroidCommandLine/article.html) **:** 另一个 VO gella 教程，这一个涵盖了 ADB 如何工作的基础知识和你可以用它做的一些常见的事情。如果您不想在 Google 文档中寻找您需要的命令，这可能是一个不错的起点。

### **安卓开发者指南**

到目前为止，我们已经链接了几个来自官方 [Android 开发者指南](https://developer.android.com/develop/index.html) 的资源，这只能证明它们是多么有用。谷歌保存了大量关于如何编写应用程序的文档和资源，你可以参考或搜索。

如果你是 Android 开发的新手，浏览这里的一些教程和指南不会有什么坏处。它们的布局方式是一个借给另一个(见上面的 Android 开发人员培训)。如果你是新手，下面是一些值得复习的部分:

*   [**谷歌服务**](https://developer.android.com/google/index.html) **:** 我们之前已经讨论过 [Google Play 服务](http://lifehacker.com/why-google-play-services-are-now-more-important-than-an-975970197) ，但是在这里你可以看到幕后发生了什么。谷歌提供了各种各样的功能，否则你可能不得不自己构建，如地图和位置功能，云备份，登录服务等。你可以在这里找到它们。
*   [**API 指南**](https://developer.android.com/guide/index.html) **:** 谷歌服务是与常规 API 分开的，你也可以在这里读到。这些包括从创建基本动画的代码，到读取传感器和连接到互联网。这里有大量的信息可以为你的应用添加功能。
*   [**样本代码**](https://developer.android.com/samples/index.html) **:** 有时候看看别人在你之前是怎么做的会有帮助。本节向您展示各种函数的代码示例。这可以帮助你了解一些东西是如何工作的，或者只是在你的应用程序中使用它，这样你就不必重新发明轮子了。

### **安卓设计指南**

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-Q8TXgCzxEnw&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-Q8TXgCzxEnw&start=0) 

与开发人员指南相对应的是设计指南。谷歌越来越注重教其开发者如何制作不仅好用而且好看的应用程序。因此，这意味着已经为你做了很多工作，包括基本的按钮、简单的动画等等。

获得更多信息的地方是 [Android 设计指南](https://developer.android.com/design/index.html) ，这是谷歌官方文档的第二个主要部分。请记住，这些是为那些对视觉设计没有很好理解的人准备的，因为它与创建应用程序界面有关。换句话说，如果你已经知道你的应用程序将会是什么样子，你可能不需要这个。如果你已经知道你的应用看起来像什么，但是你*不擅长*让应用看起来更好，看看这个。

以下是一些有用的领域:

*   [**设备**](https://developer.android.com/design/devices.html) **:** 安卓的目标不仅仅是手机。这一部分将帮助你了解手机、平板电脑、电视和手表之间的联系，以及如何设计一个适应所有这些设备的界面。
*   [**模式**](https://developer.android.com/design/patterns/index.html) **:** Android 是建立在结构化界面上的。这一部分讲述了应用程序如何工作的构建模块，这样你就可以设计一个框架，你将在这个框架上构建你的设计。
*   [**材料设计文档**](https://www.google.com/design/spec/material-design/introduction.html) **:** 这在技术上暂时是一个独立的章节，但谷歌最新版本的 Android 将引入一种新型的设计语言，称为材料设计。在这里，你可以细读这意味着什么，以及如何考虑设计符合这些准则的应用程序。如果你在思考用户如何与应用程序交互方面没有经验，即使你没有遵循具体的建议，这也是有帮助的。

### **GitHub/BitBucket**

当你开发一个应用程序时，有许多文件需要管理，你需要一种方法来跟踪变化。Git 是管理现有软件的新版本或变更的最常用协议之一。当然，它比基本的备份工具要复杂一些。它足够灵活，允许您管理应用程序的多个不同分支，以及在出现问题时从旧版本中提取。

用 Git 管理项目的两个最常见的服务是 Github 和 Bitbucket。两者都使用相同的底层协议，可以直接集成到 Eclipse 或 Android Studio 中。BitBucket 允许你不用付钱就可以拥有一些私有的存储库(读作:项目的存储)，而 GitHub 的免费提供则要求它们公开上市，除非你多付一点钱。这里有一些资源可以帮助你开始使用 Git:

*   [**BitBucket 教程**](https://www.atlassian.com/git/tutorials/)**:**BitBucket 的制作者 Atlassian 有一系列关于如何入门 bit bucket 并在这里导入你的项目的指南。以我个人设置 BitBucket 和 GitHub 的经验来看，这项服务和这些指南对于外行来说更容易上手。
*   [**GitHub 指南**](https://guides.github.com/) **:** GitHub 同样有一些关于如何设置其服务的教程，你可以在这里找到。在某些情况下，有些指南引用了该软件的旧版本，但一般来说，您应该能够开始使用这些版本。
*   [**沃盖拉 Git 教程**](http://www.vogella.com/tutorials/Git/article.html) **:** 沃盖拉还有另一个很棒的教程，解释 Git 本身是什么，以及它如何帮助你管理你的整个项目。虽然版本管理是 Git 的主要功能，但 Vogella 还可以带您了解更多内容。

为 Android 开发不仅仅是将 Java 放在文本编辑器中。如果你有一点点编写代码的经验，但还没有一头扎进实际的应用程序开发中，你可能还没有意识到你需要知道很多。好消息是，你不是第一个走这条路的人。这些只是你需要的一些工具，希望这些指南能让你走上正确的道路。

真诚地，
Lifehacker