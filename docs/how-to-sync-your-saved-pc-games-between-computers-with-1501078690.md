# 如何使用 Dropbox 在电脑之间同步您保存的电脑游戏

> 原文：<https://lifehacker.com/how-to-sync-your-saved-pc-games-between-computers-with-1501078690>

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-FPD5tCOQGDI&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-FPD5tCOQGDI&start=0) 

如果你可以在一台电脑上开始玩游戏，保存它，然后在另一台电脑上继续玩，那不是很好吗？以下是如何将你所有的游戏保存与 Dropbox 同步。

Watch

### 为什么不用蒸汽云呢？

Steam 确实有这样一个内置的特性，叫做 Steam Cloud。遗憾的是，Steam Cloud 并不支持 Steam store 上的所有游戏——只是部分游戏。而且，即使对于那些它确实支持(或看起来支持)的，它 [也不总是起作用](http://steamcommunity.com/app/43160/discussions/0/810924774434777419/) 。因此，当 Steam Cloud 不是一个选项时，Dropbox 是下一个最好的解决方案:它很可靠，很容易设置，而且工作很好。

### 如何与 Dropbox(或任何其他云服务)同步游戏保存

当游戏加载你的保存时，它会在默认位置查找，通常是在我的文档中的某个地方。我们将把这些保存文件复制到 Dropbox，然后创建一个从原始保存文件夹指向 Dropbox 的符号链接。这样，当你的游戏寻找保存时，它会被重定向到 Dropbox 中的同步保存。

#### 第一步:找到你的游戏保存

第一步很简单:找出你的游戏保存文件的地方。每个游戏都不一样，但大多数游戏都将这些数据存储在我的文档中(或者在我的文档文件夹中，或者在其中的“我的游戏”文件中)。如果你不确定，谷歌一下你的游戏，看看它的保存文件在哪里。

#### 第二步:将你保存的文件夹转移到 Dropbox

假设我们想为黑暗势力移动我们的保存，它位于 C:\ Users \ whit son \ Documents \ My Games \ dark siders。在你的 Dropbox 中创建一个保存游戏的文件夹，并将“黑暗势力”文件夹复制到其中。你应该会看到它很快与 Dropbox 同步，这意味着你的保存现在可以在你所有的电脑上使用。

#### 第三步:在你所有的电脑上创建符号链接

接下来，我们需要将每台计算机指向 Dropbox 进行保存。重命名或删除游戏的原始保存文件夹(现在它在 Dropbox 中),以管理员身份打开命令提示符并运行以下命令:

```
mklink /D "C:\Users\Whitson\Documents\My Games\Darksiders" "C:\Users\Whitson\Dropbox\Game Saves\Darksiders"
```

将第一个文件路径替换为游戏原始保存文件夹的路径，将第二个文件路径替换为新的 Dropbox 保存文件夹的路径。

按 enter 键，它应该会为您创建符号链接。要仔细检查，回到原来的保存文件夹，你应该看到一个新位置的快捷方式。查看本文顶部的视频，了解这一步骤的实际操作。

在你所有的电脑上重复这个过程，这样无论你在什么电脑上启动游戏，你的游戏都会被重定向到你的 Dropbox 文件夹中的文件。

注意:Mac 和 Linux 用户也可以这样做，只是需要一些稍微不同的命令——查看 [这篇文章](https://lifehacker.com/sync-files-and-folders-outside-your-my-dropbox-folder-5154698) 了解更多信息。

#### 第四步:游戏开始

完成后，测试一下！在一台计算机上启动游戏，将游戏保存在随机位置，然后尝试在计算机 2 上启动该游戏。运气好的话，你应该能够从计算机 1 中加载你最近保存的文件！

<small>*视频音乐由*</small> [<small>*埃里克·斯基夫*</small>](http://freemusicarchive.org/music/Eric_Skiff/Resistor_Anthems/eric_skiff_-_04_-_all_of_us) <small>*。标题图片混录自*</small>[<small>*vectorlib.com*</small>](http://www.shutterstock.com/pic.mhtml?id=112433756)<small>*。*</small>