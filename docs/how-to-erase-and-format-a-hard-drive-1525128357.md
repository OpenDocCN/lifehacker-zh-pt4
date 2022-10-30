# 如何擦除和格式化硬盘

> 原文:[https://life hacker . com/how-to-erase-and-format-a-hard-drive-1525128357](https://lifehacker.com/how-to-erase-and-format-a-hard-drive-1525128357)

格式化硬盘是一个令人讨厌的项目从头开始的最佳方式。你肯定会想在卖掉你的机器之前做这件事，但这也是你在安装新的外置硬盘或打算在你的台式电脑中安装新硬盘时要采取的步骤之一。

Watch

删除驱动器上的所有内容并重新开始通常是一个简单的过程，但在开始之前，有几件事您需要知道。(谢天谢地，如果你搞砸了什么，你可以用你需要的任何正确的规格重新格式化你的驱动器。)

### 文件系统解释

当你第一次安装一个硬盘时，你必须用一个特定的文件系统来格式化它。不同的操作系统(Windows、macOS 和 Linux)使用不同的文件系统来组织和存储数据，因此您需要使用最适合您需求的文件系统。

*   [**NTFS**](http://en.wikipedia.org/wiki/Ntfs) :这是 Windows 默认的文件系统。Windows 可以读写 NTFS 格式的驱动器。macOS 和 Linux 只能读取 NTFS 格式的驱动器，而不能写入它们——除非你安装了 [第三方驱动](https://www.howtogeek.com/236055/how-to-write-to-ntfs-drives-on-a-mac/) 。
*   [**fat 32**](http://en.wikipedia.org/wiki/Fat32#FAT32)**:**fat 32 是一个比较老的文件系统。你不能在 FAT32 系统上安装新版本的 Windows，但是它的通用兼容性使它可以方便地用于外部驱动器。Windows、macOS 和 Linux 都可以毫无问题地读写 FAT32 驱动器。然而，FAT32 有一个主要的缺点:单个文件不能大于 4GB，这意味着它不适合像电影或光盘图像这样的大文件。
*   [**exFAT**](http://en.wikipedia.org/wiki/Exfat)**:**exFAT 类似于 FAT32 [没有缺点](http://lifehacker.com/use-the-exfat-file-system-and-never-format-your-externa-5927185) 。Windows 和 macOS 都可以读写 exFAT 格式的驱动器，并且您可以存储大于 4GB 的文件。尽可能使用 exFAT，而不是更陈旧的 FAT32。
*   [](https://en.wikipedia.org/wiki/Apple_File_System)****:**这是 macOS 目前默认的文件系统，截止到 High Sierra。当你使用固态硬盘时，它可以提供更好的性能和可靠性，但它不能与任何使用 OS X Sierra 或更旧系统的系统反向兼容。 [Paragon 软件](https://www.paragon-software.com/paragon-software-group-releases-free-paragon-apfs-sdk-community-edition-for-software-developers-oems-forensic-experts/) 有一个工具包，可以让 Windows 等操作系统读取 APFS 文件。注意:如果你想使用正在格式化的驱动器进行 Time Machine 备份，你需要 [选择旧的 Mac OS 扩展(日志)格式](https://support.apple.com/en-us/HT208496) 。**

**当你格式化硬盘时，它会删除硬盘上的所有内容。在某些情况下，在不丢失文件的情况下转换您的驱动器是可能的——例如将硬盘从 FAT32 转换为 NTFS——但在大多数情况下，改变您的文件系统的唯一方法是擦除驱动器并从头开始格式化。** 

### **如何格式化外部驱动器或闪存驱动器**

**即使你的新设备插上电源就能正常工作，但许多外置硬盘和闪存盘都附带了无用或不必要的额外软件。格式化它可以消除这些烦恼，并且额外给你一点额外的硬盘空间。**

#### **如何在 Windows 中格式化驱动器**

*   **将硬盘插入电脑，如有必要，插入墙上的电源插座。**
*   **打开文件资源管理器，在侧边栏中找到您的驱动器。**
*   **右键单击驱动器并选择格式化。**
*   **在文件系统下，选择要使用的文件系统。关于选择哪一个的更多细节，请参见上一节。**
*   **在卷标下给你的驱动器命名，并选中快速格式化框。**
*   **单击开始格式化驱动器。完成后，您会收到一个通知(应该只需要几秒钟)。**

**完成后，在 Windows 资源管理器中打开该驱动器，您可以开始将文件拖到其中或备份您的计算机。如果您在文件资源管理器中找不到您的驱动器，您可能需要打开“计算机管理”(通过“开始”菜单)，单击“磁盘管理”，右键单击您的驱动器的空间块以格式化它(并最终为它分配一个驱动器号，这样您就可以在文件资源管理器中看到它)。**

**请记住，格式化驱动器时，它不会显示与包装盒上完全相同的可用空间。一个原因是 [电脑测量空间的方式与](http://lifehacker.com/why-doesnt-my-new-hard-drive-show-the-right-amount-of-s-5950506) 不同，所以你永远不会得到完全相同的数字(至少在 Windows 上)。**

#### ****如何在 macOS 中格式化驱动器****

*   **打开 **Finder >应用>实用程序**(快捷键 Shift + Command + U)双击磁盘实用程序。**
*   **在左侧边栏中选择要重新格式化的驱动器，然后转到擦除选项卡。**
*   **在“格式”菜单下，选择要使用的文件系统。关于选择哪一个的更多细节，请参见上一节。**
*   **为您的驱动器命名，然后单击擦除按钮。格式化你的驱动器应该只需要几秒钟。**

**完成后，点击 Finder 中的驱动器。您可以开始将文件拖到它上面，或者使用 Time Machine 将它设置为备份驱动器。**

### **如何格式化计算机的主硬盘**

**如果你想清除你电脑的硬盘，也就是你经常使用的硬盘，事情就有点复杂了。你需要使用可引导 CD 或 USB 驱动器来格式化它。**

**例如，如果你是 Windows 用户，你可以简单地使用微软的媒体创建工具来创建安装媒体的 USB 或 DVD。然后，假装你正在重新安装 Windows 10，但格式化你的驱动器是这个过程的一部分。关掉电脑，不要安装任何东西，你就有一个空白的驱动器。就这么简单。在 macOS 上，你可以简单的用 [macOS 恢复](https://support.apple.com/en-us/HT201314) 到 [擦写你的驱动](https://support.apple.com/en-us/HT208496) 。**

**有很多其他的 [实时操作系统](https://gparted.org/livecd.php) 可以用来擦除你的主硬盘，但这两个例子是技术新手最简单的解决方案。**

***这篇文章最初发表于 2014 年，并于 2020 年 2 月更新了最新信息。***