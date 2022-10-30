# 我该如何为我游手好闲的室友关闭网络服务？

> 原文：<https://lifehacker.com/how-can-i-shut-off-internet-service-for-my-deadbeat-roo-1523049434>

*赖账的室友？你不必忍受他们拖欠的支票。自动关闭他们的互联网。只要有一点编码技巧，你就能做到。* [*栈交换*](http://cooking.stackexchange.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-105) *的专家告诉你怎么做。*



我有几个 [**的室友**](https://lifehacker.com/how-can-i-spot-a-horrible-roommate-before-i-move-in-732317810) **，他们每个月都和我分摊我的网费。有时他们忘了付钱给我，我不得不缠着他们要钱。如果纠缠了三天，他们仍然没有付款，我会在我的基于 Unix 的**[](http://lifehacker.com/a-command-line-primer-for-beginners-5633909)****路由器中创建一个防火墙规则，阻止流量流向他们的 Mac 地址。事实证明，这对于让拖欠房租的室友掏钱非常有效。****

**如何在每月 3 日自动向防火墙规则添加/删除 Mac 地址？我希望有一种简单的方法，一旦他们付款，就可以在这个月的剩余时间里解除对他们的封锁。我目前使用的 pfsense 里面有一个 [**的强制传送门模块**](https://doc.pfsense.org/index.php/Captive_Portal) **。我在考虑建立一个强制入口。到目前为止，我所看到的都不支持逐月授权访问的用例。****

***见原问题* [*此处*](http://superuser.com/q/695883/167769?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-105) *。***

### **你做得对( [由 NReilingh](http://superuser.com/questions/695883/how-can-i-turn-off-internet-for-roommates-that-havent-paid-the-bill-this-month#comment885418_695883?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-105) 回答)**

**你现在所做的听起来是最有效的方式——我无法想象一个强制门户解决方案会比完全的矫枉过正更好。如果有的话，您可以创建一个简单的 shell 脚本来自动添加规则。**

### **RADIUS 作为后端( [被掩盖 1](http://superuser.com/a/699502/23140?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-105) )**

**这可能超出了您的期望，但是您是否考虑过使用 802.1x 身份验证对 RADIUS 设置无线凭据作为后端？**

**可以设置 RADIUS 来检查您想要的任何验证器(您可能需要编写脚本并存储在数据库或其他东西中)，以查看您的室友是否已经付了房租。当他们验证并支付后，RADIUS 会验证他们。否则，它不会。积极的一面是，你不依赖于过滤 MAC 地址。这样，如果你有精通技术的室友，他们就不会轻易绕过你设置的控制。**

### **由尼古拉回答的和[的本质问题](http://superuser.com/a/695886/238539?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-105)**

1.  **创建一个 bash 脚本，添加限制性 iptables 规则。**
2.  **把这个脚本放在每月 cron。**
3.  **在 bash 脚本中设置一个条件——如果文件`~/do_not_block_friends`存在，并且它的修改时间在这个月内(`stat -c %y filename`)—不要运行这个脚本。**
4.  **一旦他们付钱，你就做`touch ~/do_not_block_friends`。**

**脚本将运行并看到`do_not_block_friends`被修改，因此它不会运行 iptables 命令。**

**如果他们没有付钱给你， [脚本](https://lifehacker.com/learn-to-write-bash-scripts-277509) 会屏蔽他们。一旦他们支付，你运行另一个准备好的脚本解锁。这是一个大概的计划，没有太多的细节，但我不认为它的其余部分很难弄清楚。**

**下面是编写这种脚本的更简单的方法:**

```
<code>#!/bin/bash  count=`find ~ -maxdepth 1 -type f -name do_not_block_friends -mtime -31 | wc -l`  if [ "$count" -eq 1 ]; then  # Friends have paid. Do nothing;  else  #Friends have not paid. Run iptables command;  fi 
```

**我们使用带有以下选项的`find`命令:**

*   **`maxdepth 1--`不要递归搜索**
*   **`type f--`搜索文件**
*   **`name--`搜索这个名字**
*   **`mtime -31--`查找不到 31 天前修改过的文件**

**`wc -l`将统计该命令生成的行数。如果朋友没有付款(什么也没找到),将是`0`;如果朋友付款了，我们做了`touch`控制文件，将是`1`。**

**该脚本不计算一个月中的天数，默认为 31 天。我认为这很好，因为我们不是在构建一个商业计费系统，但是我相信即使这样也可以在 bash 中计算。**

**<small>*不同意上面的一个答案？不太清楚它是如何工作的？在*</small> [<small>*原问题*</small>](http://superuser.com/q/695883/167769?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-105) <small>*留下自己的答案或提交评论。在*</small> [<small>*超级用户*</small>](http://superuser.com/?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-105) <small>*查看更多喜欢的问题，一个面向电脑爱好者和超级用户的问答网站。如果你有自己的电脑问题需要解决，请*</small> [<small>*提问*</small>](http://superuser.com/questions/ask?utm_source=lifehacker&utm_medium=syndication&utm_campaign=crowdhacker&utm_content=superuser-105) <small>*。你会得到答案的。(而且是免费的。)*</small>**

**Tina Mailhot-Roberge 的插图。T3】**