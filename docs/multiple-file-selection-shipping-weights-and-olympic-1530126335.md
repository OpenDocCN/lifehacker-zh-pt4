# 多文件选择、运输重量和奥运奖牌

> 原文:[https://life hacker . com/multiple-file-selection-shipping-weights-and-Olympic-1530126335](https://lifehacker.com/multiple-file-selection-shipping-weights-and-olympic-1530126335)

读者提供了在 Windows 中选择多个文件、在发送包裹时计算运输重量以及查看谁获得了什么奥运奖牌的最佳技巧。

Watch

每天，我们的收件箱里都会收到大量优秀的读者建议，但由于各种原因——也许它们有点太小众，也许我们找不到一种好的方式来展示它，或者也许我们就是放不下——这些建议没有出现在头版。在小费箱里，我们收集了一些我们最喜欢的食物，供你自助消费。有你自己的建议要分享吗？添加到评论中，通过电子邮件发送到 lifehacker.com 的 tips，或者在我们的用户博客 [Hackerspace](http://hackerspace.lifehacker.com) 上分享。

### 使用此自动热键脚本在 Windows 中选择多个文件

Ganapathy 共享一个 [自动热键脚本](http://www.syncwithtech.org/2014/02/select-files-without-holding-ctrl.html) 用于在 Windows 中选择多个文件:

> 您可以在 Windows 中选择多个文件，方法是在单击文件时按住 CTRL 键，或者如果您打开了该功能，则选择文件复选框。但是如果你想用你的鼠标，我写了这个自动热键脚本。单击鼠标中键“打开”CTRL 键。像往常一样用鼠标左键选择您想要的文件，然后再次单击鼠标中键以松开 CTRL 键。
> 
> `#IfWinActive ahk_class CabinetWClass`

> `MButton:: KeyWait MButton, U`
> 
> `Send {Ctrl down}`
> 
> `KeyWait MButton, D`
> 
> `Send {Ctrl up}`
> 
> `^WheelUp:: Send {Up}`
> 
> `^WheelDown:: Send {Down}`

如果要打开文件的复选框，请打开 Windows 资源管理器。在 Windows 8 中，选择**视图**选项卡，并选中**项目复选框**复选框。在 Windows 7(或 Windows 8)中，选择**组织** > **文件夹选项** > **使用复选框选择项目**。

### 使用 Amazon 查找发送包裹的运输重量

诺亚分享了这个发送包裹的技巧:

> 很简单的提示，但它帮助了我。如果你需要快速估算一件商品的运输重量，而不需要实际装箱称重，可以在亚马逊上查找该商品，并在商品详情中查找运输重量。这可能不是最可靠的方法，但在我查找的三个项目(一个无线扬声器，一个棋盘游戏和一本书)中，亚马逊的运输重量是正确的。

### 用这个可视化扫描索契奥运会奖牌

Chris 分享 [本网站](http://www.bytemuse.com/post/sochi-winter-olympics-medals-by-country-sport/) 快速查看索契冬奥会获奖情况:

> 昨天，我创建了一个可视化的索契冬奥会奖牌国家和运动之间的地图。只需将鼠标放在比赛项目列表中，查看哪些国家获得了奖牌，或者放在国家列表中，查看他们在哪些项目中获得了奖牌。这是一个有趣的方式来看看谁赢得了什么，我想生活黑客的读者可能会喜欢它！

### 使用此交互式地图查找并分享绝佳的野餐地点

蒂莫西分享了一个 [网站](http://www.thepicnicworld.com/best-picnic-spots.php) 来寻找完美的野餐地点:

> 找到一个很棒的野餐地点是很困难的，尤其是如果你想稍微偏离一下常规的话。我在野餐世界找到了这张非常酷的互动野餐地图，上面有数百个用户提交的美国各地的地点。他们经常更新用户提交的内容，所以你总是可以找到一个新的地方去探索，或者分享一个你喜欢的地方。