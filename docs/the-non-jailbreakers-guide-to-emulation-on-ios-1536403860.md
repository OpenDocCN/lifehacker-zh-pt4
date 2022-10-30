# 非越狱者 iOS 仿真指南

> 原文：<https://lifehacker.com/the-non-jailbreakers-guide-to-emulation-on-ios-1536403860>

从技术上讲，你不应该在 iPhone 上安装模拟器来玩经典游戏。但这并不意味着这是不可能的。以下是如何在任何 iOS 设备上安装模拟器，不需要越狱。

Watch

如果你越狱了 ，那么在 iOS 设备上的仿真已经有很长一段时间是可能的。这仍然是更好的方法，因为它很容易安装仿真器、rom，并且 [使用控制器](http://lifehacker.com/how-to-use-a-gamepad-for-any-ios-game-not-just-emulato-5991266) 。也就是说，不是每个人都想越狱。如果你愿意做一点工作，并留意进入应用商店的流氓应用程序，你仍然可以运行模拟器。

### 从网上下载模拟器

让大多数模拟器与 iOS 一起工作的技巧是通过一个叫做侧加载的过程。这是当你从你的网络浏览器而不是官方 iTunes 应用商店安装应用程序时。在模拟器的情况下，这通常通过 [将模拟器](http://readwrite.com/2013/07/16/super-mario-zips-through-a-loophole-in-apples-app-restrictions#awesm=~oxzZLdYmqxLfOn) 注册为 [企业应用](https://developer.apple.com/support/ios/enterprise.html) 来完成。企业应用程序应该是用于私营公司向员工发布应用程序的，但任何开发者都可以制作一个。

另一条安装模拟器的路线稍微复杂一点，需要你注册成为 iOS 开发者，然后 [在自己的](http://www.aorensoftware.com/blog/2011/05/23/play-snes-games-on-your-ipad-without-jailbreaking/) 上安装模拟器。出于我们的目的，我们将坚持使用模拟器，您可以直接从浏览器下载。

我们已经 [讨论过一些你之前可以下载的模拟器](https://lifehacker.com/gba4ios-emulates-gameboy-advance-games-on-ios-no-jailb-1526268098) 。它们往往运行良好，但也有一些警告。也就是说，没有真正的安全保证，而且使用起来有点麻烦。当你从网上下载一个应用程序时，你正在安装一个来自未知开发者的未经批准的应用程序。理论上，它们可能包括恶意软件。所以， [就像在安卓](http://lifehacker.com/how-secure-is-android-really-1446328680) 上一样，你要想安装这些就要自担风险。

好消息是，大多数模拟器都是开源的，并且倾向于将它们的代码放在 GitHub 上，这样每个人都可以确保它们不包含恶意软件。比如最近的两个应用，[GBA 4 IOs](http://gba4iosapp.com/download/)(Game Boy Advance/Game Boy)和 [NDS4iOS](http://nds4ios.angelxwind.net/i/?page/downloads) (任天堂 DS)的代码都在 GitHub 上。

对于其他的模拟器，你需要通过类似 [iEmulators](http://iemulators.com/) 或者 [Emu4iOS](http://emu4ios.net/) 这样的第三方站点，从那里安装，也就是说你无法很好的查看代码。这些通常仍然建立在开源软件上，但是很难确切地知道你正在安装什么代码。

另一个问题是这些模拟器的安装有点棘手。由于他们倾向于使用过期的企业帐户证书，您通常需要更改设备的日期来安装和使用该应用程序。每个模拟器都需要不同的日期，您通常可以在模拟器网站上找到，但是安装的基本过程大体上是相同的:

1.  进入设置>通用>日期和时间
2.  关闭“自动设定”
3.  将日期更改为您想要使用的模拟器建议的年份(通常是 2012 年)
4.  在 mobile Safari 中打开模拟器的网站
5.  安装您选择的模拟器

一旦你安装了模拟器，每次你想打开应用程序的时候，你都需要把日期调回来。这很麻烦，但这是应用程序打开的唯一方式。如果你从 iEmulators 这样的网站安装，你一次只能安装一个模拟器，所以要明智地选择。

### 潜入应用商店的非官方应用

每隔一段时间，一个 [模拟器潜入 iTunes 应用商店](https://lifehacker.com/remote-file-manager-sneaks-a-snes-emulator-onto-your-ip-1245256779) 。这些通常隐藏在其他应用程序中，但有时 [它们非常明显](https://itunes.apple.com/kr/app/idos/id377135644?l=en&mt=8) 并且只需要 [变通办法来安装游戏](http://forums.toucharcade.com/showpost.php?p=1546797&postcount=54) 。

这些应用程序通常将模拟器隐藏在一系列菜单后面，因此在苹果的应用程序审查过程中不会被注意到，但它们通常会在受到任何压力时被拉出来。这里的一般经验是，在苹果删除之前，尽快下载并安装带有隐藏模拟器的应用程序。为了跟上潜入商店的应用程序，像 [TouchArcade](http://forums.toucharcade.com/forumdisplay.php?s=65a2c31c2245678317600ad54925704d&f=2) 或[iOS Gaming Subreddit](http://www.reddit.com/r/iOSGaming)这样的网站上的论坛是很好的起点。

一旦你得到了这些应用程序中的一个，就到了 [备份它的时候了](https://lifehacker.com/what-do-i-do-when-apple-removes-an-app-i-bought-from-th-5867673) 。由于苹果将从应用商店中撤出它，所以备份模拟器是很好的，这样你就可以在未来的 iOS 设备上安装它。只要您在电脑上的 iTunes 中有备份，您就可以在未来的设备上安装它。

如果其他都失败了，至少偶尔的网络应用足够强大，可以运行从 [游戏机](http://www.benmidi.com/gameboy/) 到 [任天堂](https://lifehacker.com/webnes-plays-your-nintendo-games-in-a-mobile-browser-1524412442) 的任何东西。