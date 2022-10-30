# 将你变成电子表格忍者的四项技能

> 原文:[https://life hacker . com/four-skills-that-will-turn-you-a-spread sheet-ninj-1525058930](https://lifehacker.com/four-skills-that-will-turn-you-into-a-spreadsheet-ninj-1525058930)

电子表格是你在成年生活中遇到的最神秘的软件之一。尽管它们可能很可怕，但是你可以用四个简单的技巧做很多事情。

Watch

出于本文的目的，我们将把重点放在 Microsoft Excel 上，因为这是使用最广泛的电子表格软件。然而，几乎所有这些技能和功能在 LibreOffice 和 Google Drive 中都很有用。必要时，我们会做笔记，以强调套房之间的差异。

### 使用表单轻松输入数据

将数据输入电子表格是任何分析的起点。虽然您可以手动输入您需要的数据，但是表单允许您(或者在某些情况下，允许其他人)快速地逐行输入信息，而不需要太多的麻烦。

在 Excel 2013 中，表单按钮有点害羞地隐藏起来了，但是您可以像这样恢复它:

1.  右键单击功能区界面上的任意位置，然后选择“自定义功能区”
2.  在右侧窗格中，选择要添加表单按钮的功能区部分。
3.  在左侧，从下拉列表中选择“不在功能区中的命令”。
4.  在下面的框中，从列表中选择“表单…”并单击“添加”将其放入功能区。

现在功能区中有了表单按钮，可以创建数据输入表单了。首先创建标题和第一行条目。在中有了初始数据集后，可以使用 form 命令输入其他行。只需将光标放在数据集的左上角，然后单击表单按钮。

将出现的对话框允许您逐行输入信息。填写表单，按 enter 键，将会创建一个包含所有新信息的新行。

#### 使用 Google Drive 创建面向公众的表单

Google Drive 没有完全相同的功能，但它有自己值得注意的形式。您可以直接在 Drive 中创建表单，也可以从电子表格中创建表单。您将创建供用户回答的问题，他们的回答将填充一个表单。要创建表单:

1.  在电子表格中，单击插入>表单。
2.  在表单顶部输入描述。
3.  输入并修改每个问题:
4.  在“问题标题”框中输入标题。
5.  选择问题类型。
6.  可选:选择数据验证的形式。您可以使用它来确认输入的数据符合特定的类型，如设定范围内的数字或电子邮件地址形式的文本。
7.  可选:选择“必填问题”

完成表格后，您可以公开分享或通过电子邮件发送给一组特定的受访者。所有条目将被自动放入时间戳旁边的列中，时间戳指示数据提交的时间。

### 使用函数和公式执行计算

你已经输入了一堆数据，但是现在你需要对它做些什么。函数和公式允许您操作电子表格中的数据。您可以执行简单的数学运算，如将一列中的数字相加，获得平均值，甚至可以处理现实世界中的事情，如日期或财务计算。

各种电子表格程序都有自己的一套功能，虽然其中许多功能在不同的套件之间是共享的，但还是有一些差异，所以一定要查看完整的列表，例如[libre office](https://help.libreoffice.org/Calc/Functions_by_Category)和 [Google Drive](https://support.google.com/drive/table/25273?hl=en) 。

记住这一点，这里有几个你可以做的例子。

#### 执行基本数学运算

最简单的是，函数可以使用您输入的任何数据执行基本的数学运算。例如，假设您需要将两个单元格中的数字相加。为此，您可以使用 SUM 函数:

```
=SUM(A1,B1)
```

这将把单元格 A1 和 B1 的内容相加。对于简单的数学，您也可以使用典型的简写数学运算符，如+、-、*和/。例如，下面将执行与上面的示例完全相同的数学运算:

```
=A1+B1
```

您可以将任意多个单元格中的值相加。你可以用冒号来实现，就像这样:

```
=SUM(A1:A10)
```

上面的函数将把 A 列中第 1 行和第 10 行之间的所有数字相加，将负值计算在内。你可以在这里 找到 Excel 可以执行的 [所有数学函数的列表。](http://office.microsoft.com/en-us/excel-help/examples-of-commonly-used-formulas-HP005200127.aspx)

#### 进行统计计算

您还可以对一组数据进行统计计算，包括计算平均值中位数。举个例子:

```
=AVERAGE(A1:A10)
```

函数 上面的 [将返回 A1 和 A10 之间所有单元格的平均值。各种功能包括基本和高级统计功能。虽然并不是所有的函数都对普通的电子表格爱好者有用(是的，我们确实存在)，但是像和](http://office.microsoft.com/en-us/excel-help/average-function-HA102753108.aspx?CTT=5&origin=HA102752955) [中值](http://office.microsoft.com/en-us/excel-help/median-function-HA102752938.aspx?CTT=5&origin=HA102752955) 这样的简单函数在日常工作中确实很有帮助。

#### 格式化并计算日期和时间

您还可以使用公式来处理日期和时间格式的条目。例如，您可以使用以下函数计算两个日期之间的天数:

```
=DAYS([End_date],[Start_date])
```

Excel 还包括一个返回当前日期的函数:

```
=TODAY()
```

这个函数将把今天的日期放在一个单元格中。您可以将这两个函数结合起来，创建一个公式来计算距离未来某个特定日期还有多少天，如下所示:

```
=DAYS(TODAY(),[Target_date])
```

还有许多其他的日期和时间函数，你可以在这里 查看 [。](http://office.microsoft.com/en-us/excel-help/excel-functions-by-category-HA102752955.aspx#_Toc309306709)

#### 组合多个函数来创建公式

正如您在上一个示例中可能已经注意到的，您可以组合多个函数来创建所谓的公式。从本质上讲，公式是放在一个单元格中的多个函数。因此，例如，如果您想将 A 列中的数字相加，并将其四舍五入为最接近的整数，您可以使用以下公式:

```
=ROUND((SUM(A1:A10)),0)
```

上面的公式由两个函数组成: [SUM](http://office.microsoft.com/en-us/excel-help/sum-function-HA102752855.aspx?CTT=5&origin=HA102752955) 作为 [ROUND](http://office.microsoft.com/en-us/excel-help/round-function-HA102752882.aspx?CTT=5&origin=HA102752955) 的自变量。在此语句中，单元格 A1 到 A10 将首先相加，然后将得到的数字提供给 ROUND 函数，四舍五入到最接近的整数。公式可以简单也可以复杂，尽管它们越复杂，语法也越复杂。你可以在 这里阅读更多关于公式语法如何工作的 [。](http://www.wikihow.com/Type-Formulas-in-Microsoft-Excel)

函数也可以与 [逻辑函数](http://office.microsoft.com/en-us/excel-help/excel-functions-by-category-HA102752955.aspx#_Toc309306713) 组合，创建条件公式。构建有用的公式是一个非常广泛的主题，它可以产生自己的一整套文章。幸运的是，我们在 How-To Geek 的朋友有一套关于这个主题的深入文章。你可以在这里找到第一课。

### 使用筛选器和数据透视表对数据进行排序

所以你已经输入了你的原始数据，做了你需要做的任何计算，现在是时候实际解释它了。您有几个可视化数据的选项，这取决于您需要如何使用它。

#### 按列排序

有时，您可能需要按您输入的类别之一对数据进行排序。就像你的 iTunes 音乐库一样，你可以按列重新排列你的数据。为此:

1.  按 Ctrl-A 选择工作表中的所有内容。
2.  选择功能区中的数据选项卡。
3.  点击“排序”
4.  选择要作为排序依据的列和排序标准。
5.  单击确定。

例如，参见上面的屏幕截图——我们已经按照订单编号对整个数据集进行了重新排序，从最少到最多。

#### 过滤掉重复的项目

有时，一个类别中可能会有一些重复的项目。在上面的例子中，我们有 8 个条目，但是只有 5 个名字。要过滤掉这些重复项并查看我们拥有的所有名称(而不是所有订单)，我们可以使用功能区中 Data 选项卡下的过滤选项。为此:

1.  在“数据”下，单击“排序和过滤”部分中的“高级”。
2.  选择“拷贝到另一个位置”,以非破坏性方式提取特定数据(如果您想要删除电子表格中在此栏中没有唯一数据的任何行，请选择“就地过滤列表”。)
3.  单击“列表范围”框，选择要过滤的列。
4.  单击“复制到”框，选择要将唯一数据列表复制到的空单元格。
5.  确保选择了“仅唯一数据”。
6.  单击确定

这将创建一个新列，其中只包含该范围内的唯一数据，这对于分隔重复条目非常有用。

#### 创建数据透视表

当你有数百行数据时，几乎不可能从中收集任何信息——你需要一个摘要。数据透视表允许您提取数据的某些部分并对其进行汇总，因此您只能看到您想看到的内容。

以下面的例子为例。假设我们想看看从 Bob Boberson 那里得到的总金额。

这些数据现在看起来很容易，但如果有几十或几百笔交易，就不是这样了。因此，要查看汇总，请创建一个数据透视表:

1.  创建一个名为“工作表 2”的新工作表。
2.  在“插入”选项卡下，单击“数据透视表”。
3.  单击工作表 1 并选择工作表中所有填充的单元格。
4.  单击确定。
5.  在右侧窗格中，您可以将列拖到筛选、列或行中。对于本例，将“Name”拖到“Filters”部分，将“Order number”拖到“Rows”部分，将“Payments”拖到“Values”部分。
6.  这将创建一个表格，列出每个订单编号上的所有付款。在数据透视表顶部的下拉框中，您可以选择一个特定的客户来查看他们的订单。

当我们这样做时，我们得到这样的结果:

有了数据透视表，我们可以很容易地看到 Bob Boberson 下的所有订单以及他支付的所有款项的总和。

这只是你如何使用数据透视表的一个简单例子——它们的用途非常广泛，你可以用它来概括任何事情。要在 LibreOffice 或 Google Drive 中创建数据透视表，请进入数据>数据透视表。

### 使用宏和脚本执行重复性任务

使用电子表格很快就会变得重复。为了使一些重复的任务更简单，您可以使用 Excel 将您反复做的事情记录到一个宏中。然后，任何时候你需要重复这些任务，你可以使用快捷键来“回放”宏，它会为你做所有的工作。例如，假设我们想将一大组单元格的字体更改为非常特殊的字体，如 Arial 12 斜体:

1.  在“视图”选项卡下，单击“宏”下拉列表并选择“记录宏”。
2.  给宏命名。
3.  可选:为宏分配键盘快捷键。
4.  单击确定
5.  单击主页选项卡。
6.  从字体下拉列表中选择“Arial”。
7.  从尺寸下拉列表中选择 12。
8.  单击斜体按钮。
9.  单击 Excel 左下角的“停止”按钮。

从那时起，您将能够通过按一个键盘快捷键(您在步骤 3 中指定的快捷键)，或者通过从“视图”>“宏库”中选择宏，来应用 12pt 大小的 Arial 字体和斜体。显然，这是一个基本的例子，但是您可以使用宏特性来记录任何重复的任务。你同样可以在 LibreOffice 中录制宏 [。](https://help.libreoffice.org/Common/Recording_a_Macro)

在 Excel、LibreOffice 和 Google Drive 中，只要稍微懂点编程，就可以创建更复杂的宏和脚本(事实上，脚本是使用专有脚本格式在 Google Drive 中自动化任务的唯一方式)。要开始了解这些，请查看下面的资源:

*   [Excel:使用宏](http://office.microsoft.com/en-us/excel-help/work-with-macros-RZ103988275.aspx?CTT=5&origin=HA104032083)
*   [LibreOffice:宏入门](http://libreoffice-na.us/English-4.0-installs/documentation-PDF-and-other/0100-LibreOffice--Getting-Started/GS4013-GettingStartedWithMacros.pdf)
*   [Google Drive:Google Apps 脚本概述](https://developers.google.com/apps-script/overview)

### 更多资源

所有这些技能只是冰山一角。使用电子表格本身就是一门学科，如果你愿意，你可以更深入地研究每一个类别。为了方便起见，这里有一些资源，你可以用来学习更多关于这些技能和磨练你的手艺:

**表格和数据输入**

*   [在 Excel 中创建订单](http://www.contextures.com/xlOrderForm01.html)
*   [用 LibreOffice](https://help.libreoffice.org/Common/Working_with_Forms) 创建表单
*   [创建谷歌表单](https://support.google.com/drive/answer/87809?hl=en)

**函数和公式**

如何进入极客学校:

*   [为什么需要公式和函数？](http://www.howtogeek.com/school/microsoft-excel-formulas-and-functions/lesson1/)T3】
*   [定义和创建公式](http://www.howtogeek.com/school/microsoft-excel-formulas-and-functions/lesson2/)
*   [相对和绝对单元格引用，并格式化](http://www.howtogeek.com/school/microsoft-excel-formulas-and-functions/lesson3/)
*   [你应该了解的有用功能](http://www.howtogeek.com/school/microsoft-excel-formulas-and-functions/lesson4/)
*   [查找、图表、统计和数据透视表](http://www.howtogeek.com/school/microsoft-excel-formulas-and-functions/lesson5/)

**过滤和透视表**

*   [在 Excel 中过滤数据](http://www.gcflearnfree.org/excel2013/19)
*   [【过滤区域或表格中的数据(Excel)](http://office.microsoft.com/en-us/excel-help/filter-data-in-a-range-or-table-HP010073941.aspx)
*   [【数据透视表 101 (Excel)](http://office.microsoft.com/en-us/excel-help/pivottable-reports-101-HA001034632.aspx)
*   [【透视表(LibreOffice)](https://help.libreoffice.org/Calc/Pivot_Table)
*   [【数据透视表概览(Google Drive)](https://support.google.com/drive/answer/1272898?hl=en)

**宏和脚本**

*   [在 Excel 中使用宏](http://office.microsoft.com/en-us/excel-help/work-with-macros-RZ103988275.aspx?CTT=5&origin=HA104032083)
*   [libre office 宏入门](http://libreoffice-na.us/English-4.0-installs/documentation-PDF-and-other/0100-LibreOffice--Getting-Started/GS4013-GettingStartedWithMacros.pdf)
*   [open office 宏介绍](http://www.linux.com/learn/tutorials/380813-introduction-to-openoffice-macros)
*   [Google Apps 脚本概述](https://developers.google.com/apps-script/overview)
*   [用 Apps 脚本](https://support.google.com/drive/answer/2942256?hl=en) 扩展 Google 文档、表格和表单