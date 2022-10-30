# 用树莓皮制作一个动画 GIF 相框

> 原文:[https://life hacker . com/make-an-animated-gif-photo-frame-with-a-raspberry-pi-1658839211](https://lifehacker.com/make-an-animated-gif-photo-frame-with-a-raspberry-pi-1658839211)

Raspberry Pi 非常适合各种有趣而复杂的项目。对于愚蠢的项目来说也很棒，比如我这周做的这个动画 GIF 相框。以下是如何为自己制作一个。

Watch

### 你需要什么

这个项目不需要太多，但是你需要的不仅仅是一个树莓派来让它工作

*   [树莓派 B 型或者 b+](https://www.amazon.com/dp/B00LPESRUK?asc_campaign=InlineText&asc_refurl=https://lifehacker.com/make-an-animated-gif-photo-frame-with-a-raspberry-pi-1658839211&asc_source=&linkCode=ogi&psc=1&smid=AN9XFB4R34UOI&tag=kinjalifehackerlink-20&th=1)(A 中的 256MB 根本不够用)
*   [PiTFT 显示器](http://www.adafruit.com/products/1601) (任何显示器都可以，这个只是便宜又小)
*   USB 键盘(暂时，我用了一个 [迷你无线键盘](http://www.amazon.com/gp/product/B00556NMMW/ref=oh_aui_detailpage_o04_s00?asc_campaign=InlineText&asc_refurl=https://lifehacker.com/make-an-animated-gif-photo-frame-with-a-raspberry-pi-1658839211&asc_source=&ie=UTF8&psc=1&tag=kinjalifehackerlink-20) ，这样我就可以随时轻松地更改 gif 的网址)
*   sdcard
*   [Wi-Fi 适配器](http://www.amazon.com/Edimax-EW-7811Un-150Mbps-Raspberry-Supports/dp/B003MTTJOY/ref=sr_1_2?asc_campaign=InlineText&asc_refurl=https://lifehacker.com/make-an-animated-gif-photo-frame-with-a-raspberry-pi-1658839211&asc_source=&ie=UTF8&keywords=wifi adapter&qid=1415929958&sr=8-2&tag=kinjalifehackerlink-20)
*   电源适配器(如果你不想让难看的电线挂在墙上，你也可以买一个电池组)
*   (如果你想把它挂在墙上)
*   [一个廉价的相框](http://www.amazon.com/Pinnacle-Frames-Silver-Frame-Black/dp/B006020N9K/ref=sr_1_14?asc_campaign=InlineText&asc_refurl=https://lifehacker.com/make-an-animated-gif-photo-frame-with-a-raspberry-pi-1658839211&asc_source=&ie=UTF8&keywords=2x3 photo frames&qid=1415927518&sr=8-14&tag=kinjalifehackerlink-20)

### 第二步:挂上你的显示器

我走了非常懒惰的路线，买了已经焊接好 的 [PiTFT，准备出发。所以，你需要做的就是点击你的 Raspberry Pi 上的 GPIO。](http://www.adafruit.com/product/1601)

当它连接上后，继续启动 Raspbian。你将被要求校准触摸屏。按照屏幕上的指示操作，一切都准备好了。

### 第三步:安装铬合金

为了做到这一点，你需要一个全屏模式的网络浏览器。Chromium 的 [kiosk 模式](http://lifehacker.com/use-chromes-kiosk-mode-to-limit-someones-access-to-yo-1243433249) 非常适合这种情况。加载 LXTerminal 以进入 Raspbian 中的命令行。然后键入以下内容:

```
sudo apt-get install chromium
```

一旦下载完成，你就可以带着你的 GIF 机器进行测试了。我用 [Giphy TV](http://giphy.com/giphytv) 来提供 gif。键入:

```
chromium --kiosk tv.giphy.com/giphytrending
```

Chromium 现在应该会显示一些全屏的 gif。您可以将 URL 的`/giphytrending`部分更改为 Giphy 支持的任何搜索字符串，如`/science`、`/adhd`或`/cat`

当你确认它可以工作时，点击 Ctrl+F4 退出 kiosk 模式并返回命令行。

### 步骤 4:停止屏幕保护和节能功能

你可爱的小 GIF 相框已经启动并运行，但不幸的是，大约 10 分钟后，屏幕会变暗，你将看不到那些精彩的 GIF 照片。接下来，您需要禁用您的树莓 Pi 上的任何节能功能。在命令行中，键入:

```
sudo nano /etc/xdg/lxsession/LXDE/autostart 
```

这将加载文本编辑器。你要在这里做几件事。首先，通过在`@screensaver -no-splash`行前添加一个`#`来注释掉该行，如下所示:

```
# @xscreensaver -no-splash 
```

然后，在下面添加这几行:

```
@xset s off @xset -dpms @xset s noblank 
```

当你在那里的时候，你也可以让 Chromium 在开机时启动，以防你不小心拔掉了你的树莓派。在这一行中添加，插入您想要的任何 Giphy URL:

```
@chromium --noerrdialogs --kiosk tv.giphy.com/giphytrending 
```

这样，您的 Pi 将直接启动到 GIF 模式。

### **步骤 5(可选):将其安装到墙上**

最后，你只需要把你的树莓皮挂在墙上，并在它周围贴上一个框架。我用了几个 [命令图片挂条，就像这个](http://www.amazon.com/Command-Large-Picture-Hanging-Strips-4-Strip/dp/B00404YKZI/ref=sr_1_2?asc_campaign=InlineText&asc_refurl=https://lifehacker.com/make-an-animated-gif-photo-frame-with-a-raspberry-pi-1658839211&asc_source=&ie=UTF8&keywords=command hangers&qid=1415927107&sr=8-2&tag=kinjalifehackerlink-20) 这样我就可以在需要的时候轻松地把 Pi 从墙上取下来。然后，我去沃尔格林超市买了一个便宜的钱包大小的相框，剪下一些空间让圆周率的零件露出来，然后用胶带把它们粘在一起。我喜欢电子设备仍然可见，但如果你喜欢，你可以用垫子盖住它们。