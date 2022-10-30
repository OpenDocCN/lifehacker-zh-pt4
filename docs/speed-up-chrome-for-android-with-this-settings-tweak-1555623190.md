# 通过这一设置调整加速 Android 版 Chrome

> 原文：<https://lifehacker.com/speed-up-chrome-for-android-with-this-settings-tweak-1555623190>

Android: Chrome 是 [我们最喜欢的 Android 浏览器](https://lifehacker.com/five-best-android-web-browsers-5925969) 之一，但它有时会有点迟钝。多亏了 Redditor [红血球数量 64](http://www.reddit.com/user/erythrocytes64) ，这个设置调整可以给你一个相当快的速度提升，这取决于你的设备。

Watch

简而言之，你所做的是让 Chrome 获得更多的内存，并消除你上下滚动页面时的口吃。你所要做的就是在你的 Android 设备上打开一个新的 Chrome 标签，并把它粘贴到地址栏中:

`chrome://flags/#max-tiles-for-interest-area`

增加到 512。你的更改要等到下次 Chrome 重启后才会生效，但你会在底部看到一个写着“立即重启”的按钮。点击这个按钮，Chrome 就会关闭，然后重新打开。它应该比以前更快。我测试了这个调整，果然，我在我的 Moto X 上看到了更好的滚动和导航性能。它不会使页面加载更快，但肯定会使它们更容易浏览。

Reddit 帖子中的一些其他评论者指出，对于持怀疑态度的人来说，让 Chrome 获得更多内存意味着 Android 将更积极地关闭其他闲置应用程序，以确保 Chrome 拥有它需要的所有食物；因此，如果你使用的是旧设备或内置内存较少的设备，你可能希望从 256(默认为 128)开始，找到你的最佳点。不过，512 为我们工作。

红细胞 64 指出了其他一些也可能提高你的表现的标志:

> 其他(相对)有用的标志:
> 
> enable-offline-mode - AFAIK 允许在没有互联网连接的情况下访问存储在设备缓存中的页面。
> 
> 据 ElTimablo 报道，enable-spdy4a2 可能有助于在一些页面上显示更好的结果，特别是脸书，但其他人在使用它时遇到了故障。
> 
> enable-cast - only in beta“启用实验性 Chromecast 支持，允许在 Chromecast 设备上播放和控制网络视频。”

启用 SPDY/4 alpha 2 将会改善支持它的网站，比如脸书，但是你不会在其他地方看到太多的回报。您还可以启用“显示 fps 计数器”来查看您是否真的获得了调整所承诺的性能提升。点击下面的链接查看整个帖子。

[我如何加速我设备上的 Chrome 浏览器](http://www.reddit.com/r/Android/comments/21r0a6/how_i_sped_up_chrome_on_my_device/) | Reddit