# 如何快速学习终端命令？

> 原文:[https://life hacker . com/how-can-I-quick-learn-terminal-commands-1494082178](https://lifehacker.com/how-can-i-quickly-learn-terminal-commands-1494082178)

在 Ubuntu 中，鼠标点击只能让你到此为止。对于认真使用“另一个操作系统”的人来说，学习终端命令是重要的一步专家们在 [*询问 Ubuntu*](http://ubuntu.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=ubuntu-99) *提供学习“shell”的最佳方法*

Watch

在我看来，学习如何使用终端是学习如何使用 Ubuntu 的先决条件。所以我在努力找出最好的学习方法。有 Quizlet 在线闪存卡吗？更好的方法？

*见原问题* [*此处*](http://askubuntu.com/q/337300/59636?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=ubuntu-99) *。*

#### 随机学习( [由拉杜·勒德努](http://askubuntu.com/a/337382/147044?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=ubuntu-99) 回答)

您可以在“~/”的末尾添加以下行(命令)。“bashrc”文件:

```
echo "Did you know that:"; whatis $(ls /bin | shuf -n 1)
```

每次打开终端，你都会学到一些关于随机命令的知识。

如果你想找点乐子，可以用‘cow say’‘utility’。要安装它，请在终端中运行:

```
sudo apt-get install cowsay
```

然后在“~/”的末尾添加下面一行。“bashrc”文件:

```
cowsay -f $(ls /usr/share/cowsay/cows | shuf -n 1 | cut -d. -f1) $(whatis $(ls /bin) 2>/dev/null | shuf -n 1)
```

或者可以在' ~/中添加上面一行作为别名。bash_aliases。我补充道:

```
alias ?='cowsay -f $(ls /usr/share/cowsay/cows | shuf -n 1 | cut -d. -f1) $(whatis $(ls /bin) 2>/dev/null | shuf -n 1)'
```

每当你觉得无聊的时候，你可以在终端输入:'？'(后面跟着回车)。就像自己玩骰子一样。

#### 什么是( [由阿丘](http://askubuntu.com/a/337303/9701?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=ubuntu-99) 回答)

我过去常玩“什么东西”。这不完全是一个游戏，但这是一个相对容易的学习方法。例如，键入`whatis sudo apt-get update`，它会返回:

```
![whatis sudo apt-get update]
```

在我执行任何命令之前，我会先点击“whatis”。我知道我要做什么，然后我会充满信心地执行命令。

如果“whatis”不能提供太多信息，或者对我来说不清楚，我会去阅读“man”。

比如`man sudo`。

谷歌在这里给了你这么多信息，里面的来源 [问 Ubuntu](http://askubuntu.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=ubuntu-99) 和外面的。在这里，LMGTFY: [在 Ubuntu 上学习终端命令的最好方法](http://www.google.co.uk/search?%7Bgoogle:acceptedSuggestion%7Doq=learn%20terminal%20command%20game&sourceid=chrome&ie=UTF-8&q=learn%20terminal%20command%20game#fp=cb6a94a782f8cc3b&q=best%20way%20to%20learn%20terminal%20commands%20on%20ubuntu) 。

#### 一局( [由 snim2](http://askubuntu.com/a/337507/41916?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=ubuntu-99) 回答)

是的，终点曾经是这样的游戏，将有所帮助。这里有真人版。而 github 上的代码是 [。这是一个好主意，尽管我更希望代码更容易扩展。](https://github.com/mprat/Terminus)

#### 终端不是学习 Ubuntu 的先决条件( [由 avernet](http://askubuntu.com/a/337424/187410?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=ubuntu-99) 回答)

Ubuntu 的设计非常用户友好。学习如何使用终端并不是学习如何使用 Ubuntu 的先决条件。但是，如果您想成为超级用户或自己解决问题，就需要这样做。

为了回答你的问题，我不知道有什么游戏是为帮助或教授 shell 命令而设计的，但是我强烈推荐以下与 bash 和系统管理相关的资源:

*   [UNIX 初学者教程](http://www.ee.surrey.ac.uk/Teaching/Unix/) (请注意，本教程使用了 Red Hat(另一个 Linux 发行版)，并引用了一些只适用于萨里大学学生的目录。)
*   [【BASH 编程——入门指南](http://www.tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html) (主持于 Linux 文档项目，作者 Mike G)。
*   [Bash Shell 脚本](http://en.wikibooks.org/wiki/Bash_Shell_Scripting) (来自维基百科的 wikibook)
*   [学习手册](http://www.nongnu.org/lpi-manuals/manual/) 来自 Linux 职业学院(LPI)
*   [GNU Bash 参考手册](http://www.gnu.org/software/bash/manual/bashref.html)
*   作者孟德尔·库珀的《高级 Bash 脚本指南》

<small>*不同意以上答案？有自己的专长可以贡献？查看*</small> [<small>*原问题*</small>](http://askubuntu.com/q/337300/59636?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=ubuntu-99) <small>*，在*</small> [<small>*问 Ubuntu*</small>](http://ubuntu.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=ubuntu-99)<small>*查看更多类似这样的问题，一个面向 Ubuntu 用户和开发者的问答网站。而如果你有自己的 Ubuntu 问题需要解决，*</small> [<small>*提问*</small>](http://ubuntu.stackexchange.com/questions/ask?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=ubuntu-99) <small>*。你会得到答案的。(而且是免费的。)*</small>