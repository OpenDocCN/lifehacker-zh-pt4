# 如何为 Android 上的任何东西创建自定义的 Google Now 命令

> 原文:[https://life hacker . com/how-to-create-custom-voice-commands-with-tasker-and-aut-1282209195](https://lifehacker.com/how-to-create-custom-voice-commands-with-tasker-and-aut-1282209195)

谷歌现在已经在 中内置了大量 [有用的语音命令。不过，多亏了 Tasker 插件 AutoVoice](https://lifehacker.com/everything-you-didnt-know-you-could-do-with-google-voi-512727229) 最近的 [更新，你现在可以创建自己的命令，直接插入 Google Now 来完成 Tasker 只用你的声音就能完成的任何事情。](http://lifehacker.com/preview/autovoice-now-lets-you-create-custom-google-now-command-1607156863)

Watch

在本指南中，我们将主要使用 Tasker 和 AutoVoice，重点是新的 UI[。如果你还没有这两个应用程序，它们当然值得你花几个钱去买。你不需要被告知这些。](https://lifehacker.com/taskers-new-user-friendly-ui-makes-automating-your-andr-5992802) [大伙儿都爱 Tasker](http://lifehacker.com/show-us-your-best-tasker-actions-487360630) 。那么，我们开始吧。

### (可选)第 0 步:获得 Ok，谷歌(如果你还没有)

谷歌最近推出的最酷的功能之一是无需最少的非语音输入就能启动语音命令。如果你使用的是 Moto X 这样的手机，你已经可以说“好的，Google Now”来启动语音命令了。如果你不是，这里有一些方法可以让你得到它:

*   **使用 Google Now 启动器(在某些设备上):**Nexus 5 问世时的一个显著特点是，你可以在锁定屏幕上说“好的，谷歌”。这已经扩展到其他几个设备，尽管还不清楚支持多少设备。让事情变得更复杂的是，谷歌增加了 [一个“好的，谷歌”无处不在选项](http://www.androidpolice.com/2014/06/25/apk-download-google-search-v3-5-14-brings-ok-google-hotword-detection-to-any-screen/) ，让你即使不在主屏幕上也能启动语音命令。这也只在有限数量的设备上得到支持，目前还不清楚推广是如何进行的。尽管如此，如果你是幸运的，这是一个很好的选择。
*   **使用 Apex 这样的替代启动器:**不满足于等待 Google 的推出，Apex 这样的一些开发者已经添加了 [他们自己的“Ok，Google”热门词检测](http://www.androidpolice.com/2014/06/25/apex-launcher-adds-ok-google-hotword-detection-and-dynamic-icon-support-for-today-calendar-in-version-2-4/) 。这允许你从主屏幕上启动语音命令，即使你没有使用谷歌的软件。
*   **使用类似 Open Mic+的第三方始终监听 app:**如果你真的想要 Moto X 风格的全方位操控， [Open Mic+可以帮助](http://lifehacker.com/open-mic-brings-the-moto-xs-touchless-control-to-any-1211465747) 。无论你在应用程序的哪个位置，这个应用程序都会让你的麦克风开着，听“好的，谷歌”。这样做的缺点是会耗尽你的电池，但对一些人来说，好处可能会超过成本。

显然，这些都不是适用于所有设备的完美解决方案。我们离能够在任何情况下在任何设备上完全不用手来启动所有语音命令还有一段距离。然而，对大多数人来说，至少有几个选择。

这一步也是完全可选的。大多数设备在默认的谷歌搜索栏中都有一个语音按钮，你可以点击它并发出语音命令。即使你不能在不触摸设备的情况下触发语音搜索，在大多数主屏幕上只需轻轻一点就可以开始。

### 步骤 1:允许 AutoVoice 监听 Google Now 命令

 [https://lifehacker.com/embed/inset/iframe?id=youtube-video-TToDlfHlDzM&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-TToDlfHlDzM&start=0) 

AutoVoice 通过监听特定搜索来“集成”Google Now。就像谷歌的内置命令一样，如果一个特定的搜索与你设置的 Tasker 个人资料相匹配，AutoVoice 将拦截该搜索并运行你的自定义命令。如果 AutoVoice 和谷歌都不认为它是一个指令，它将进行常规搜索。

但是，在此之前，您需要启用 AutoVoice 辅助功能服务。为此，首先安装 [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm) 和 [AutoVoice](https://play.google.com/store/apps/details?id=com.joaomgcd.autovoice) (如果你还没有的话)并执行以下操作:

1.  打开手机的设置应用程序。
2.  轻按“辅助功能”
3.  轻按“AutoVoice Google Now 集成”
4.  点击屏幕顶部的开关。
5.  在弹出的对话框中，点击“确定”

此服务可能位于“设置”应用程序中的不同位置，具体取决于您的设备。启用监听服务后，您可以开始创建自己的自定义语音命令。

### 步骤 2:创建一个自定义的 Google Now 语音触发器

有了新的 Google Now 集成，创建自定义 AutoVoice 命令的过程大大简化了。AutoVoice 单独识别命令，并通过 AutoVoice 识别事件将命令传递给 Tasker。然后，您可以将任何操作附加到该事件。要创建自定义语音命令，请按照下列步骤操作:

1.  打开 Tasker。
2.  点击屏幕底部的加号。
3.  选择事件。
4.  在“插件”下，选取“自动语音识别”
5.  轻按“配置”旁边的编辑按钮
6.  轻按“命令过滤器”以键入您想要触发事件的语音命令，或者轻按“朗读过滤器”以大声朗读。后者有助于确保谷歌能够正确识别，所以我们建议首先这么做。
7.  点击屏幕顶部的复选标记。
8.  点击屏幕左上角的左插入符号保存事件。

这将创建一个自定义语音事件，当您在 Google Now 中大声说出时，该事件将被识别。下一步将是创建一个任务，当 Google Now/AutoVoice 识别出您的命令时，该任务将被激活。在这一点上，天空是极限。

### 第三步:将你的命令与 Tasker 的巨大力量联系起来

在这里，系统会提示您创建一个新任务或从现有任务中进行选择。在这一点上，一个充满可能性的世界向您敞开了大门，这超出了本文(或整个网站)的范围。然而，这里有一些例子让你开始。

向联系人发送预设短信。

1.  在“任务”下创建新任务。
2.  为您的任务命名(即文本名称)
3.  点击加号添加新操作。
4.  轻按“电话”
5.  选择“发送短信”
6.  输入电话号码和预设消息。
7.  可选:如果您想保留已发送消息的记录，请选中“存储在消息应用程序中”。
8.  点击左上角的后退按钮。

**在单个设置中更改多个设置。**

1.  在“任务”下创建新任务。
2.  命名它(即家庭设置)
3.  点击加号添加新操作。
4.  轻按“网络”并选择 WiFi。
5.  在“设置”下选择“打开”
6.  点击“网络”并选择“蓝牙”
7.  在“设置”下选择“关闭”
8.  点击“其他”并选择“GPS”
9.  在“设置”下选择“关闭”
10.  点击左上角的后退按钮。
11.  在中详述的 AutoVoice 配置文件设置下，确保如上所述取消选中“事件行为”。

这些都是非常基本的例子，但是 Tasker 的美妙之处在于它可以扩展到大量的任务。如前所述，你已经分享了许多 [你的 Tasker 动作](http://lifehacker.com/show-us-your-best-tasker-actions-487360630) ，如果你有一个家庭自动化系统，Tasker 和 AutoVoice 可以用来创建一组令人印象深刻的语音命令 [控制你的整个家庭娱乐系统](https://lifehacker.com/automate-your-home-via-voice-commands-with-tasker-and-v-493876426) 只需一点点工作。Tasker 可能令人望而生畏，但这至少应该有助于您开始使用语音命令。

*<small>照片混合自</small>*[*<small>Vivaporius</small>*](http://conworld.wikia.com/wiki/File:Thermal_Energy_Blast.jpg)*<small>。</small>T15】*