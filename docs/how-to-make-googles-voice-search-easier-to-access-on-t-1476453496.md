# 如何让谷歌的语音搜索在桌面上更容易使用

> 原文：<https://lifehacker.com/how-to-make-googles-voice-search-easier-to-access-on-t-1476453496>

谷歌桌面上的语音命令几乎和安卓 上的 [一样令人敬畏。虽然它不能做手机能做的一切，但](https://lifehacker.com/everything-you-didnt-know-you-could-do-with-google-voi-512727229) [对话式搜索](http://lifehacker.com/googles-new-conversational-search-makes-star-trek-styl-506833940) 使用 [大部分相同的命令](https://support.google.com/chrome/answer/1331723?hl=en) ，甚至可以在 Google Now 中设置定时器或提醒。只是有时候有点难以触及。



有点讽刺的是，在你自己家里的私人空间里对着你的桌面说话 [而不显得像个混蛋](https://lifehacker.com/how-can-i-talk-to-my-phone-in-public-without-looking-li-5883564) 更容易，但是实际上要做到这一点有点困难。首先你要打开 Chrome，然后导航到谷歌的网络搜索(谁不用 omnibar？)，然后点按麦克风按钮。大声说出你可以在地址栏中输入的内容有点麻烦。一定有更好的方法，对吗？

### 获取 Ok，Google 扩展

正如我们上周报道的，谷歌发布了 Chrome 网络商店的扩展，允许你像在安卓上一样使用“Ok，Google”命令。这个命令在 Google 的网络搜索和新标签页上都有效。

有几个警告。首先，如果你真的在看一个启用了语音识别的标签，Chrome 只会监听“Ok，Google”命令。它还会在五分钟后停止监听，以延长笔记本电脑的电池寿命(尽管这似乎也发生在台式机上)。换句话说，你不能让一个 Google.com 标签一直开着，然后期待它对你洪亮的声音发出的每一个命令做出反应。不过，我们可以让它变得简单一点。

### 使用自动热键创建键盘快捷键

如果你用的是 Chrome，拉起一个语音搜索框并不太难(除非你用的是备用的新标签页)。然而，在 Windows 的其他地方，你必须经历重重困难才能到达那里。一种解决方法是创建一个自定义的 AutoHotkey 脚本来启动 Google 搜索页面。

在可能是最简单的自动热键脚本中，将以下内容添加到您的脚本列表中:

```
Capslock::Run www.google.com
```

虽然 [Capslock 是重新利用](https://lifehacker.com/how-to-make-your-caps-lock-key-search-the-web-chrome-o-5751343) 的一个很棒的键，但是你可以用你选择的任何快捷键替换 Capslock。如果你需要一本关于如何在 AutoHotkey 中表示键盘快捷键的入门书，你可以查阅 [官方文档](http://www.autohotkey.com/docs/) 或者我们自己的指南 [创建 AutoHotkey 快捷键](http://lifehacker.com/turn-any-action-into-a-keyboard-shortcut-a-beginners-g-316589) 。一旦完成，你就可以在操作系统的任何地方按下这个键来调出谷歌，如果你已经安装了 [OK，谷歌扩展](https://chrome.google.com/webstore/detail/google-voice-search-hotwo/bepbmhgboaologfdajaanbcjmnhjmhfn)——只要开始与谷歌对话，你就上路了！

### 用 Windows 语音命令增强它

我知道你在说什么:“按键显然是给那些不知道如何不用手指的傻瓜准备的。”如果你想仅仅通过声音进行更多的控制，你可以使用微软自己的内置在 Windows 中的语音识别软件。

正如我们之前所报道的，微软的语音识别 [非常强大](https://lifehacker.com/control-your-pc-with-your-voice-391884) ，它可以在大多数版本的 Windows 上使用。虽然一起使用起来不太直观，但你可以用微软的方法轻松打开谷歌自己的语音搜索。例如，如果你创建了上面的 AutoHotkey 脚本，你可以说“按 Capslock”打开 Google.com，然后在那里说“Ok，Google”开始运行。你可能需要指示 Windows 的语音搜索“停止监听”，以确保你 [不会越过溪流](http://www.youtube.com/watch?v=jyaLZHiJJnE) 。这并不完全优雅，但它确实可以让你不用触摸键盘就能调出谷歌。

不幸的是，尽管这项技术很好，但我们还没有达到一个普遍可用的、完全语音控制的计算机 24/7 的地步。然而，通过一点小技巧(也许还有几个稍微有点笨拙的命令)，您就可以非常接近了。