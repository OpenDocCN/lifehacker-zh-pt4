# 如何用 Wineskin 在 OS X 上运行你最喜欢的 Windows 程序

> 原文：<https://lifehacker.com/how-to-run-your-favorite-windows-programs-on-os-x-with-1660969393>

如今，有很多适用于 Mac 和 Windows 的软件问世，但总有一些游戏或应用程序没有进入 OS X。谢天谢地，你可以通过一个名为 Wineskin 的免费应用程序，轻松地将许多 Windows 程序移植到 OS X。



Wineskin 是一个免费的开源工具，可以将 Windows 程序移植到 OS X，这样你就可以在本地运行它们。它建立在 [酒](http://en.wikipedia.org/wiki/Wine_(software)) 之上，是一个为开发者快速移植软件而打造的引擎。有几个应用程序可以做到这一点，如前面提到的[wine bottler](http://lifehacker.com/winebottler-turns-windows-programs-into-standalone-os-x-5440703)或商业软件如 [CrossOver](https://www.codeweavers.com/products/) ，但我们最好的运气是与 Wineskin 一起工作。

由于 Wineskin 的工作方式，你将无法玩最新的、图形最密集的游戏或耗电软件。但是你可以移植不占用大量资源的旧软件和轻量级游戏(就像许多独立游戏一样)。对于更密集的程序，你可能会想用苹果的 Boot Camp 软件 代替 [双启动窗口](https://lifehacker.com/how-to-run-windows-and-all-your-favorite-windows-progr-5887081) 。

软件可能会在 Boot Camp 上运行得更好，但 Wineskin 很棒，因为你可以移植你最喜欢的程序，并在 OS X 运行它——无需购买 Windows 或重启计算机。这样一来，让我们移植一些软件。我们已经用许多应用测试了 Wineskin，但我们将使用 [Torchlight II](http://www.torchlight2game.com/download) 作为我们的样本，因为 [Mac 端口似乎已经死了](http://kotaku.com/a-couple-of-readers-have-asked-about-torchlight-2s-much-1006075540) 。

### 第一步:下载 Wineskin 并更新包装器

开始之前，你需要 [下载 Wineskin](http://wineskin.urgesoftware.com/tiki-index.php?page=Downloads) 。一旦你得到了它，继续拖动文件到你的应用程序文件夹，并启动它。如果您还没有，也下载您选择的程序的 Windows 安装程序(在这种情况下，Torchlight II 安装程序)。

您将在 Wineskin 中更新两个不同的东西:包装器和引擎，而不是总是更新程序本身。下一步您将进入引擎，但是您现在只需点击“update”按钮就可以更新包装版本。包装器是一组注册表文件和一个假的 C:驱动器。您需要为想要移植的每个应用程序制作一个新的包装器。

### 第二步:安装一个 Wineskin 引擎

接下来，是时候安装一个 Wineskin 引擎了。这就是事情变得有点奇怪的地方。引擎包括一系列可以帮助您运行软件的设置。最新版本是 WS9 1.7.29。你可以下载并使用旧的 Wineskin 引擎，某些引擎比其他引擎更兼容某些游戏。只需单击“+”按钮，选择您想要用于软件端口的引擎。

当我第一次尝试运行火炬之光 II 时，我使用了最新版本的 Wineskin 引擎，但无法让它工作。所以，我做了一些调查来找出原因。谢天谢地，Wine HQ 提供了一个 [软件兼容性](https://appdb.winehq.org/objectManager.php?sClass=category&iId=0&sAction=view&sTitle=Browse+Applications) 的庞大列表。在 [搜索火炬之光 II](https://appdb.winehq.org/objectManager.php?sClass=version&iId=26690) 后，我发现它只适用于 WS9 1.7.16。

所以，在你选择你的引擎之前，在 Wine HQ 上挖掘一下，看看其他人对兼容性有什么看法。最新的版本并不总是最好的，所以选择与你想移植的软件最兼容的引擎。

### 第三步:创建包装器

现在您已经选择了引擎，是时候创建一个包装器了:

1.  点击“创建新的空白包装”按钮，并命名您的应用程序。Wineskin 需要一些时间来构建包装器
2.  现在，您可能会收到一些不同的安装软件的通知。我只好下载安装了 [单声道](http://wiki.winehq.org/Mono) 和 [壁虎](http://wiki.winehq.org/Gecko) 。继续点击 Wineskin 让你点击的任何东西上的“安装”按钮
3.  完成后，您会收到一条提示，要求您在 Finder 中打开该文件。单击“是”在 Finder 中打开一个窗口

您的包装器现在已经创建好了。不过，在安装软件之前，您需要尝试一些选项。

### 第四步:配置你的包装器

接下来，是时候对您的包装进行一些调整了。双击 Finder 中的文件(第一次你可能会得到一个错误信息，如果你这样做，只需再次双击它)，你将打开包装设置。

你会在这里看到三个选项:安装软件、设置屏幕选项和高级。除非你知道你的软件是完全兼容的，没有额外的设置，暂时不要安装。相反，请单击“高级”

高级设置有大量的选项，其中大部分都很混乱。在您的主配置选项卡上，您可以设置一个特殊的 Windows EXE 文件来打开，更改应用程序图标，并根据需要重命名应用程序。“工具”标签有大量不同的选项来改变配置，安装特殊的 Winetricks 来使软件更加兼容，以及重新构建你的包装器。WineTricks 是一个将基本组件安装到您的包装器中的脚本。这些通常是可以修复端口问题的 Microsoft DLL 文件和字体。有十亿种葡萄酒技巧可供选择，但你会在这里 找到安装它们的 [指南。“选项”选项卡为您的软件提供了更多选项，包括更改三键鼠标的工作方式、ALT 键的工作方式等等。](https://code.google.com/p/winetricks/)

乍一看，所有这些东西都令人难以理解。不过不要担心。您有几个选项来确定需要更改哪些设置。

你首先要查的地方是 [酒总部](https://www.winehq.org/) 。如果你想安装流行软件，你通常会在 Wine HQ 上找到安装指南。看看 [战队要塞 2 页](https://appdb.winehq.org/objectManager.php?sClass=version&iId=9901) 为例。你安装的每一个软件都需要一套定制的包装设置，所以每次你想创建自己的端口时，都要准备好钻研这些页面。

不幸的是，火炬之光 II 在葡萄酒总部没有一个很好的页面。于是，我求助于谷歌，找到了我的系统管理员 关于如何让它工作的帖子。下面是我必须配置的要点，只是为了让您了解这一步会发生什么:

1.  点击“高级”按钮。
2.  点击顶部的“工具”标签，然后点击“Winetricks”。
3.  从顶部的搜索字段中键入“msxml3”，选择它并运行。
4.  按照步骤下载文件，手动，并把它放在文件夹中，并重新运行。
5.  搜索 vcrun2010，选择并单击运行按钮。
6.  按照提示操作。
7.  点击“关闭”按钮关闭 Winetricks 窗口。
8.  在“工具”选项卡下，单击“配置实用程序”。
9.  单击图形选项卡。
10.  选择“在全屏窗口中自动捕捉鼠标”。
11.  单击应用。
12.  单击“库”选项卡。
13.  在“库的新覆盖”下选择 dwrite，然后单击添加按钮。
14.  选择 dwrite 覆盖，然后单击编辑按钮。
15.  选择禁用，然后单击确定。
16.  单击应用和确定。

显然，不是所有的软件都需要这么多的配置，但是有些软件会需要。除非你是一个擅长阅读错误日志的 Windows 高手，否则我建议你在尝试安装软件之前先搜索一下有效的配置设置。

### 第五步:安装并运行你的软件

既然所有的配置废话都已经解决了，是时候真正安装您的软件了。

1.  点击 Wineskin 高级页面上的“安装软件”。
2.  单击“选择安装程序可执行文件”。
3.  选择您的设置或安装您之前下载的 EXE 文件(在火炬之光 II 的情况下，它是火炬之光 2_FullInstall_v1.21.exe 文件)。
4.  像在 Windows 电脑上一样运行安装程序。

安装过程完成后，您应该可以运行您的软件了。

您可以在 Wineskin 文件夹(用户>应用程序> Wineskin)中找到您的端口。只需双击您新创建的应用程序即可运行它。如果一切正常，它就会加载，你可以像使用 Mac 应用程序一样开始使用它。

如果你安装了一个游戏，你可能想在开始前弹出设置，并放下任何图形设置。由于这是一个被黑在一起的软件端口，事情往往有点慢，所以你最好从低图形设置[开始，然后向上移动。](http://lifehacker.com/get-more-from-your-games-a-beginners-guide-to-graphics-5985304)

### 步骤六:如何返回包装器配置页面

如果你的软件不能正常工作，或者你需要重新配置一些东西，你可以回到包装设置，而不需要全部重新安装:

1.  前往您的 Wineskin 文件夹(用户>应用程序> Wineskin)
2.  右键单击要编辑的应用程序，然后选择“显示包内容”
3.  双击 Wineskin.app 文件以重新打开 Wineskin 设置

就是这样！如果需要，您可以重新配置任何设置或使用不同的选项。

移植软件可能会给你带来好运，但如果你想在 Mac 桌面上运行 Windows 软件，而不必安装虚拟机或用 Boot Camp 对你的驱动器进行分区，这值得一试，花 20 分钟的时间..