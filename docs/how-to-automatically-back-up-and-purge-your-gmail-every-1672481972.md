# 如何每 30 天自动备份和清除您的 Gmail

> 原文：<https://lifehacker.com/how-to-automatically-back-up-and-purge-your-gmail-every-1672481972>

如果说索尼黑客 [教会了我们什么](http://sonyhack.gawker.com/) 的话，那就是把指控邮件放在收件箱里是个糟糕的主意。即使你没有做什么特别糟糕的事情，如果有人进入你的邮箱，你所说的一切都可能被公之于众。以下是如何确保不会发生这种情况，方法是按照计划自动备份和删除 Gmail 帐户中的所有内容。

Watch

### 如何自动清除 30 天的旧邮件

如果你想经常清理你的 Gmail，你需要一个 [谷歌脚本](http://www.google.com/script/start/) 。我们的 [将使用数字灵感中的这张](http://www.labnol.org/internet/gmail-auto-purge/27605/) 。很多电子邮件客户端都可以做到这一点，但我们将重点放在 Gmail 上。如果你愿意，这里有关于 [Outlook](http://www.howto-outlook.com/downloads/backupscript.htm) 和 [雷鸟](http://www.howtogeek.com/howto/44791/how-to-backup-your-web-based-email-account-using-thunderbird/) 的指南。谷歌应用程序的所有者也可以仅仅 [改变电子邮件的保留期限](https://support.google.com/a/answer/151128?hl=en) 。也就是说，下面是如何在普通的旧免费 Gmail 帐户上设置它:

1.  [点击此处复制谷歌自动清除脚本的](https://script.google.com/d/1PF1irj2h7nIKvpFF6MpihNP9_-CBaUJvFSNd3E_xxWk8_jgvhvYP38qD/edit?newcopy=true)
2.  该脚本删除基于标签的电子邮件，所以你需要在这里输入你想要的标签。对于总括来说，使用“收件箱”作为`var GMAIL_LABEL = " ";`行。不幸的是，您需要对每个标签都这样做，但这也会提取您已存档的邮件。
3.  在`var PURGE_AFTER = "1";`下输入您希望安排清除的天数，我们选择了 30 天。任何超过 30 天的邮件都会被发送到垃圾箱
4.  单击运行>初始化，并按照提示添加权限
5.  单击运行>安装以安装脚本。

现在，您的 Gmail 帐户将清除所有超过 30 天的邮件。如果你的 Gmail 账户塞满了电子邮件，你可能想先手动检查并删除所有邮件。值得注意的是，这会将你的邮件移到 Gmail 的垃圾邮件中，这需要多 30 *天*才能完全删除。如果你担心这一点，设置一个提醒，弹出到你的垃圾桶，手动删除一切。

### 如何按计划备份和加密您的 Gmail 帐户

删除你的邮件很容易，但是一旦它消失了，你就不能再搜索旧邮件了。太糟糕了。所以，你可以考虑对你的电子邮件做一个加密的本地备份。这样，你可以在需要的时候进行搜索，但你的电子邮件不会存储在任何人的服务器上，这对黑客来说都是很容易的。

对此你有 [很多选项(包括一些如果你没有使用 Gmail 的选项)](https://lifehacker.com/how-can-i-save-all-my-emails-for-a-personal-backup-5990556) ，但是我们将使用开源软件 [GMVault](http://gmvault.org/) 下载 Gmail 账户的备份。

1.  为您的操作系统 下载并安装 [GMVault](http://gmvault.org/download.html)
2.  打开应用程序，你会得到一个命令行界面
3.  回到 GMVault，输入`gmvault sync -e account@gmail.com`用你的电子邮件地址代替 account@gmail.com
4.  您将被要求登录并允许 GMVault 在您的默认浏览器中访问您的帐户。单击“允许访问”
5.  回到 GMVault 并按回车键。它会备份你所有的邮件并加密(你的加密密钥保存在你硬盘的`/users/name/gmvault-db/.info/.storage_key.sec`下)。这需要一段时间，所以让它做它的事情。

这是您的第一次备份，可能需要一段时间才能完成。恢复您的电子邮件取决于您希望如何查看它们。 [GMVault 有各种恢复选项](http://gmvault.org/in_depth.html#restore) 的指南，具体看你什么时候需要。一旦 GMVault 备份完成，你需要建立一个系统来每周备份一次你的邮件。如何操作取决于您使用的是 Windows 还是 OS X。

如果你没有使用 Gmail，你可以使用任何桌面邮件客户端来备份你的邮件。以下是一些更受欢迎的应用程序的指南:

*   [展望](https://support.office.com/en-sg/article/Back-up-Outlook-data-with-the-Microsoft-Outlook-Personal-Folders-Backup-tool-7ef27bac-6088-4f03-a9f7-34165d885883)
*   [雷鸟](http://www.howtogeek.com/howto/44791/how-to-backup-your-web-based-email-account-using-thunderbird/)T3】
*   [苹果邮箱](http://support.apple.com/kb/PH14884)
*   [航空邮件](http://www.manula.com/manuals/airmail/airmail-manual-1-3/1.3/en/topic/exporting)
*   [邮箱](http://support.postbox-inc.com/hc/en-us/sections/200422230-Importing-Exporting-Email-Messages)

当你备份完你的邮件后，如果你愿意，你可以继续 [在本地](https://lifehacker.com/a-beginners-guide-to-encryption-what-it-is-and-how-to-1508196946) 加密这些文件。

#### 如何在 Windows 上自动化备份

GMVault 具有同步功能，可以查看您当前的备份，并且只备份新邮件。它只能回顾一周，所以你需要每周运行一次备份。在 Windows 上，您可以使用任务计划程序来完成此操作:

1.  在 Windows 中打开任务计划程序(控制面板>系统和安全>管理工具)
2.  单击创建基本任务
3.  为任务命名，并将触发器设置为每周(如果您想更加安全，可以每天进行)
4.  点击 Action 选项卡，选择 Start a Program，然后选择 gmvault.bat 文件，默认应该在这里:`C:\Users\NAME\AppData\Local\gmvault\gmvault.bat`
5.  选择添加参数并添加，用你的电子邮件代替 account@gmail.com`sync -e -t quick account@gmail.com`

就是这样。您可以在任务调度器中右键单击它，然后选择 Run 来测试它。

#### 如何在 Mac 上自动备份

在 OS X，使用 Automator 按计划运行 GMVault:

1.  打开 Automator(“应用程序”>“实用工具”)并创建一个新文稿
2.  选择“日历提醒”
3.  添加运行 Shell 脚本操作
4.  在文本框中，键入`gmvault sync -e -t quick youraccount@gmail.com`，用您的信息替换 youraccount@gmail.com。根据 Gmvault 的安装位置，您可能还需要包含该目录
5.  保存文件
6.  保存后，它会自动打开带有新事件的日历。将日历事件设定为每周重复一次

Automator 将每周运行一次 GMvault 来备份您的电子邮件。

就这样，你现在可以按照设定的时间表备份和删除你的电子邮件，这样你就不用太担心黑客攻击了。