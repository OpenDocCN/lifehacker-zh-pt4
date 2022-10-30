# 如何隐藏电脑上的文件

> 原文:[https://life hacker . com/how-to-hide-files-on-your-computer-1642112044](https://lifehacker.com/how-to-hide-files-on-your-computer-1642112044)

有时候，你需要在你的电脑上保存一些你不想让其他人看到的文件。无论是礼物清单还是色情收藏，隐藏文件都很容易。下面是怎么做的。

Watch

### 级别 1:使用隐藏文件夹

如果你只是想把一些文件藏起来，避免被人窥探，那么使用电脑内置的隐藏文件夹是一个简单的方法。这不会真的对知道他们在做什么的人隐藏文件，但它会使他们看不见，所以人们不会偶然发现他们。把它想象成在你的床垫下藏东西的数字等价物。

#### 在 Windows 上

在 Windows 中隐藏文件相当容易:

1.  选择要隐藏的文件或文件夹
2.  右键单击并选择属性
3.  单击常规选项卡
4.  单击“属性”部分中“隐藏”旁边的复选框
5.  单击应用

现在，您选择的文件已被隐藏，人们在查看您的文件夹时将看不到它们。当你需要再次查找那些文件时，只需将 [中的隐藏项转到](https://lifehacker.com/navigate-files-like-a-pro-with-these-windows-explorer-t-1466669311) 上即可。

#### 在 Mac 上

在 Mac 上，您将使用快速终端命令来隐藏文件夹。只需在“终端”中键入以下内容，用您想要隐藏的文件夹替换/path/to/folder:

`chflags hidden /path/to/file-or-folder`

要取消隐藏，请键入:

`chflags nohidden /path/to/file-or-folder`

如果您不知道想要隐藏的文件夹的完整路径，请键入命令，然后将该文件或文件夹拖到终端窗口中。或者，你可以把那个文件夹放进你的图书馆文件夹 里。

### 第二级:使用应用程序来隐藏搜索和历史记录中的文件

如果隐藏文件夹对你来说太难了，你可以使用第三方应用程序来隐藏文件。同样，这些应用程序并没有真正保护你的数据，但他们确实做到了这一点，所以没有人会随便看到你不想让他们看到的文件。

#### 隐藏 Windows 的“我的密码箱”文件夹

[我的密码箱](http://fspro.net/my-lockbox/) 把你的个人文件塞进应用程序，需要密码才能解锁。我的密码箱里的任何东西都不会出现在搜索中，所以你不必担心有人会看到你的文件。这里没有加密，所以虽然它不是超级安全，但它很快而且易于使用。

#### 对 Mac 使用 Skedaddle 或 Obscurity

在 Mac 上，你有两个可靠的选项来使用应用程序隐藏文件夹。首先是前面提到的(2.99 美元)。有了 Skedaddle，你可以在桌面上找到一个隐藏的空间来放文件夹。此处的文件不会在 Spotlight 搜索或 Finder 中显示。也就是说，任何人只要知道拉起 Skedaddle 的快捷键，就可以很容易地访问它们。

另一个窍门是使用类似前面提到的 [默默无闻](http://www.mednotes.net/about/portfolio/programmer/) 的 app。尽管如此，称晦涩为应用并不完全正确。它实际上只是一个虚拟的应用程序，你可以把文件放在里面。只需右键单击晦涩，并选择“显示包内容。”在这里，您可以将所有文件转储到应用程序容器中。这些文件不会显示在搜索或 Finder 中。这并不真正安全，因为任何人都可以访问它，但很可能没有人会只是在你电脑的应用程序文件夹中挖来挖去，右键单击每个应用程序。

### 第三级:加密文件，把它们永远锁起来

隐藏应用程序或用密码保护它们在安全方面并没有多大作用。如果你真的想保护这些文件，你需要 [加密它们](https://lifehacker.com/a-beginners-guide-to-encryption-what-it-is-and-how-to-1508196946) ，这样没有人可以在没有密码的情况下访问它们。这将会稍微减慢你访问这些文件的速度，但是这绝对是最安全的隐藏方法。你有一个 [吨不同的选项来加密文件](https://lifehacker.com/five-best-file-encryption-tools-5677725) ，但最简单的方法是创建一个加密的 ZIP 文件。

#### 使用 7-Zip for Windows 加密文件

在 Windows 上，我们喜欢使用 [7-Zip 作为归档工具](http://lifehacker.com/the-best-file-archive-utility-for-windows-5820410) ，这也是一种加密文件的简单方法。

1.  右键单击要加密的文件夹或文件
2.  选择 7-Zip >添加到存档...
3.  将存档格式更改为 ZIP
4.  将加密方法更改为 AES-256
5.  输入密码，然后单击确定

现在，你的文件将被藏在一个有密码保护的档案室里，没有人能找到它们。ZIP 文件会在搜索中显示，但其内容不会。如果你愿意，也可以使用上面的方法隐藏压缩文件，这样更安全。

7-Zip 并不完美——访问你的文件可能会有点慢——所以另外，你可以使用加密程序。TrueCrypt 是超级简单的 ，但已经不再开发，所以它不像许多人希望的那样安全(尽管它肯定会把普通用户挡在你的文件之外)。 [BitLocker](http://windows.microsoft.com/en-us/windows7/products/features/bitlocker) 是另一个不错的选择，尽管你需要 Windows 7 旗舰版、Windows 7 企业版或 Windows 8 专业版才能使用它。

#### 使用 Mac 上的“磁盘工具”来加密文件

你不需要在 Mac 上安装额外的软件来加密文件。您可以使用内置的磁盘工具应用程序。

1.  启动磁盘工具
2.  选择文件>新建>文件夹中的磁盘映像
3.  选择要加密的文件夹
4.  从加密下拉菜单中选择 256 位 AES 加密
5.  键入密码

就这样，您现在已经加密了您的文件夹。继续使用上面的一个步骤来隐藏它，增加一层安全保护。如果你正在寻找加密一吨的文件， [我们喜欢](https://lifehacker.com/hider-2-secures-and-hides-files-on-your-mac-1564742428) [Hider 2](http://macpaw.com/hider) 因为它也创建了一个可浏览的文件系统。

### 额外收获:隐藏文件内部的文件

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-bnHVSXbXdnQ&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-bnHVSXbXdnQ&start=0) 

把文件藏在奇怪的文件夹里，并在档案室里加密，并不是让它们远离窥探的唯一方法。您还可以将文件隐藏在其他文档中。例如，您可以 [隐藏 Office 文档](https://lifehacker.com/hide-secret-files-in-office-2007-documents-5538370) 中的文件，甚至可以隐藏 JPEG 图像 中的文件。在 之前，我们已经带你通过 [隐写工具隐藏文件，所以如果你正在寻找一种更炫的方法来隐藏你的文件，值得一看。](http://lifehacker.com/geek-to-live-hide-data-in-files-with-easy-steganograph-230915)