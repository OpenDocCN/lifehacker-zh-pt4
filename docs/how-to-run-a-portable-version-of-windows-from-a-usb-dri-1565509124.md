# 如何从 USB 驱动器运行 Windows 的便携版

> 原文：<https://lifehacker.com/how-to-run-a-portable-version-of-windows-from-a-usb-dri-1565509124>

曾经想要一个可以随身携带的 Windows 副本，可以在任何计算机上使用吗？这是可能的:下面是如何在 USB 硬盘上安装 Windows 8 的便携式版本，你可以带着它去任何地方。



Windows 8 的企业版有一个名为 Windows To Go 的功能，可以让你在“认证”的闪存驱动器上安装一个便携式版本的 Windows。不幸的是，我们大多数人都没有 Windows 8 的企业版，也没有经过认证的闪存驱动器。然而，有一个叫 WinToUSB 的工具可以做同样的事情，不管你用的是什么版本的 Windows。它是这样工作的。

(注意这和 [从 u 盘](http://lifehacker.com/how-to-create-a-windows-8-installation-dvd-or-usb-drive-505769939) 安装 Windows *不同，u 盘可以让你在没有光驱的电脑上安装 Windows。在这里，我们实际上是在 USB 驱动器上安装 Windows，这样我们就可以从您想要的任何计算机上的驱动器运行它，并随身携带它进行故障排除、远程工作等。如果你是 Mac 用户， [看看这篇文章](http://lifehacker.com/build-the-perfect-portable-powerful-mac-then-carry-i-5926945) 了解更多关于如何在 OS X 上这么做的信息。)*

### 您将需要什么(以及您将得到什么)

你只需要几样简单的东西就能让它工作。它们包括:

*   **Windows 安装盘或 ISO 镜像**。 [我们推荐使用 Windows 8](http://lifehacker.com/why-does-everyone-hate-windows-8-should-i-upgrade-5955229) 。Windows 8 将允许您在任何计算机上使用您的可移植安装，但 Windows 7 没有那么可移植，如果您在其他计算机上使用它，可能会有驱动程序或激活问题。(如果一定要用 Windows 7， [这个替代方法](http://www.intowindows.com/install-windows-7-on-usb/) 可能更可取)。
*   **一个 USB 驱动器**。与闪存驱动器相比，外置硬盘驱动器更受青睐，因为它的运行速度要快得多。USB 2.0 就足够了，但如果你有 USB 3.0 驱动器，我们建议使用它(尽管它只在你安装 Windows 8 而不是 Windows 7 时才有效)。
*   [](http://www.easyuefi.com/wintousb/)**。这是一个简单的程序，将引导您完成安装过程。**

**如你所见，有一些警告。我们在 USB 2.0 外置硬盘上使用 Windows 8.1 对此进行了测试，结果相当令人满意。它以合理的速度运行，自动安装所需的驱动程序，并在多台计算机上工作。但如果你尝试使用 Windows 7 或闪存盘，你的里程数可能会有所不同。**

### **第一步:安装 WinToUSB**

**首先，下载 [WinToUSB](http://www.easyuefi.com/wintousb/) 并安装在你的系统上，就像你安装其他程序一样。请注意，您需要成为安装 WinToUSB 的计算机的管理员。**

**当你这样做的时候，找到你的 Windows 安装盘或 ISO 并准备好，因为你将在下一步需要它。如果你没有，你可以从微软 T3[下载一个。](http://lifehacker.com/how-to-create-a-windows-8-installation-dvd-or-usb-drive-505769939)**

### **第二步:创建你的移动硬盘**

**接下来，您只需要启动 WinToUSB 并按照它的(简短的)向导来创建您的可移植安装。只需要几个步骤:**

#### **1.选择您的安装介质**

**启动 WinToUSB 时，会提示您选择 ISO 文件或光盘。单击浏览按钮找到它，选择要安装的操作系统，然后单击下一步。**

#### **2.选择您的硬盘**

**接下来，您将被要求选择您的硬盘驱动器，并选择系统和引导分区。你可以在这里 找到更多关于这个 [的信息，但是有了 USB 硬盘你应该只能选择第一个分区作为系统，第二个分区作为引导，如上图所示。确保您的驱动器被格式化为 NTFS。](http://www.easyuefi.com/wintousb/faq/en_US/What-are-system-partitions-and-boot-partitions.html)**

#### **3.开始安装**

**当您单击“下一步”时，安装将开始。我发现它只花了半个小时左右，虽然你的里程可能会有所不同，取决于你的硬盘速度。**

### **第三步:从你的移动硬盘启动**

**就是这样！这实际上是一个非常快速和简单的过程，当它完成后，您可以开始在任何您想要的计算机上运行您的便携式安装。为此，只需插上电源，重启电脑，然后从驱动器 启动 [，就像你启动 CD 或闪存驱动器一样(在我的电脑上，这意味着在启动时按 F11 键，并从列表中选择驱动器)。](http://lifehacker.com/how-to-boot-from-a-usb-drive-or-cd-on-any-computer-5991848)**

**第一次启动时，它会安装必要的驱动程序并需要一段时间来引导，之后您可以像设置新的 Windows 8 PC 一样设置您的机器。您可能需要手动调整一些东西，如屏幕分辨率，但一旦完成，您可以关闭它，将其移动到另一台电脑，并从那里运行它。它可能会在每台新电脑上经历驱动程序安装步骤(这意味着需要一段时间来启动)，但我发现它在我的两台电脑之间移动得相当好。尽情享受吧！**

**<small>*标题图片由*</small>[<small>*grebcha*</small>](http://www.shutterstock.com/pic-128453198/stock-photo-portable-hard-drive-and-laptop-computer.html)<small>*(Shutterstock)。*T15】</small>**