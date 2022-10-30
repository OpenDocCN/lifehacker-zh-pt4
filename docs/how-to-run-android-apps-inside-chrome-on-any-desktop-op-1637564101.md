# 如何在任何桌面操作系统上运行 Chrome 内部的 Android 应用程序

> 原文:[https://life hacker . com/how-to-run-Android-apps-inside-chrome-on-any-desktop-op-1637564101](https://lifehacker.com/how-to-run-android-apps-inside-chrome-on-any-desktop-op-1637564101)

近日，谷歌为 Chrome 提供了首批安卓应用 [。一些聪明的用户将这种能力赋予每个人只是时间问题。现在是时候了。以下是如何在任何操作系统上安装(几乎)任何安卓应用。](https://lifehacker.com/the-first-android-apps-are-now-available-for-chrome-os-1633549691)

Watch

**显而易见的免责声明:**这仍然是 800 万种坏的，这里绝对没有任何保证。除了没有官方支持的应用程序，你还会在 Chrome 中摆弄一些低级的东西。这可能不是您应该在工作计算机上尝试的事情，也不应该期望这很简单或没有错误。这个过程与这两件事是相反的。**您将需要 Chrome 37+来阅读以下指南。**

### **词汇表**

这个过程相当新，所以为了简单起见，我们先定义几个术语:

Chrome 的应用运行时(或 ARC)是允许 Android 应用在 Chrome 上运行的软件。同样的方式，ART(和老一点的 Dalvik )目前也在 Android 上运行 Android 应用程序。通过为 Chrome 制作 Android 运行时的修改版本，谷歌可以允许开发人员添加对 Chrome 的支持，而无需从头开始重建他们的应用程序。

**ARChon 定制运行时:** ARC 目前官方只针对 Chrome OS 设计。为了解决这个问题，开发人员 vladikoff 创建了 ARChon 自定义运行时，它不仅允许 Windows、OS X 和 Linux 运行 Android 应用程序，还取消了运行数量的限制。

**Google Play 服务:**我们过去已经讨论过 [什么是 Google Play 服务](https://lifehacker.com/why-google-play-services-are-now-more-important-than-an-975970197) 。正如我们之前解释的那样，应用程序开发人员可以插入这些 API 来获得预先编写的功能。把它们想象成谷歌给开发者的应用程序插件。在本文的上下文中，我们将根据应用程序是否包含 Google Play 服务的功能来讨论 Chrome 是否支持这些应用程序。

**未打包的扩展:**扩展通常来自 Chrome 网上商店或者预先打包在一个. CRX 文件中。出于 Android 应用的目的，我们将使用未打包的扩展。这些文件夹包含一个扩展的所有文件(或者，在这种情况下，Android APK)。它们的功能与扩展相同，但是没有包装在一个文件中。

### **第一步:安装执政官运行时**

Chrome OS 使用专门的运行时，允许 Android 应用程序在其中本地运行。这意味着它不是一个仿真器或虚拟化栈，而是一个合适的运行时。通俗地说，Chrome OS 使用的是安卓直接运行软件的同类型引擎。因此，你可以从 Chrome 启动器中启动安卓应用，而不是像 Genymotion 那样在电脑上运行整个安卓手机。

首先，我们需要下载执政官自定义运行时。这是在 Windows、OS X 和 Linux 中运行 Android 应用程序所必需的。虽然从技术上讲，你可以在 Chrome 操作系统中运行 Android 应用，但目前你只能运行四个应用中的一个。本文其余部分中的方法将通过欺骗这些应用程序上的签名密钥来运行替代应用程序，但是如果您想运行任何您想要的应用程序，请下载 ARChon。方法如下:

1.  下载执政官运行时 [这里](https://bitbucket.org/vladikoff/archon/get/v1.0.zip) 。
2.  解压存档文件。
3.  进入“功能表”>“更多工具”>“扩展”,打开 Chrome 中的扩展页面
4.  如果尚未启用，请在右上角启用开发人员模式。
5.  选择“载入未打包的扩展”
6.  选择包含您之前解压缩的 ARChon 运行时的文件夹。

执政官运行时现在将作为 Chrome 的扩展运行。您可能会在扩展页面上看到如下警告。然而，这些都是正常的，不应该影响你运行 Android 应用的能力。

接下来，你需要运行一些 Android 应用程序。这有点复杂，因为 Android APKs 没有为 Chrome 正确打包。然而，只要一点点努力(或者你友好的邻居互联网的一些帮助)，你就可以让其中一些启动。它们的功能是否正常完全是另一回事。

### **第二步:安装现有的安卓应用**

获得一些可用的 Android 应用程序的最快、最简单的方法是在网上找一些。像这样的论坛已经在努力获得一些功能。然而，这与 Play Store 上的 130 万个应用相去甚远。虽然由于不兼容的问题，其中大部分可能还在你的能力范围之外，但我们也将看看如何(尝试)创建你自己的。

**免责声明:**一般来说，分发修改过的应用程序在某种程度上侵犯了版权。实际上，下载一个修改前的应用程序和下载普通版本并自己修改没有什么区别。出于这个原因，任何一个免费应用的开发者都不会太在意你是否下载了一个修改过的应用来玩。但是，下载一个修改过的付费 app 就是盗版。请支持开发者，不要不付费就下载付费应用的修改版。此外，不言而喻，如果一个应用在 Chrome 中出现问题，不要写差评或批评开发者。你在这里只能靠自己了。

一些乐于助人的互联网用户创建了一个不断增长的应用程序清单。你可以在那个文档中找到下载链接，或者在当前致力于 Chrome APKs 的社区 中找到更多。一旦您有了包含这些修改过的 apk 之一的. zip 文件，下面是安装它的方法:

1.  解压文件并将文件夹(可能命名为“com.twitter.android”)放在一个容易找到的地方。
2.  在 Chrome 中打开扩展页面。
3.  点按“载入未打包的扩展”
4.  选择包含您下载的修改过的 APK 的文件夹。

该应用现在将出现在你的 Chrome 扩展列表中。如果你是 Chrome 应用的特别粉丝，你可能还会注意到一个快捷方式被添加到了 [Chrome 应用启动器](https://lifehacker.com/googles-chrome-app-launcher-runs-chrome-apps-from-the-838022840) 。根据它的包装方式，它可能会有一个良性的 Android 图标和软件包名称，而不是一个正确的应用程序名称。

### **(可选)第三步:为 Chrome 重新打包你自己的安卓应用**

有几种方法可以制作和调整 apk，使它们可以在 Chrome 上运行。这些方法也在积极开发中，所以如果你在后面读到这篇文章，可能会有更简单的方法来转换它们。为了完整起见，我们将介绍如何安装 chromeos-apk 工具 ，以及如何手动转换它们，如果你需要做任何额外的调整。

#### **视窗:**

1.  下载 node.js。msi 文件(**不是**了。exe)从的[到这里的](http://nodejs.org/download/)的。
2.  安装 node.js。
3.  在命令提示符下，运行以下命令:npm install chromeos-apk -g

就是这样。现在，chromeos-apk 工具已经安装在您的机器上，您可以从命令行中的任何文件夹调用它。你可以直接跳到下一节如何使用它。

#### **OS X/Linux:**

chromeos-apk 工具最初是为 Linux 和 OS X 设备开发的。下面是如何在那里安装它:

1.  在终端中，运行以下命令:`sudo apt-get install npm`
2.  *(仅限 Ubuntu):*运行以下命令:`sudo apt-get install lib32stdc++6`
3.  下载 [node.js](http://nodejs.org/) 。
4.  解压你从上面链接下载的 tar.gz 文件。
5.  根据自述文件，打开包含 node.js .的解压缩文件夹的终端，并按顺序运行以下命令:
6.  `./configure`
7.  `make`
8.  `make install`
9.  运行命令:`sudo npm install chromeos-apk -g`
10.  要确保您已更新到最新版本(现在或将来)，请运行:`sudo npm install -g chromeos-apk@latest`

#### **如何使用 Chromeos-apk 工具**

现在，您的机器上已经安装了 chromeos-apk 工具。要使用它，首先你需要获得一个 APK。如果你试图转换一个免费的应用程序，你可以使用 [这个工具](https://lifehacker.com/apk-downloads-lets-you-pull-apk-files-directly-from-goo-1456775931) 直接从 Play Store 拉一个 APK。你也可以使用 [这个工具](http://lifehacker.com/myappsharer-pulls-and-shares-apks-installed-on-your-pho-1504913643) 从你手机上安装的应用程序中获得一个 APK。许多文件管理器和备份工具，如 es 文件资源管理器和钛备份也可以拉你的设备上的 apk。

一旦你有了你的 APK，创建一个 Chrome 友好的版本就非常简单了。在存储 APK 的文件夹中打开命令提示符或终端，然后执行以下操作:

1.  运行以下命令:`chromeos-apk [NAME OF APK]`
2.  示例:`chromeos-apk com.evernote.apk`
3.  如果出现提示，请输入应用程序的包名称。这通常可以在播放商店列表的 URL 中找到。例如，在 [这个 URL](https://play.google.com/store/apps/details?id=com.evernote) 中，后面的部分“？id= "是包名。本例中为“com.evernote”。

你现在有了一个修改过的 APK，可以使用 Chrome 了！您可以使用本文前面的步骤 2 中的相同说明来安装它。也就是说，打开您的扩展页面，点击“Load unpacked extension”，并选择您刚刚创建的文件夹。

在撰写本文时，chromeos-apk 工具仍然只能让应用程序工作。它不会移除按键(这允许你同时运行多个应用程序)，也不会修复应用程序图标。我们将在清理部分处理这个问题。

#### **备选方案:手动转换 APKs】**

如果你不能(或者不想)使用命令行工具来修改 apk 以适应 Chrome 的使用，你可以自己重新打包。你仍然需要从 Github[这里](https://github.com/vladikoff/chromeos-apk) 下载 chromeos-apk。你还需要一个有问题的应用程序的 APK，所以使用上一节描述的方法来获得它们。然后，按照以下步骤操作:

1.  你下载的 chromeos-apk 工具里面有一个名为“_template”的文件夹。在其他地方复制一份(最好在你下载的 APK 附近)。
2.  将 APK 复制到“_template > Vendor > chromium > crx”中。在正确的文件夹中应该有一个自述文件，上面写着“APK 在这里”在正确的文件夹中。
3.  将“_template”文件夹重命名为包名。包名通常可以在 Play Store 列表 URL 中的“？id= "。
4.  修改包的主文件夹中的“manifest.json”文件。使用像这样的应用程序，这要容易得多。
5.  将应用程序的包名(如“com.pandora.android”)添加到“包名”栏。
6.  将应用程序的常规名称(如“Pandora”)添加到“名称”栏。
7.  删除名为“key”的条目，它将有一个很长的、看似随机的值字符串。
8.  将修改后的 JSON 文件保存为“manifest.json ”,并用编辑后的新版本替换现有版本。
9.  从 Play Store 下载应用图标。
10.  在一个 Play Store 列表页面 [像这样一个](https://play.google.com/store/apps/details?id=com.pandora.android) ，右键点击图标图片。
11.  在 URL 栏中，将“w300-rw”更改为“w128”。按回车键。
12.  右键单击新图像，并在修改后的模板文件夹的主文件夹中将其另存为“icon.png”。

恭喜你！您刚刚手动修改了一个 APK，可以在 Chrome 中运行。整个过程并不十分复杂，如果你手动修改每个应用程序，这只是很耗时。

您还会注意到，这个过程不涉及更改应用程序本身。APK 坐落在一个精致的包装里。要么成功，要么失败。时间将会证明 Android 应用程序是否能够或者将会成为桌面应用的目标，但是现在如果你真的想尝试的话，闸门已经向修补者们敞开了。