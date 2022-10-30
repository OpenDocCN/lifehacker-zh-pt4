# 如何将 Windows 更新整合到安装光盘中

> 原文:[https://life hacker . com/how-to-slipsstream-windows-updates-into-your-installation-1562956432](https://lifehacker.com/how-to-slipstream-windows-updates-into-your-installatio-1562956432)

重新安装 Windows 的一个可怕之处是，为了保证安全、稳定和最新，需要进行无休止的软件更新和重启。但是有一个更好的方法:滑流。只需做一点准备，您就可以创建一个包含所有更新的新安装光盘，这样就可以一次安装所有内容。

Watch

### 什么是滑流？

组合流是一种将软件更新与原始安装媒体相集成的方法。这意味着，如果你有一张 Windows 8.1 光盘，你可以将最新的更新“整合”到光盘中，这样这些更新就可以随 Windows 一起安装，而不是随后安装。这减少了您需要更新和重新启动系统的次数，如果您在多台电脑上安装 Windows 或者您的互联网连接速度较慢，这也很有用。

微软自己的命令行组合工具在 Windows XP 上使用起来非常简单，但在 Windows Vista 上，这个过程发生了变化，变得更加繁琐。幸运的是，第三方实用程序使滑流变得不那么复杂，并提供了额外的功能。

### 我为什么要滑流？

Slipstreaming 最初是为企业设计的，目的是让 it 人员更快更容易地保持多个系统的最新状态，但它对经常重新安装 Windows 的最终用户同样有用。它将所有单调的更新和重启减到最少，如果你使用第三方工具，你可以根据自己的喜好定制安装。例如，使用 WinReducer 8.1，您可以绕过 EULA 和语言屏幕来加快安装速度。你也可以删除内置程序，输入计算机名，设置鼠标灵敏度，等等。

听起来熟悉吗？我们之前已经讨论过这个问题，在我们的 [创建定制的 Windows 8 安装](http://lifehacker.com/how-to-create-custom-windows-8-install-and-refresh-disc-1433371693) 指南中。我们今天要讨论的是同一个工具，不过更侧重于该过程的滑流部分以及为什么要这样做——所以如果你是初学者，你应该不会对本指南有任何问题，并且可以跳过更高级的内容。Windows 7 用户可以 [查看本指南](http://lifehacker.com/customize-your-windows-installation-to-create-the-os-of-5894838) 寻找基于 Windows 7 的替代品。

### 如何整合 Windows 8.1 更新 1

在今天的例子中，我们将把最新的 Windows 8.1 更新整合到 Windows 8.1 安装盘中。该更新是免费的，可以通过 Windows Update 获得，但如果你想将该更新集成到你的 Windows 8.1 媒体中，这很容易做到。对于这个特殊的例子，您需要:

*   运行 Windows 8.1 的电脑
*   [WinReducer 8.1](http://www.winreducer.net/winreducer-81.html) 及其所需的第三方软件(见下图)
*   Windows 8.1 零售光盘或官方 ISO(升级光盘和 ISO 不工作)
*   一个 8GB 的 USB 闪存驱动器来创建安装程序

下载 WinReducer 8.1 后，您还需要下载一些它需要的第三方实用程序，包括:

*   [7-Zip](http://www.7-zip.org) :这是值得拥有的，因为它是我们最喜欢的文件存档工具
*   ImageX 和 Oscdimg:这些工具通常包含在 [Windows 自动安装工具包(AIK)](http://www.microsoft.com/en-us/download/details.aspx?id=5753) 中，但是 [GetWaikTools](http://www.msfn.org/board/topic/156869-get-waik-tools-wo-downloading-the-huge-isos/) 允许您下载它们，而不必下载大的 ISO。在 Waik 工具下载屏幕上选择“Waik tools for Windows 8.1”。
*   [资源黑客](http://www.angusj.com/resourcehacker/)
*   :下载 EXE 版本，*不是*DLL 版本

当你准备好了，继续下面的步骤，开始滑流！

#### 步骤 1:在 WinReducer 8.1 中设置第三方程序

第一次启动 WinReducer 时，您会看到一个配置屏幕。软件检测部分列出了它需要的五个第三方软件程序。将下载的程序(7z.dll、7z.exe、imagex.exe、oscdimg.exe、ResHacker.exe 和 SetACL.exe)中的可执行文件和 7-Zip DLL 复制到 WinReducer81\HOME\SOFTWARE 文件夹中。复制完程序后，将配置屏幕上的开关从“关”滑动到“开”一旦所有开关都“打开”，关闭配置屏幕以启动 WinReducer。

#### 步骤 2:挂载您的 Windows 8.1 文件

点击 WinReducer 中的开始按钮，然后选择 Windows 8.1 文件所在的位置。如果您使用的是零售光盘，请将其内容拷贝到电脑上的一个文件夹中，然后点按 WinReducer 中的“文件夹”按钮浏览到该文件夹。如果您使用的是 Windows 8.1 ISO，请单击 ISO 按钮并导航到您的 ISO 文件，然后将 Windows 8.1 挂载到 WinReducer。

#### 步骤 3:下载 Windows Update 1 文件

Windows 8.1 挂载到 WinReducer 后，你会看到几个配置部分。转到系统部分，然后单击 WinReducer 更新工具按钮。为 32 位 Windows 选择 x86 或为 64 位 Windows 选择 x64，然后单击更新按钮。选中“Updates (Update 1) (6)”旁边的框以及您想要包含在新 ISO 中的任何其他更新，然后单击“下载”按钮。下载完成后，退出更新工具，然后在更新框中输入更新的路径:winreducer 81 \ WORK \ INTEGRATE \ Updates \ x64(适用于 64 位 Windows)。

#### 步骤 4:应用其他定制(可选)

如果您想进行任何其他定制，现在就开始吧(同样，请参见我们更高级的指南】，否则您可以跳过这一步)。

#### 步骤 5:应用更新并创建新的 ISO

设置完毕后，单击完成，然后单击应用。这一步可能需要相当长的时间，所以你可能想起来伸展一下，喝杯饮料，然后再回来。

当 ISO 文件创建器窗口最终出现时，选择将文件保存为 ISO，然后单击保存。几分钟后，您的定制 ISO 就完成了。此时，您可以通过右键单击 ISO 并选择“刻录光盘映像”将它刻录到光盘上你也可以用它来 [创建一个可引导的 u 盘](http://www.eightforums.com/tutorials/2227-create-bootable-usb-dvd-windows-8-iso.html) ，或者保存 ISO 以备将来使用。

就是这样！现在，您有了一张包含所有最新更新的 Windows 安装光盘，使以后的安装更加容易和快捷。把它放在安全的地方，好好享受吧！