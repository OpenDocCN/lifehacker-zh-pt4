# 如何检查你的 Mac 或 Linux 机器是否容易受到 Shellshock 的攻击

> 原文：<https://lifehacker.com/how-to-check-if-your-mac-or-linux-machine-is-vulnerable-1639211806>

Shellshock，这个新发现的漏洞 [允许攻击者向你的机器](https://gizmodo.com/why-the-shellshock-bash-bug-could-be-even-worse-than-he-1639047786) 注入代码，使你的 Mac 或 Linux 面临恶意攻击的严重风险。以下是如何测试您的机器是否易受攻击。



Shellshock 使用 bash 脚本来访问您的计算机。从那里，他们可以启动程序、启用功能和访问文件。该脚本只影响基于 UNIX 的系统，因此 Linux 和 Mac 是唯一易受攻击的系统。

您可以通过从终端运行以下测试命令来测试您的系统:

`env x='() { :;}; echo vulnerable' bash -c 'echo hello'`

如果你不脆弱，你会得到这样的结果:

`bash: warning: x: ignoring function definition attempt bash: error importing function definition for `x' hello`

如果你很脆弱，你会得到:

`vulnerable hello`

您还可以通过输入以下命令来检查您正在运行的 bash 的版本:

`bash --version`

如果你得到版本 3 . 2 . 51(1)-结果发布，你将需要更新。许多 Linux 发行版已经有补丁可用，所以你可以 [按照这些指令](http://www.linuxnews.pro/patch-bash-shell-shock-centos-ubuntu/) 来更新你的系统。**更新:** Mac 用户现在可以从苹果获得补丁。可以 [在这里](http://support.apple.com/kb/DL1769) 下载安装。