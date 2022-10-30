# 如何使用亚马逊冰川作为一个非常便宜的备份解决方案

> 原文：<https://lifehacker.com/how-to-use-amazon-glacier-as-a-dirt-cheap-backup-solut-1460814873>

不久前，亚马逊 [推出了 Glacier](https://lifehacker.com/amazon-glacier-archives-your-important-data-for-a-penny-5936556) ，这是一种在线存储/存档解决方案，每月每 GB 的起价仅为 1 美分。根据您的存储需求，Amazon Glacier 可能是终身备份数据的最经济高效的方式。以下是您需要了解的内容以及设置方法。

Watch

### 亚马逊冰川是如何工作的

[亚马逊冰川](http://aws.amazon.com/glacier/?asc_campaign=InlineText&asc_refurl=https://lifehacker.com/how-to-use-amazon-glacier-as-a-dirt-cheap-backup-solut-1460814873&asc_source=&tag=kinjalifehackerlink-20) 是一项低成本的在线存储服务，你每月只需为你使用的东西付费(在线存储空间加数据传输)。这就像亚马逊的另一个便宜的存储服务，S3——只便宜大约 10 倍。为什么花费这么少？亚马逊设计的 Glacier 针对你不经常访问的数据进行了优化——比如照片和视频、存档项目文件等的长期存储。你不应该使用它来定期检索文件或不断地从服务器上删除它们，如果你这样做，你会付出代价。

关于亚马逊冰川，最需要知道的是，如果要检索文件，需要 3 到 5 个小时才能完成。因此，这不是为了备份和快速检索您意外删除并立即需要的文件。

你的文件和文件夹存储在亚马逊冰川容器中，称为“金库”亚马逊称你冰川储藏室里的所有东西为“档案”这些可以是单个文件，或者您可以将多个文件和文件夹压缩到单个归档文件中，该归档文件可以高达 40TB。如果您需要检索数据，可以通过存档来请求。(他们不希望你一次下载整个库；如果你想，你会付出昂贵的代价。)

最后，定价有点复杂，亚马逊不提供上传和下载数据的软件，但你可以使用很棒的第三方工具。(见下文)

### 亚马逊冰川 vs. CrashPlan 和其他备份服务

那么，当你可以使用[Backblaze](http://www.backblaze.com)或另一个 [流行的在线备份服务](https://lifehacker.com/five-best-online-backup-services-1006345049) 时，为什么要为所有这些怪癖而烦恼呢？老实说，如果你只是想要一个 [一劳永逸的在线备份系统](http://lifehacker.com/set-up-an-automated-bulletproof-file-back-up-solution-5787572) ，那些在线解决方案之一将是最好的。

然而，如果你已经在本地将数据备份到 NAS 或外部驱动器，并且可能还在使用云存储和同步，如 Dropbox 或 Google Drive，亚马逊冰川可能是你非常便宜的异地备份。(还记得 [3-2-1 备份规则](https://lifehacker.com/why-you-should-always-have-more-than-one-backup-5961216) ？)这样，您就有了本地备份来检索删除的文件，在系统崩溃后恢复系统，或者做其他任何事情。你的亚马逊冰川备份就在那里，以防你的电脑和备份驱动器*都被毁坏，比如在火灾或地震中。*

不过，所有这些都取决于你想在异地存储多少。再来对比一下我们最喜欢的在线备份， [CrashPlan](https://www.crashplan.com/consumer/store.vtl) :

*   CrashPlan 为一台电脑制定的 10GB 备份计划是每月 2.99 美元。对于同样数量的冰川数据，大约是每月 0.10 美元。(以冰川服务器地区美国东部为例，因为它是价格最低的地区之一。)
*   CrashPan 的一台电脑的无限备份每月 5.99 美元。这大约相当于你每月在 Glacier 上存储 600GB 的费用。
*   其他例子:100GB 在 Glacier 上是每月 0.88 美元；200GB 每月 1.88 美元；300GB 每月 2.88 美元。

(CrashPlan 有更吸引人的定价如果你提前一年或更长时间付款而不是按月付款，我们来比较一下苹果和苹果。)因此，本质上，如果您要异地备份的数据少于 600GB，Glacier 是更实惠的选择。亚马逊冰川之于在线存储，就像预付费手机计划之于无线计划一样。

同样，这是假设您不需要定期检索任何数据(例如，您使用本地或 Dropbox 备份)，因为正如我前面提到的，存在检索费用。

为了看看这对你是否值得，使用这个 [冰川成本计算器](http://blender.ca/aws-glacier-calculator/) ，输入你想要备份的数据大小。(前期删除费是如果删除最近三个月上传的数据；它大约是每 GB 0.03 美元——或者说是你存储它三个月的费用，所以你还是把它放在那里吧。)

### 如何备份到亚马逊冰川

如果你觉得这听起来不错，那么开始使用 Glacier 相当容易。

#### 第一步:注册亚马逊网络服务

首先，登录您的亚马逊账户或在这里 创建一个新的亚马逊网络服务账户。您需要输入信用卡号，但在您开始使用亚马逊冰川/AWS 之前不会收取费用。您还必须通过电话验证您的身份，然后选择一个客户支持计划(大多数人都想要免费版本)。

此时，在设置的最后一个屏幕上，使用多因素身份验证(MFA)保护您的帐户，也称为 [双因素身份验证](http://lifehacker.com/tag/two-factor-authentication) ，这是您数据的第二层安全保护。例如，如果您的移动设备上有 Google Authenticator:

1.  从 Amazon 上的身份验证方法类型中选择“虚拟 MFA”
2.  然后，在谷歌认证器中，进入选项菜单添加账户>扫描二维码
3.  用你的移动设备，扫描亚马逊显示在屏幕上的条形码
4.  然后在 Amazon 安全页面中输入来自 Google Authenticator 的验证码

#### **第二步:为你的亚马逊冰川账户创建一个安全访问密钥**

接下来，转到 Amazon Web Service 中的 [安全凭证页面](https://console.aws.amazon.com/iam/home?#security_credential) ，展开“访问密钥”部分，并单击“创建新的访问密钥”按钮。您将把密钥文件(CVS 格式)下载到您的计算机上，其中有 Amazon Glacier 客户端软件访问您的文件所需的号码。

**第三步:在冰川中创建一个拱顶**

在 [亚马逊冰川控制台/主屏](https://console.aws.amazon.com/glacier/home) 中，点击创建金库按钮。您也可以单击顶部导航栏上的区域名称，切换到不同的数据中心。(亚马逊要求您为您的冰川存储选择一个数据中心:例如，美国东部、美国西部、亚洲、欧盟。这些有不同的定价方案。总的来说，美国东部和美国西部-俄勒冈州更便宜，但你会想检查前面提到的 [成本计算器](http://blender.ca/aws-glacier-calculator/) 。)

只需命名存储库，选择是否需要存储库活动通知，就大功告成了。如果您想要更好地组织保管库，您的 Glacier 帐户中可以有多个保管库(例如，“照片归档”或“软件备份”)，每个区域可以有多达 1，000 个保管库。此外，许多 Glacier 客户端允许您直接在软件中创建保管库。

#### **步骤 4:下载并安装亚马逊冰川客户端**

第三方软件使上传、同步和自动备份数据变得容易。我用的是 [Fast Glacier](http://fastglacier.com/) (免费，Windows)，因为它有很多功能，比如带宽调节、拖放支持、同步工具和智能数据检索支持(如果你必须检索文件，通过错开作业请求，这可以为你省钱)。其他受欢迎的客户端还包括前面提到的 Mac 版[Arq](http://www.haystacksoftware.com/arq/index.php)的[CloudBerry Explorer](http://www.cloudberrylab.com/free-amazon-s3-explorer-cloudfront-IAM.aspx)和 [。数字灵感有好看的](https://lifehacker.com/arq-backs-up-just-the-mac-files-you-need-to-amazon-s3-5900687) [几个冰川客户端的概述](http://www.labnol.org/internet/amazon-glacier-clients/25314/) 。

对于这些例子的其余部分，我将使用快速冰川截图，但它们在其他程序中应该是相似的。

#### **第五步:将你的亚马逊冰川客户端连接到你的账户**

打开您下载的安全访问密钥文件，获取访问 ID 和密钥代码，放入您的客户端。完成后，您将看到自己创建的保管库，并可以向其中上传文件和文件夹。

在 FastGlacier 和 CloudBerry Explorer(可能还有其他客户端)中，您可以简单地拖放文件夹和文件来开始上传。您可以使用映射的网络驱动器做到这一点，这非常适合备份 NAS。这也是你下载或删除文件的地方(知道上面提到的限制)。

#### **第 6 步:自动备份**

FastGlacier 有一个方便的比较和同步工具(在文件>与本地文件夹比较下)，在这里你可以看到冰川中缺少哪些文件，并选择同步它们(可以选择只上传更改的文件、新文件或缺少的文件)。不过，这需要手动启动。

要在 FastGlacier 中自动备份，您需要使用 Windows 任务计划程序。在任务计划程序中，创建一个新任务，并将其指向 FastGlacier 同步脚本(C:\ Program Files \ fast glacier \ glacier-sync . exe)。在任务的参数中，输入您的 Glacier 帐户名称、您计算机上的源文件夹、您为保管库选择的区域、保管库名称以及您要备份到的目录。更多例子参见 FastGlacier 的 [命令行旧同步工具](http://fastglacier.com/console-folder-sync-tool.aspx) 指令或者 [上天](http://www.getinthesky.com/2013/02/backup-to-amazon-glacier-for-free/) 。

作为一种替代方案，[CloudBerry Backup](http://www.cloudberrylab.com/amazon-s3-cloud-desktop-backup.aspx)(29.99 美元，Windows)更像是这项工作的传统备份工具，或者你甚至可以通过 FTP 备份 免费使用 [。](http://www.timbendt.com/2012/09/backup-to-amazon-glacier-for-very-little/)

基本就是这样。每年只需几美元，您就可以为您的备份系统添加更多的冗余，并且有信心将您最珍贵的数据保存在冗余服务器上，并且您的归档平均具有 99.999999999%的持久性。