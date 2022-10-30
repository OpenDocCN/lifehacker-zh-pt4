# 构建一个超级机器人手臂:初学者的完美 Arduino 项目

> 原文:[https://life hacker . com/build-a-kickass-robot-arm-the-perfect-arduino-project-1700643747](https://lifehacker.com/build-a-kickass-robot-arm-the-perfect-arduino-project-1700643747)

Arduino 是一种廉价、有趣的方式来建造自己的电子产品 。开始也可能令人望而生畏。在这里，我们将向您展示如何用一个杀手级项目获得一个从头到尾的 Arduino 入门:构建 [一个甜美的机械臂](http://store.hackaday.com/products/mearm-pocket-sized-robot-arm) 。

Watch

在本指南中，我们将使用 [meArm 机械臂](http://www.phenoptix.com/products/mearm-pocket-sized-robot-arm) 项目作为各种技能的指南，向您介绍 Arduino。meArm 是一个开源套件，包含构建一个小型 Arduino 驱动的机械臂所需的所有部件。你可以从 Hackaday 或 [等](http://www.thingiverse.com/thing:360108) [商店订购一套现成的，或者从 Thingiverse](http://store.hackaday.com/products/mearm-pocket-sized-robot-arm) 下载设计图，自己裁剪。你可以使用激光切割机、 [3D 打印机](http://lifehacker.com/how-to-get-started-with-3d-printing-without-spending-a-1340345210) ，甚至可以用木头雕刻出零件。这些工具包相对便宜(我的大约 50 美元)，所以很容易买到。

### **为什么是机械臂？**

学习任何新技能总是一个挑战。Arduino 可能特别令人生畏，因为你实际上是在学习如何从零开始构建整个电子设备。它需要同时学习几种新技能:电力、试验板、编码、传感器、伺服系统、远程控制、组装等等。

这些技能中的任何一项都很难独自学会。虽然网上有大量的教程，但重要的是要有一个单一的总体目标，你可以朝着这个目标努力 。我们还知道，当你 [将你的学习随着时间](http://lifehacker.com/the-science-behind-how-we-learn-new-skills-908488422) 展开时，你的大脑学习得更好。有什么东西 [让你兴奋的](http://lifehacker.com/stay-passionate-by-asking-what-am-i-excited-about-5929021) 伤害不了。

建造一个机器人手臂是一个长期的项目，可以一次性满足所有这些需求。在过去九个月左右的时间里，我个人一直在尝试断断续续地学习 Arduino 项目，在这段时间里，机械臂是我经历过的最好的学习体验，特别是因为:

*   很全面:找到第一个项目很难。找到一个能真正教会你东西的人就更难了。你可以很容易地构建一个 LED 电路，但你所拥有的只是一个 LED 电路。学习建立一个机器人手臂将教你如何电路板电路，如何编程你的 Arduino，以及如何与移动部件。最终，你将拥有一个真正的、物理的东西，它按照你的程序去做。而不仅仅是一个概念验证灯，当你按下按钮时就会打开。
*   **它是可扩展的:**如果说钢铁侠的 [45 套不同的套装](http://ironman.wikia.com/wiki/Mark_45) 教会了我们什么，那就是你总能改进一个机器人。这个机器人手臂工具包从一些基本的基本技能开始，但你可以在它的基础上进行各种扩展。你可以添加遥控器(像 [红外](http://www.espruino.com/MeArm) 或者 [蓝牙](https://www.youtube.com/watch?v=HbxhVs3UmuE) )，甚至学习如何用 [额外的盾牌](https://learn.adafruit.com/16-channel-pwm-servo-driver/overview) 扩展你的 Arduino 的能力。只要问“我还能让它做什么？”你可以找到各种新技能来学习，而不用从头开始一个新项目。
*   这太酷了:如果你读到这里，很有可能是因为拥有自己的机器人让你兴奋。机器人很酷。他们还会感到未来派和难以接近。如果当你对你正在学习的东西感到兴奋时，学习会更好，那么很难击败机器人手臂闯入 Arduino 世界。

尽管如此，这并不一定意味着这应该是你的第一个项目。可以的！但是如果你从来没有接触过电路板，慢慢来也没问题。不要把机械臂当成你的第一步。就当是你的期末考试吧。一旦你有了一个好的 [Arduino 初学者工具包](https://www.adafruit.com/categories/172) ，你应该尝试一些基本的东西，比如把 LED 插到试验板上或者用按钮控制它，只是为了掌握它的窍门。不过，你或许可以跳过“爱情速度计”项目 。

最重要的是，**谷歌一切**。记住，这是一个长期的项目。我们不会指导您完成每一步，但我们会向您展示实现这一目标所需的构建模块。不要指望周五开始时没有经验，周日就能拥有一个遥控的、有感知能力的机器人。在整篇文章中，我们会有很多指向指南的链接，我们完全希望您离开这里，跟随这些指南几个小时，然后再回来。不要把它想成一个循序渐进的手册，而更像一张地图。如果你一路上有点迷路，不要害怕停下来问路。

### **你需要什么**

本指南将分为两个主要部分。第一步是建造基本的机器人手臂并投入使用。第二部分将向您展示一些可选项目，您可以使用它们来扩展它的功能。要完成第一部分，你需要:

*   Arduino 初学者工具包:大多数 Arduino 初学者工具包将包括您在这个项目(以及许多其他项目)中需要的基本组件。你需要一个 Arduino(我们将使用一个[**【Uno R3】**](http://www.arduino.cc/en/Main/ArduinoBoardUno)**)、各种长度的电线、一根 USB 电缆来连接到你的计算机，以及一个** [**试验板**](https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard) **和** [**一个电位器**](http://www.arduino.cc/en/Tutorial/Potentiometer) **，它可以在以后用作控制你的机器人的旋钮。Adafruit 有几款** [**入门套件可供选择，这里有**](https://www.adafruit.com/categories/172) **价格不等。** [**特别是这个套装**](https://www.adafruit.com/products/68) **包括上面列出的所有东西，售价 65 美元。稍后你可能还需要一个 470uf 的电容，你可以在 RadioShack 的** [**买到非常便宜的**](http://www.radioshack.com/470uf-35v-20-radial-lead-electrolytic-capacitor/2721030.html#.VT-Jh_nBzRY) **。**
*   **一套 meArm 套件:为了简单起见，你可以在这里** **购买一整套套件** [**。这包括建造手臂本身所需的一切。或者，您可以在此处**](http://store.hackaday.com/products/mearm-pocket-sized-robot-arm) **下载** [**计划并自行制作。平面图确实需要非常精确的尺寸，所以只有在你有工具可以正确切割(或 3D 打印)的情况下才使用这个选项。**](http://www.thingiverse.com/thing:360108)
*   一个 Arduino IDE:一个 IDE(或称 [**集成开发环境**](http://en.wikipedia.org/wiki/Integrated_development_environment) **)是一个程序，你可以用它来编写和上传软件——称为“草图”——到你的 Arduino 上。你可以在这里** **下载官方 Arduino IDE** [**。在我的个人经历中，我发现**](http://www.arduino.cc/en/main/Software) [**之前提到的**](http://lifehacker.com/codebender-makes-it-easy-to-program-your-arduino-from-a-1309299552)**[**CodeBender**](https://codebender.cc/)**是一个优秀的、基于浏览器的替代品，它可以在线存储你的草图，以便于访问。****

**这些将让你开始，并涵盖基本知识。一下子买也是很多的，如果你不想比这个更进一步，也不要难过。随着时间的推移，你可以添加更多的工具和设备到你的军火库。**

### ****该项目需要什么****

**我们假设您已经获得了上一节第一个项目列表中的所有东西，并且您已经准备好将您的机器人组装起来。我们不会像其他更官方的指南那样详细介绍每一个步骤，但是我们会指导你完成项目的不同阶段。你可以以你觉得舒服的任何速度进行，但我们会把它分成几个部分，你可以在多个周末处理。**

#### ****第一阶段:施工****

 **[https://lifehacker.com/embed/inset/iframe?id=youtube-video-p_n_xKCrfrk&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-p_n_xKCrfrk&start=0)** 

**需要什么:在这个阶段，你要组装你的机械臂。它还不会做任何事情，但看起来会很酷。该公司的工具包后面有 [这里有](http://www.instructables.com/id/Pocket-Sized-Robot-Arm-meArm-V04/?ALLSTEPS) 的详细说明。你的工具包应该带有一套各种塑料件，一些螺丝，和四个伺服。如果你以前从未使用过伺服系统，它是一个小的，低功率的马达，将为你的机器人的运动提供动力。该套件在底座上使用一个，在臂的两侧各使用两个，在夹持器上使用一个。如果你曾经做过一件宜家家具，这应该不会太复杂。只要准确地按照指示**去做**。机器人比你的咖啡桌更精致，这里的螺丝拧得过紧，或者那里用错了零件，都会让你头疼。幸运的是，上面的说明非常详细，会在你做一些会把你搞得一团糟的事情之前反复警告你，所以你很安全。**

****你将学到什么:**就个人而言，这是我最喜欢的部分，因为你学到了大多数项目教程忽略的东西:*如何构建这个东西*。许多项目向你展示了一个挂在试验板上的概念，但是从来没有把它变成现实。在这里，您将学习如何将伺服系统安装到已完成项目的工作部件上。你还将学习使用微小运动部件的微妙艺术。**

****所需时间:**这里的施工部分只要几个小时就能完成。然而，我建议让你的工作深入一点。如果你以前从未使用过机器人，这是一个很好的机会来检查你的机器人是如何组装的，它是如何移动的，并开始考虑以后如何安装你的 Arduino。下一步可能会变得复杂，所以不要急于求成。你可以手动轻轻移动机械臂**的部件**来摆弄它。不过，不要太用力，否则会损坏伺服系统。**

#### ****第二阶段:试验板****

**下一步是将你的一个伺服系统连接到你的 Arduino 上。你可以使用 [和](http://en.wikipedia.org/wiki/Breadboard) 来完成这个任务。试验板是一种简单的工具，允许在完全组装之前制作电子电路原型，不需要焊接。Adafruit 有 [这里有一个优秀的教程](https://learn.adafruit.com/adafruit-arduino-lesson-14-servo-motors/overview) ，它将带你完成将你的伺服直接连接到 Arduino 的步骤，以及在后面的步骤中添加一个电位计，你可以用它作为一个旋钮来手动控制移动。**

**如果这一段有点令人不知所措，那么这是一个很好的时间来备份和学习如何面包板工程。Sparkfun 的 [有一个很好的指南](https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard) ，它解释了如何使用试验板以及你可以用它做什么。Tutsplus 有 [一个很棒的教程](http://computers.tutsplus.com/tutorials/how-to-use-a-breadboard-and-build-a-led-circuit--mac-54746) 关于如何将 LED 连接到电源并添加按钮。花点时间组装这个，理解你刚刚组装的电路。一旦你掌握了电流如何通过一个简单的电路，你应该准备好连接你的机器人的伺服系统。从个人经验来看，这一部分似乎令人望而生畏。不过，组装零件并遵循说明是很容易的。理解它是如何工作的是困难的部分，但这需要时间。**

****你将学到什么:**试验板是大多数业余电子产品原型制作的基础。如果您遵循了以上所有指南，您将学会如何将 led、按钮、电阻器、电位计和伺服系统连接到电源或 Arduino。有了这些组件，你已经可以做出很多有趣的东西了。一旦你有了基本的东西，通过学习不同类型的组件，它们是如何工作的，以及如何将它们集成到你的项目中，你就可以更容易地构建它了(在下面的扩展部分中有更多的方法)。**

****所需时间:**如果你已经熟悉试验板，连接伺服应该需要大约五分钟。*然而*，如果你以前从未接触过电子产品，给自己一两天时间阅读上面的指南，摆弄各种电路，感受一下它们是如何工作的。我甚至建议花一周时间来消化你所学到的东西。试验电路板电路很简单，但很难理解。这不是你想匆忙完成的事情，尤其是考虑到下一部分会变得多么复杂。**

#### ****第三阶段:编程****

**需要什么:一旦你把所有东西都装好，就该开机了。为此，您需要安装 Arduino IDE 并将其插入主板。如果你想像我一样使用 [CodeBender](https://codebender.cc/) ，可以在这里按照 [入门指南](https://codebender.cc/static/walkthrough/page/1) 。或者，你可以按照 Adafruit 的 [指南到官方 ide 这里](https://learn.adafruit.com/adafruit-arduino-ide-setup) 。**

**一旦你的环境设置好了，你就可以开始编程了。Adafruit 的指南有 [一个简单的伺服草图](https://learn.adafruit.com/adafruit-arduino-lesson-14-servo-motors/arduino-code-for-sweep) 你可以用它来让你的机器人移动。我建议使用底部的伺服系统，因为它是你的机器人上唯一一个可以进行 180 度全方位运动的系统。如果你用其他伺服系统尝试这个草图，你可能会通过迫使它们超出物理极限来损坏其他一些伺服系统。然而，一旦你理解了这个草图是如何工作的，你可以试着修改它来和其他的一起工作！**

**你将学到什么:在这个阶段，所有的事情都汇集在一起。你会学到一些关于伺服运动如何工作的知识，并且*会学到很多关于如何编写 Arduino 程序的知识。如果你以前从未涉足过编程，你可以将 sweep sketch 放到 IDE 中，它将会工作，但是我建议查看一下我们以前的一些关于如何学习编码的指南。Arduino 语言与 C/C++和 Java 共享很多语法，所以如果你有任何使用这些语言的经验，你应该会感觉很舒服。你也可以在这里 查看 [Arduino 参考库。](http://www.arduino.cc/en/Reference/HomePage)***

**即使你有一些编程经验，我也建议你再花一个周末来学习如何设置 Arduino IDE。学习编码是一生的技能，所以不要害怕在这个阶段工作几个星期。你可以在此基础上使用 [旋钮绘制](https://learn.adafruit.com/adafruit-arduino-lesson-14-servo-motors/the-breadboard-layout-for-knob) 提供的 Adafruit 草图，这将允许你手动控制你的机器人。不要害怕搞砸。在这个阶段，您还可以尝试一些基本的逻辑结构。**

#### ****恭喜你！你刚刚做了一个机器人****

**如果你完成了所有这些，那么你只是在一个长期的项目中学到了一些技能。当我第一次组装这个机器人时，我发现它出奇的简单，尽管它是许多复杂主题的介绍。然而，一旦你坚持到最后，大多数电子项目——像我们经常提到的 中的[——看起来就不再那么可怕了。](http://lifehacker.com/tag/arduino)**

**从这里，你可以开始扩展你所拥有的。如果你觉得你只是勉强通过这一点，尝试简单的增加，如 [增加一个 LED](https://www.youtube.com/watch?v=YWY_Is0L7fE) 来指示电机何时转动，或 [一个按钮](http://www.raywenderlich.com/32392/arduino-tutorial-for-complete-beginners-using-a-button) 来打开和关闭运动。稍微摆弄一下这个软件，看看它的反应如何。如果你搞砸了某个软件，推翻了某个伺服，可以在线订购 [超级便宜的替换品](http://www.hobbyking.com/hobbyking/store/__9549__Turnigy_TG9e_9g_1_5kg_0_10sec_Eco_Micro_Servo.html) 。**

### ****利用这些扩展项目积累您的知识****

**你造了一个机器人。现在怎么办？好吧，假设它还没有 [变得有知觉并试图杀死人类](https://www.youtube.com/watch?v=tmeOjFno6Do) ，你可以在现有项目的基础上一点一点地进行一些项目。我们不会讨论每一个细节，但我们会给你一些链接让你开始:**

#### ****同时控制多个伺服系统****

**对于我的构建，我订购了 [这个微控制器](https://www.adafruit.com/product/815) ，它可以自己控制多达 16 个伺服系统(对于那些在家计算的人来说，这将增加到 4 个臂机器人...甜)。该套件是**而不是**预组装的，这意味着它将需要一些焊接工作。你可以得到其他控制器 [像这个](https://www.pololu.com/product/1350) 是预先组装好的，但是很多成本更高，功能更少。就我个人而言，我认为 15 美元的控制器是一种不错的练习焊接的方式，不会冒太大的风险，如果你毁了它，但如果你不想冒这个险，可以先把几根电线焊接在一起。以下是一些可以引导你完成这一过程的指南:**

*   **[Adafruit 16 路伺服驱动器带 Arduino](https://learn.adafruit.com/16-channel-pwm-servo-driver/overview)T3】**
*   **优秀焊接指南**
*   **[伺服系统是如何工作的？](https://www.servocity.com/html/how_do_servos_work_.html#.VT65w_nBzRZ)T3】**

#### ****增加一个红外遥控器****

**红外(IR)遥控器看似简单(几乎可以方便地添加到任何 Arduino 项目中)。你所需要的就是 [一个传感器](https://www.adafruit.com/products/157) 和 [一个遥控器](https://www.adafruit.com/products/389) 。遥控器会向您的 Arduino 发送代码，然后您可以使用这些代码来触发命令。在这种情况下，你可以给你的机器人编程，让它开始移动，停止移动，或者移动到某个预先编程好的位置。已经有很多非常棒的代码可以在你的项目中使用。为了好玩，你甚至可以在你的电视遥控器上读取代码，如果你想的话，比如说，每当有人换频道时，让你的机器人活过来。以下是您开始工作所需的一些资源:**

*   **[如何使用红外遥控器搭配 Arduino](http://www.instructables.com/id/The-Easiest-Way-to-Use-Any-IR-Remote-with-Ardiuno/)**
*   **[Arduino 红外遥控教程](http://www.instructables.com/id/Arduino-Infrared-Remote-tutorial/)**
*   **[shiriff/Arduino-非远程库](https://github.com/shirriff/Arduino-IRremote)**

#### **使用 Wii 双截棍控制你的死亡机器**

 **[https://lifehacker.com/embed/inset/iframe?id=youtube-video-HbxhVs3UmuE&start=0](https://lifehacker.com/embed/inset/iframe?id=youtube-video-HbxhVs3UmuE&start=0)** 

**好吧，你想变得疯狂吗？看看上面的视频，展示了机器人手臂——和你做的模型一样！—被 Wii 双截棍控制。它使用 [这种分线适配器](https://www.adafruit.com/products/345) (你可以直接将双截棍插入其中)，并提供完全的操纵杆控制，这意味着你可以让它向任何你想要的方向移动，就像一个未来主义的木偶。如果你已经准备好使用这个指南进行这个项目，你可能是第十二次回来了，所以欢迎回来。这是我们在本文中包含的最高级的附加组件，所以如果它超出了您的理解范围，请不要难过。然而，它真的很酷。以下是一些可供进一步阅读的资源:**

*   **[Wii 双截棍转接适配器](https://www.adafruit.com/products/345)**
*   **[phenom optix meArm 的逆运动学控制库](https://github.com/yorkhackspace/meArm)**

**如你所知，机械臂项目涵盖了 Arduino 黑客场景中的大量概念和技能。如果你能完成这个项目而不被压垮或放弃，你可能会处理大多数 Arduino 项目 [我们定期推出](http://lifehacker.com/tag/arduino) 。开始可能看起来令人生畏，但是如果你一点一点地增加你的知识和经验，你可以建立一些非常棒的东西。**

**[Open *kinja-labs.com*](http://kinja-labs.com/related-widget/?posts=742869540,5875365,513094593&title=Check Out More Arduino Goodness)**