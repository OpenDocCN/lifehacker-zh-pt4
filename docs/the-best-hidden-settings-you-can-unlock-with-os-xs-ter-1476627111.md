# 最好的隐藏设置，你可以用 OS X 的终端解锁

> 原文:[https://life hacker . com/the-best-hidden-settings-you-can-unlock-with-OS-xs-ter-1476627111](https://lifehacker.com/the-best-hidden-settings-you-can-unlock-with-os-xs-ter-1476627111)

MAC 电脑并不以其定制选项而闻名，但如果你愿意深入了解终端，你会发现它隐藏了很多东西。这里有一些我们最喜欢的隐藏设置，你只需要一两行文字就可以改变。

Watch

### 什么是终端？

如果你不熟悉它，终端是一个应用程序，包括在你的实用程序文件夹内的 OS X，这是一个基于文本的方式来使用你的操作系统。本质上，它允许你用文本命令而不是鼠标和图形界面与 OS X 互动。作为一名 Mac 用户，你可能不会经常钻研终端，但在幕后隐藏着大量的设置和调整。终端是揭露这些的好地方。

使用终端很简单:只需打开它，键入命令，然后按回车键。您的命令可以操作文件、启动程序、更改设置等等。这看起来很复杂，但实际上这是访问计算机上某些内容的最简单的方法。在 之前，我们已经 [谈到了命令行的基础知识，所以如果你需要的话，你可以在那里温习一下初学者技巧。我们已经](https://lifehacker.com/a-command-line-primer-for-beginners-5633909) [涵盖了大量的高级功能](https://lifehacker.com/become-a-command-line-ninja-with-these-time-saving-shor-5743814) 。

但是，不要让这些吓倒你。今天，我们将看看一些非常简单的命令，启用或调整隐藏的 OS X 选项。你不需要成为一个终端专家来完成这些——只需要从这篇文章中复制并粘贴命令，粘贴到终端中，然后按回车键来尝试它们。这里有一些我们最喜欢的调整。

### 自定义 OS X 的外观

人们喜欢用终端做的一件事是改变 OS X 的一系列设置，而苹果并不完全允许他们这么做。这可能会改变 dock、滚动条的外观，或者只是让你可以看到隐藏的文件。

#### 将 Mac 的 Dock 移到角落

不喜欢 dock 在屏幕中央？您可以使用此终端命令将它移动到您想要的任何角落:

```
defaults write com.apple.dock pinning -string end  killall Dock
```

如果你更愿意将 dock 移动到顶部或回到默认位置，只需将单词`end`替换为`start`或`middle`即可。

#### 向您的桌面添加小部件

不管你喜不喜欢，苹果公司似乎都不会介意在 OS X 的仪表盘上放些小工具。如果您喜欢在桌面上使用这些小部件，可以使用以下命令:

```
defaults write com.apple.dashboard devmode YES
```

现在，注销并重新登录。打开您的仪表板，用鼠标点击并按住您想要的小部件，然后按 F12 将它放到您的桌面上。如果小部件没有出现，跳回终端并键入:

```
killall Dock
```

要颠倒这个过程，只需反过来做上面的事情，将第一条命令中的`YES`改为`NO`。

#### 默认情况下显示隐藏文件

OS X 隐藏各种文件，以防止你搞乱你的系统。这很好，但有时你需要访问那些隐藏的文件。要查看它们，请在终端中键入以下命令:

```
defaults write com.apple.finder AppleShowAllFiles true  killall Dock
```

要再次隐藏这些文件，只需将`true`切换到`false`。

#### 启用 2D 码头

不喜欢那个 3D dock？很容易做成 2D(在小牛不起作用):

```
defaults write com.apple.dock no-glass -bool true
```

如果您想要回 3D dock，只需将`true`更改为`false`。

### 向 OS X 添加要素

OS X 总是有一些隐藏的功能，只能通过终端命令访问。有时候这些是你一直想要的特性，而其他时候大多数人不需要它们，它们有一点缺陷，或者是为开发人员准备的。

#### 启用单一应用程序模式

如果你经常分心，单一应用程序模式可以极大地帮助你保持专注。这使得你一次只能显示一个应用程序。它并不适合所有人，但当你需要专注于一个项目时，它真的很有帮助:

```
defaults write com.apple.dock single-app -bool true  killall Dock
```

要将其切换回正常状态，只需将`true`换成`false`。

#### 从快速查看中复制文本

快速浏览是 OS X 最好的特点之一。当你选择一个文件时，只需按空格键，你将看到该文件的预览，而不必打开应用程序。这很好，但是当你在预览的时候你不能选择任何文本。您可以使用终端命令添加该功能:

```
defaults write com.apple.finder QLEnableTextSelection -bool true  killall Finder
```

现在，只需打开快速查看，选择你想要的文本，然后复制。

#### 将弹出通知添加到 iTunes

想从应用程序的图标上获得 iTunes 中当前播放曲目的通知吗？这很简单:

```
defaults write com.apple.dock itunes-notifications -bool TRUE  killall Dock
```

如果您不是粉丝，禁用它也只需要一个简单的命令:

```
defaults delete com.apple.dock itunes-notifications
```

#### 启用调试模式

在苹果的许多应用程序中，调试模式以各种隐藏的功能存在。每个应用程序都有一点不同，但你通常可以获得一些在某种程度上有用的实验性功能。

**启用通讯录中的调试菜单:**

```
defaults write com.apple.addressbook ABShowDebugMenu -bool true
```

**在 iCal 中启用调试菜单(在 Mavericks 中不起作用)**:

```
defaults write com.apple.iCal IncludeDebugMenu -bool true
```

**启用磁盘工具中的调试菜单:**

```
defaults write com.apple.DiskUtility DUDebugMenuEnabled -bool true
```

和

```
defaults write com.apple.DiskUtility advanced-image-options -bool true
```

### 修复常见的 OS X 烦恼

OS X 的每个版本都有其令人烦恼的，但是 OS X 的许多最常见的问题都可以通过一两个终端命令来解决。

#### 禁用启动蜂鸣器

你的 Mac 喜欢在启动时发出响亮的声音，这意味着告诉你一切正常。对于大多数人来说，这种启动铃声没什么问题，但如果你在课堂上或其他需要让 Mac 保持安静的地方，这通常是个问题。要永久禁用声音，只需在终端中输入以下内容:

```
sudo nvram SystemAudioVolume=%80
```

现在，你的 Mac 会像忍者一样安静地开机。

#### 摆脱显示和隐藏 Dock 时的延迟

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-Cw4JlgcN3Og&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-Cw4JlgcN3Og&start=0) 

默认情况下，当鼠标悬停在 Dock 上并启用“自动隐藏和显示 Dock”时，Dock 会有轻微的延迟。这有点烦人，但是您可以使用以下命令自定义动画的速度:

```
defaults write com.apple.Dock autohide-delay -float 0 &&  killall Dock
```

现在，当你将鼠标悬停在 Dock 上时，它会立即出现。

#### 停止 Quicktime 和“预览”,以免自动恢复您打开的内容

自动恢复是一种方便的设置，可以在应用程序中打开上次使用的文件。这对大多数应用程序来说没问题，但它可能会在 Quicktime 或 Preview 等应用程序中导致一些尴尬的事情。幸运的是，逐个应用程序地禁用该功能很容易:

**进行预览**:

```
defaults write com.apple.Preview NSQuitAlwaysKeepsWindows -bool false
```

**对于 Quicktime** :

```
defaults write com.apple.QuickTimePlayerX NSQuitAlwaysKeepsWindows -bool false
```

#### 停用窗口动画来加快旧 Mac 的速度

OS X 的窗口动画很棒，但是它们会让老 Mac 的速度慢很多。如果你想让你的操作系统速度更快一点，只需禁用它们:

```
defaults write NSGlobalDomain NSAutomaticWindowAnimationsEnabled -bool false
```

#### 禁用通知中心

不喜欢新版 OS X 的通知中心吗？您可以使用终端命令禁用它，并将其从菜单栏中永久删除:

```
launchctl unload -w /System/Library/LaunchAgents/com.apple.notificationcenterui.plist killall NotificationCenter
```

这样，通知中心将关闭并消失，直到您重新启动。

### 其他很酷的技巧

你可以用终端做各种很酷的事情，这里有一些我们最喜欢的技巧，它们不属于其他类别。

#### 阻止您的 Mac 睡眠

您的电脑会进入睡眠状态，以便在您不使用它时不会浪费资源和电力，但有时您需要在执行某项任务时让它暂时保持清醒。为此，只需在终端中输入以下命令:

```
caffeinate -t 3600
```

那会让你清醒一个小时。3600 来自于一个小时的秒数，所以只要把这个数字改成你想让你的电脑保持清醒的时间就可以了。

#### 即时生成日历

需要一个快速日历？您可以使用以下命令在终端中立即显示一个:

```
cal 12 2013
```

只需将`12`更改为您想要的月份，将`2013`更改为您需要的年份。

#### 阻止帮助查看器在其他窗口上浮动

Mac Help Viewer 总是将自己放在最上面，当您试图进行故障诊断时，这非常烦人。不过这很容易禁用:

```
defaults write com.apple.helpviewer DevMode -bool true
```

当然，上面的列表并不代表一切。我们已经讨论过 [和终端](http://lifehacker.com/tag/terminal) 的许多其他功能，所以开始深入研究吧。如果你想用一个界面做更多的调整， [OnyX 是我们最喜欢的工具](https://lifehacker.com/the-best-system-tweaker-for-mac-5862462) 。