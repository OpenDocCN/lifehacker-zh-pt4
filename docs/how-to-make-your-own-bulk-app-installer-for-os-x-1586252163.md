# 如何为 OS X 制作自己的批量应用安装程序

> 原文:[https://life hacker . com/how-to-make-your-own-bulk-app-installer-for-OS-x-1586252163](https://lifehacker.com/how-to-make-your-own-bulk-app-installer-for-os-x-1586252163)

设置新 Mac 最糟糕的部分是找到并下载你所有的软件。很费时间，很无聊，通常感觉是在浪费时间。令人欣慰的是，只需一点点设置，你就可以用家酿啤酒和家酿啤酒桶自动完成整个过程，这样你就再也不用做了。

Watch

### 什么是自制？

[家酿](http://brew.sh/) 是一个命令行工具，可以自动下载你想安装在新电脑上的大部分应用程序。本质上，您只需在“终端”中键入一个命令来下载和安装软件，而不是在浏览器中搜索、下载，然后运行安装程序。这包括像[Chrome](https://www.google.com/intl/en-US/chrome/browser/)[aText](http://www.trankynam.com/atext/)等等。一旦你设置了 Homebrew，你可以保存你的安装脚本并在几秒钟内设置好你的新 MAC。基本上，家酿简化了下载和编译软件的过程。一般来说，它是通过从 GitHub 这样的网站下载源代码来实现的。

我们还将使用 [家酿木桶](http://caskroom.io/) ，它允许家酿啤酒一次下载流行的程序。家酿更专注于安装开发者工具，家酿木桶让你安装更常见的软件，如 Chrome 或 Spotify。你需要安装自制酒桶。

### 第一步:安装自制啤酒和自制啤酒桶

你需要做的第一件事是安装自制软件。因此，打开终端(在应用程序>实用程序中)并键入以下命令:

```
ruby -e "$(curl -fsSL "https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

一旦完成，我们将安装家酿桶，并将其连接到家酿。在终端中键入以下两条命令:

```
brew tap caskroom/cask
```

```
brew install caskroom/cask/brew-cask
```

就是这样！家酿啤酒和家酿啤酒桶现在都已安装。

### 第二步:熟悉木桶

既然家酿啤酒和家酿啤酒桶已经安装好了，是时候让自己熟悉一下家酿啤酒桶是如何工作的了。从技术上讲，如果您只想创建一个新的系统安装脚本，可以直接跳到第三步，但是在继续之前，最好先了解一下自己的方向。

家酿木桶有几个你想知道的基本命令。你有四个可能比其他人用得更多的命令:搜索、安装、卸载和清理。

要安装应用程序，请在“终端”中键入以下内容:

```
brew cask install app name
```

要卸载:

```
brew cask uninstall app name
```

家酿木桶为不总是直观的应用程序使用特定的名称。因此，如果您不确定某个应用程序的具体名称，您可以搜索它:

```
brew cask search app name
```

如果你想看到每一个可以下载的应用程序，请输入:

```
brew cask search
```

在你安装了一堆软件后，你也可以进行清理，删除所有你不再需要的下载文件:

```
brew cask cleanup
```

虽然这四个命令几乎是你经常使用的唯一命令，但家酿木桶有一吨。您可以通过键入以下命令获得完整的命令列表:

```
brew cask
```

有了这个，你就能很好地掌握自制啤酒和自制啤酒桶能做什么，不能做什么。

### 第三步:创建一个安装脚本

现在，我们将列出希望包含在安装脚本中的每个程序。为此，我们需要确保应用程序可用于家酿木桶。所以，我们会逐一寻找。例如，如果你想包括 Chrome，你可以输入:

```
brew cask search chrome
```

这将显示:

```
==> Partial matches   <br>chrome-remote-desktop-host  google-chrome  chromecast
```

现在我们知道“google-chrome”是我们需要的程序名。我们将使用这些信息通过文本编辑器来制作一个脚本。

打开你选择的文本编辑器( [我们喜欢 TextMate](http://lifehacker.com/the-best-programming-text-editor-for-mac-5817833) )，并创建一个新的脚本。首先，我们需要告诉文件这是一个脚本，所以要做第一行:`#!/bin/sh`。接下来是安装命令列表。这里有一个例子，它从 2013 life hacker Pack for Mac 中抓取了除 Wunderlist 和扩展包之外的所有内容:

```
#!/bin/sh <br>brew cask install quicksilver <br>brew cask install notational-velocity  <br>brew cask install evernote <br>brew cask install atext <br>brew cask install google-chrome <br>brew cask install sparrow <br>brew cask install adium <br>brew cask install skype <br>brew cask install reeder <br>brew cask install vlc <br>brew cask install handbrake <br>brew cask install plex-media-server <br>brew cask install picasa <br>brew cask install spotify <br>brew cask install dropbox <br>brew cask install utorrent <br>brew cask install skitch <br>brew cask install growlnotify <br>brew cask install crashplan <br>brew cask install the-unarchiver
```

完成后，将文件保存为`caskconfig.sh`。考虑到你想在新电脑上运行它，把它保存在 Dropbox 这样的云存储服务上或者 u 盘这样的外部驱动器上是个好主意。一旦保存，我们需要使它可执行。回到终端，指向文件的目录，然后输入:

```
chmod a+x caskconfig.sh
```

现在，在一个新系统上，按照第一步安装家酿啤酒和家酿啤酒桶。然后，将`caskconfig.sh`移动到您的个人目录中，并在“终端”中键入以下内容来安装您的所有应用程序:

```
./caskconfig.sh
```

就是这样！您刚刚创建了自己的定制安装包，让在新 Mac 上安装新应用变得轻而易举。