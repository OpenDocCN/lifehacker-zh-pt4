# 如何让 GIMP 工作起来更像 Photoshop

> 原文：<https://lifehacker.com/how-to-make-the-gimp-work-more-like-photoshop-1551318983>

六个月前，我停止使用 Adobe Photoshop，转而使用开源软件 GIMP 来完成我所有的个人摄影项目。这并不是大多数人认为的不可能完成的任务。

Watch

***本帖最初出现在*** [***莱利·勃兰特的摄影博客***](http://www.rileybrandt.com/2014/03/09/photoshop-to-gimp/) ***。**T15】*

用户经常声称 Photoshop 绝对是他们工作流程中必不可少的。在互联网上，论坛用户甚至因为建议某人尝试用 GIMP 代替 Photoshop 而遭到嘲笑。

但是时代变了。Photoshop 不再是过去的杀手级应用了。我大约 90%的时间在 Lightroom，只有 10%的时间在 Photoshop。其他很多专业人士也是如此。我们都切换到 RAW 格式，所以我们大多数时候使用 RAW 照片编辑器。Photoshop 经常只是用来做最后的润色。

对于 Photoshop 现在在很多摄影师工作流程中扮演 的 [缩减角色来说，](https://lifehacker.com/five-best-photoshop-alternatives-1483312519) [GIMP 却出奇的能干](http://lifehacker.com/top-10-photoshop-tricks-you-can-use-without-buying-phot-5864755) 。然而，过渡到 GIMP 可能会令人沮丧，因为键盘快捷键、工具和界面与 Photoshop 的不同。希望这些设置技巧能让 Photoshop 用户在 GIMP 中感觉更自在。

### 首先:找到你的 GIMP 文件夹

在本教程中，我们将调整 GIMP 的设置文件夹中的一些配置文件。这是在每个系统的不同位置。因此，请记下该文件夹的位置，并在以后的步骤中记住它:

**Windows**:C:\ Users \[您的用户名]\。gimp-2.8

**Mac OS X**:~/Library/Application Support/GIMP/2.8/(你可能要先 [取消隐藏库文件夹](http://bit.ly/1dr59Ln) )

**Linux** : ~/。gimp-2.8

从现在开始，我们称之为.../.gimp-2.8，你用上面的路径替换就可以了。现在让我们开始吧！

### 在 GIMP 中设置 Photoshop 键盘快捷键

只需替换一个配置文件，你就可以在 GIMP 中启用 Photoshop 的 [键盘快捷键](https://lifehacker.com/learn-photoshop-and-illustrator-shortcuts-with-these-ch-1079957831) 。到目前为止，这是我做的最有帮助的事情，让我更容易过渡到 GIMP。事实上，没有它我在 GIMP 中几乎毫无用处。

由于 GIMP 和 Photoshop 并不完全相同，所以有一些不同之处。您可以在 处查看所有键盘快捷键 [的列表。](http://epierce.freeshell.org/gimp/gimp_ps.php)

1.  从下载 ps-menurc 文件
2.  在瘸子的...\.gimp-2.8 文件夹中，将文件“menurc”重命名为“menurc-backup”
3.  将下载的 ps-menurc 文件重命名为“menurc”(没有。txt 扩展名)并将其移动到...\.gimp-2.8
4.  重新启动 GIMP 以使更改生效

**注意**:安装配置文件后，你可能会有几个快捷键相互冲突，所以我建议去编辑>键盘快捷键，确保 [一切都符合这张图](http://epierce.freeshell.org/gimp/gimp_ps.php) 。我还建议绑定“[”来进一步减小笔刷大小，绑定“]”来进一步增加笔刷大小以加快笔刷大小的变化。

### 安装“当前选择的图层”替换

在 Photoshop 中，CTRL+J 不仅可以用于复制当前图层，还可以从当前选区创建一个新图层。这是我在 Photoshop 中经常使用的一个非常方便的工具。你可以通过复制/剪切将相同的功能添加到 GIMP 的图层菜单中。

1.  通过复制/剪切 下载插件 [图层](http://registry.gimp.org/node/26396)
2.  通过将 layer-via-copy-cut.py 文件拖动到.../.gimp-2.8/插件/(如果你在 Linux 上，确保文件是可执行的)
3.  在当前层处于活动状态时，进行选择
4.  在主菜单中，选择“图层”>“通过复制图层”
5.  您的选择将被复制到一个新的层

将“复制图层”功能与图层蒙版结合起来是在 GIMP 中创建合成图像的一个好方法。这两个工具也可以替代 Photoshop 中的修补工具，但效率较低。

### 将“吸附到画布边缘”设为默认设置

在 GIMP 中，我发现真正令人沮丧的是，在默认情况下，当我移动图层时，它们不会贴紧画布(或网格)的边缘。更糟糕的是，每次打开图像时，你都必须启用它。幸运的是，由于开源软件是如此可定制，这很容易改变。

1.  打开.../.带有文本编辑器的 gimp-2.8/giprc
2.  在底部，添加两行:

`(default-snap-to-canvas yes)`
T1】

*   保存并关闭

### 默认情况下禁用“显示层边界”

GIMP 中我一直不习惯的是围绕活动层的黄黑虚线。虽然它有时会有所帮助，但我更愿意默认禁用它。

1.  从主菜单中，导航至编辑>首选项>图像窗口>外观
2.  取消选中在正常模式和全屏模式下显示图层边界
3.  重新启动 GIMP 以使更改生效

你可以通过点击主菜单中的视图并选择显示图层边界来临时打开它。

### 让移动工具的功能像 Photoshop 的一样

默认情况下，GIMP 中的移动工具设置为选择一个层或向导。设置此选项后，它的行为有点像 Inkscape 或 Illustrator，因为您还可以移动不在当前图层上的东西(如背景)。如果你是一个长期的 Photoshop 用户，这是非常奇怪的。

要使它像 Photoshop 一样工作，您可以设定默认行为来移动活动层。

1.  为左侧面板中的工具箱选择移动工具
2.  在“工具选项”对话框中，选中“移动活动层”
3.  从主菜单导航至编辑>首选项>工具选项>立即保存工具选项
4.  重启 GIMP

### 安装“内容感知填充”替换

Photoshop CS5 中出现的有用的“内容感知填充”功能实际上起源于一个叫做“再合成器”的 GIMP 插件它可以让你选择你想从图像中删除的东西，按下一个键，它就消失得无影无踪了。

愈合选择插件(又名智能删除)是一个伟大的内容感知填充的替代品。要安装它，只需下载 [再合成器](http://registry.gimp.org/node/27986) 和 [治愈选择](http://registry.gimp.org/node/15118) 插件，并将所需文件拖到.../.gimo-2.8/插件。

如果你使用的是 Linux，你也可以通过运行 [Thorsten Stettin](https://plus.google.com/+ThorstenStettin) 的 PPA 来安装这些和许多其他有用的插件:

`sudo add-apt-repository ppa:otto-kesselgulasch/gimp`
`sudo apt-get update`
T2】

安装后，您可以进行选择，然后导航到过滤器>增强>修复选择。瞧啊。

### 安装 ICC 颜色配置文件

你可以在线下载高质量的免费 ICC 色彩描述文件(如 sRGB ),并在 GIMP 中使用。Windows、Mac 和 Linux 用户可以直接从 [国际色彩联盟](http://www.color.org/srgbprofiles.xalter) 获得 sRGB ICC 配置文件。如果你运行的是 Ubuntu，或者任何它的衍生版本，比如 Linux Mint 或者 elementary OS，你可以直接从软件仓库获得它们。只需在软件包管理器中搜索“icc 颜色配置文件”。它们将被复制到/usr/share/color/icc/。

对于在 Abode RGB 色彩空间(比 sRGB 色域更广)中拍摄的摄影师，您可以从 Adobe 的网站上 [下载](http://www.adobe.com/support/downloads/iccprofiles/iccprofiles_win.html) 色彩配置文件。该软件包还包括 CMYK 颜色配置文件。您需要同意 Adobe 的 EULA。我建议将文件复制到 Linux 上的/usr/share/color/icc/或 Windows 或 Mac 上的另一个安全文件夹中。

一旦您在磁盘上有了颜色配置文件，您需要让 GIMP 知道它们在哪里。从 GIMP 的主菜单中，进入编辑>首选项>色彩管理。确保操作模式设置为色彩管理显示，并在下面的下拉菜单中选择 RGB 和 CMYK ICC 文件。

当然，你的显示器已经被校色了吧？没有人会傻到在没有校准显示器的情况下尝试对照片进行色彩平衡...正确

### 安装 CMYK 转换插件

如果您想在 GIMP 中将图像从 RGB 色彩空间转换为 CMYK，您可以使用 [单独+](http://registry.gimp.org/node/471) 插件来完成。然而，有一些限制。 [Arch Linux wiki](https://wiki.archlinux.org/index.php/CMYK_support_in_The_GIMP) 有一篇关于局限性(以及如何对图像进行软校样)的精彩文章。分开+可以做几件事:

*   分离 RGB 图像
*   将 ICC 配置文件附加到单独的图像文件
*   从一个 RGB 配置文件转换到另一个
*   不褪色的颜色

你也可以从 GIMP 插件注册表中安装它，就像我们之前安装其他插件一样。如果你运行的是 Linux，并且安装了我之前提到的[【PPA】](http://www.webupd8.org/2013/06/install-gimp-286-in-ubuntu-ppa.html)中的“gimp-plugin-registry”包，你就已经有了。

要在 GIMP 中将图像转换为 CMYK:

1.  从主菜单中，导航至图像>分离>分离
2.  这将给你一个新的图像，看起来颠倒，有四个单独的层
3.  前往“图像”>“分离”>“导出”,将图像导出为. tiff 文件

根据我作为专业摄影师的经验，实际上是图形设计师和印刷商需要 CMYK 支持。无论是杂志、报纸，甚至是 [广告牌广告](http://www.rileybrandt.com/2014/03/05/billboard/) ，我从未遇到有人要求在 CMYK 色彩空间中拍照。事实上，他们总是要求照片在 RGB 颜色空间，然后他们自己进行转换。

### 自定义您的工作区

#### 启用单窗口模式

这似乎是一个显而易见的步骤，但是我遇到过几个 GIMP 用户，他们甚至不知道这是一个选项。当 Photoshop 用户将他们的工具、菜单、面板和工作区集中在一个窗口中时，他们会感觉更加自在。

从主菜单，只需导航到窗口>单一窗口模式。

#### 可对接的对话

要释放左侧面板上的大量空间，请将工具选项 dock 移动到右下面板。然后将你的左面板调整到更薄的尺寸。

如果你想让 GIMP 真正模仿 Photoshop，你可以把图层对话框移到右下角。就我个人而言，我越来越喜欢顶部的图层和底部的工具选项。

[从 Photoshop 切换到 GIMP:来自专业人士的提示](http://www.rileybrandt.com/2014/03/09/photoshop-to-gimp/) |莱利·勃兰特摄影

* * *

Riley Brandt 是卡尔加里大学的一名摄影师和 Linux 爱好者。T3】

<small>*想看看你在 Lifehacker 上的作品？邮箱*</small> [<small>*安迪*</small>](mailto:andy@lifehacker.com) <small>*。*T15】</small>