#Linux 桌面玩家指南：01. 玩转 Linux 系统的方法论#

> **特别说明：**要在我的随笔后写评论的小伙伴们请注意了，我的博客开启了 MathJax 数学公式支持，MathJax 使用`$`标记数学公式的开始和结束。如果某条评论中出现了两个`$`，MathJax 会将两个`$`之间的内容按照数学公式进行排版，从而导致评论区格式混乱。如果大家的评论中用到了`$`，但是又不是为了使用数学公式，就请使用`\$`转义一下，谢谢。

##什么情况下适合玩 Linux 桌面##

我的这一个系列是讲 Linux 桌面的。Linux 系统开源、开放、稳定性强、软件丰富且性能颇高，在服务器领域占据了相当大的市场份额，但是在桌面领域，市场占有率还是非常低。我为什么把写作的重点放在 Linux 桌面呢？那是因为 Linux 服务器系统往往提供比较详细的文档，例如这个 [Ubuntu官方文档](https://help.ubuntu.com/)，而 Linux 桌面的文档和教程却相当缺乏，网上也只能找到一些零散的资料，这些资料往往内容陈旧，跟不上 Linux 桌面的发展，大部分又不能讲明白其背后的原理。所以我决定，将我多年使用 Linux 桌面的心得与体会拿出来与大家分享。喜欢的朋友请点赞。

什么情况下适合使用 Linux 桌面呢？首先，当然是程序员群体。这是由 Linux 特性决定的，不管怎么说，Linux 毕竟还是一个专家系统和玩家系统，它的门槛比较高，就算是有图形化的桌面环境，没有一定的基础也玩不转。而且就算是有基础懂电脑，也必须得要有一个爱折腾的心，否则，极容易走上从入门到放弃的道路。Linux 对普通用户门槛高，但是对程序员却相当友好。很多编程工具几乎都是开箱即用的，例如 C/C++、Python、Java 啥的，还有最流行的 LAMP 组合（Linux+Apache+MySQL+PHP），由于目前的 Linux 发行版都有维护很好的软件源，所以当需要某些编程工具的时候，一条`sudo apt-get install`命令就可以搞定整个工具链的安装。很多情况下，程序员的成果需要部署到服务器上运行，所以直接在和服务器同源的 Linux 系统下开发和测试，会更加方便。另外，Linux 系统中充斥着各种各样的微型语言，像正则表达式、Shell脚本、sed和awk、JavaScript、宏语言（tex、m4）、标记语言（Markdown、xml、css）等，这些语言会出现在使用 Linux 系统的整个过程中，通过这些语言，可以学到各种闪光的思想，熟练使用这些语言，可以极大地提高我们使用电脑的效率。

另外一个适合使用 Linux 桌面系统的人群就是装 B 犯，就像我这样的。虽然 Windows 系统好用，但是烂大街了不是吗？在大家都用 Windows 的时候，我突然掏出来一个装着 Linux 桌面的笔记本，是不是 B 格爆棚？多年前，我使用 Linux 系统是偏爱字符界面的。装 B 神器啊，不管是别人看起来还是自己看起来，都显得特别的高大上。当然，字符界面用起来那也是相当舒服的，不过只是曾经。为什么这么说呢，那是因为在 14 寸或 17 寸，分辨率限于 1024\*768 的时代，使用字符界面，字体不大不小，也没有刺眼的强光，眼睛看着非常舒服。可是，自从液晶屏、高分屏时代来临之后，这种舒服感就一去不复返了。原因何在？字太小。比如在我这个 15.6 寸 1920\*1080 的 Dell XPS 15 上，使用纯字符界面根本没法看，必须使用 15pt 到 16pt 的 Dejavu Sans Mono 字体，眼睛看着才舒服。现在网络上，仍然有很多人问怎么把 Linux 设置成启动后自动进入字符界面这样的问题，我很想告诉他们：拉倒吧，还是使用图形界面靠谱。对于确实没有图形界面的服务器系统，还是老老实实使用 ssh 远程连接吧。

在图形界面下，使用 gnome-terminal 依然可以模拟全字符界面，只要按一个 F11 键全屏即可。还可以设置为半透明背景，看起来更拉风。如下图，这个是用的 Vim，在我这一系列的后续随笔中，肯定会有一篇专门讲 Vim 的：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180828103227951-2130406079.png)

即使不是程序员，Linux 桌面也确实是可以用来工作的。写论文、做 PPT、讲课都不在话下，我已经用 Linux 桌面工作十几年了。我的笔记本电脑是 Dell XPS 15，系统是 Ubuntu 16.04，用的软件是 LibreOffice，不管是写论文，还是做 PPT 课件，或者连接到大屏幕上进行 PPT 展示，都毫无压力。而且，Linux 还可以切换工作区，我可以在一个工作区中全屏播放 PPT，然后按一个快捷键，就切换到另一个工作区，使用非播放状态的 LibreOffice 教别人怎么做 PPT。不得不承认，最好用的办公软件还是 Microsoft 的 Office 2016，但是在 Linux 下，只能使用 LibreOffice 或者 WPS。这几个办公软件我都用过，得益于我不怕困难的精神，不管使用哪款办公软件，我都能够圆满地完成我的工作。其实仔细想想，很多人使用 Word 时，也只是把它当成一个高配版的写字板，而 Excel 也只不过当成一个格子纸而已，并不一定需要最强功能的 Office 软件。至于更高级的数据处理需求，又怎么能够难得倒我们程序员呢，Python 和 Java 可不是吃素的。

在专业人士面前，使用 Linux 桌面也不掉价。我有个朋友，华科大的博士，南洋理工的博士后，目前在西班牙做研究。前段时间他回国，我们坐着聊了一聊。他做的是数值计算和数据可视化方面的研究，模拟肿瘤生长什么的，论文发了不少，其中有一个计算，据说使用 128 核的服务器跑了一个多月。我羡慕得不得了，这样的项目和资源，我是不可能接触到的，这辈子都不可能了。我要看他的成果，他掏出了 MacBook Pro，给我看他的论文。我们聊，用什么写论文啊？他说用 LaTeX。我说哎呀，LaTeX 我也会啊，不过基本不用，国内还是 Word 用得多。然后他给我演示 LaTeX，结果中文碰到困难了，说在国外做研究写论文，用的全是英文，没碰到中文的问题啊。这时，我掏出我的 Dell XPS 15，说你看你看，我用的 TexLive 全家桶，使用 XeLaTeX 引擎，直接支持 Unicode 字符集和 UTF-8 编码，中文不是问题，哦对了，你在国内写文章的话，还有六种字体少不了，分别是宋体、楷体、黑体、仿宋、隶书和幼圆，你需要借用一下。然后再聊用什么编辑工具，我说我用 TexWorks，他说他用 TexStudio，还一再强调 TeXStudio 好用。我说那好，我也装一个吧。然后`sudo aptitude install texstudio`，一条命令一分钟搞定。

这里我反复提到 Dell XPS 15，真的不是打广告，这款笔记本颜值真的是不输的，哪怕他用的是苹果。其实我使用的已经是几年前的产品了，等我有了钱，一定买一个最新款的带 4K 屏的 XPS 15，以证实我以前说的，只要屏幕分辨率够高，字体渲染就不是事儿。然后我和我朋友接着聊，聊到数值计算的语言，我说我主要用 Octave 和 Python，他说哎呀，Octave 我知道，就是那个和 Matlib 语法一模一样的开源版本吧，我说是呀，然后给他简单演示了一下。聊到数据可视化，他说他们用的是 NASA 出品的 ParaView，然后给我演示了一下。我说这玩意儿不错，要钱吗？他说不要钱，开源的。我说你等我一下，然后我`sudo aptitude search paraview`，一看，软件仓库中还真有，再然后，`sudo aptitude install paraview`，又是一条命令一分钟搞定。接着聊，我说你这论文中的图片不错啊，都是计算生成的吗？他说不全是，你看这个概念图，是我老板用 InkScape 画的。我说 InkScape 我也会用呃，不过没有你老板画得这么漂亮，你老板功力真深厚啊。接着给他展示了一下我系统中的 InkScape，虽然没有他老板用得好，但是比我朋友强，因为他根本不会用。我说除了 InkScape，我还会用 GIMP，P 图嘛，还是我们中国人强一点。

聊着聊着，他说你这本子不错啊，用的什么系统啊，怎么感觉比我的苹果还溜呢？我说是 Ubuntu，Linux 的一个发行版。他说 Linux 他知道，他们实验室虽然清一色的苹果，但是服务器上跑的是 Fedora。我笑了，Fedora 我多熟啊，虽然我和我的这个朋友之间，差了不止十个博士后的距离，但是 Linux 桌面系统让我收获了满满的优越感。

##Linux 桌面系统的特点和现状##

当然，Linux 桌面系统并不是百分之百的好，它还是有很多问题的，也还是有很多困难的。在很多方面，它真的还是比不过 Windows，特别是在现在 Windows 10 突飞猛进、新功能越来越多的情况下。但是 Linux 桌面绝对是一个值得一玩的系统。目前，Linux 桌面是个什么现状呢？

首先，我觉得 Linux 发行版分化严重。Linux 发行版太多了，什么 ElementaryOS、ArcLinux、LinuxMint、Ubuntu、Fedora、Deepin、Zorin-OS 不一而足。除了发行版的分化外，还有桌面环境的分化，最大的两家分别是 Gnome 和 KDE，除此之外，还有 Xfce、Cinnamon、LXDE 等，而 Gnome 又分 Gnome 3 和 Gnome 2，还有相当多的人，停留在 Gnome 2 的时代不愿意升级，还把 Gnome 3 批评得体无完肤。Ubuntu 一直到 17.10 之前，都是使用自己开发的 Unity 桌面，虽然漂亮，但是也是对 Linux 桌面的一种分化。然后，Ubuntu 突然宣布放弃 Unity 桌面，回归 Gnome 3，这也算是一件好事。现在，使用最新版的 Ubuntu 和最新版的 Fedora，终于没有太大的差别了，都是使用 Gnome 3 作为桌面，即使其界面风格不同，但是使用思路和美化思路是一样的。在以后的随笔中，我只使用 Ubuntu 进行截图和举例，除非对于某些问题需要其它版本进行对比。

其次，Linux 桌面默认图形界面不够美观。如果一个系统看起来不顺眼，估计大家是没有心情继续用下去的。安装之后看一眼再卸载这种事很多人也没少干。有字体问题、主题问题、桌面壁纸问题、显卡驱动问题等等。安装 Linux 系统后，必须得非常有耐心地进行设置和美化，才能将它变成一个用起来舒服的系统。在这一篇之后，我可能需要使用至少两篇的篇幅来讲 Linux 桌面的美化和字体，当然，还是使用最新的 Ubuntu 发行版。而且 Linux 桌面光靠社区的力量，进步太慢了，Gnome 3 都有好多年了吧。还有 Wayland，提出概念也有好多年了，到现在还不能算是百分百成熟。而微软的 Windows 10 近几年突飞猛进，功能越来越强大，界面越来越美观，Windows 10 下的 Linux 子系统有了，到我写这篇随笔的时候，Windows 10 也能支持多个工作区了。

最后，就是生产力工具并不是很容易找。前面说过，Linux 系统对程序员很友好。这个友好主要表现为编程语言多，开箱即用，但并不代表针对这些语言的 IDE 工具也完美。开源的工具虽多，但是比起 Microsoft 的宇宙最强 IDE——Visual Studio 来说，一个能打的都没有。Vim 虽好，但是也不可能靠这一个锤子敲遍全天下所有的钉子啊。很多时候，我不得不寻找闭源的、甚至是收费的商业软件来进行工作。例如，Eclipse 写 Java 是不错，但是对 JavaScript 的支持就太差了，直到 2016 年过了一半才支持到 ECMAScript 5 不说，还没有智能提示。好在微软出了个 Visual Studio Code，该编辑器使用 electron 开发，JavaScript 是它的母语，所以它对 JavaScript 的支持是很完美的。但是如果写 Python，用 VS Code 的话，智能提示就又不好了，所以，我不得不上 PyCharm，大家知道，JetBrains 的全家桶是要收费的。再例如，想找一个可视化的网页设计工具，开源领域像 Dreamweaver 这样的一个都没有，每次找工具，推荐的都是 BlueFish，而其实 BlueFish 最多只能算一个支持 HTML 语言和 CSS 语言的文本编辑器，一点所见即所得的功能都没有。

##我选择 Linux 系统的原则##

Linux 的发行版这么多、桌面环境也这么多，我们究竟应该选择哪一个呢？我选择的是 Ubuntu，在我写这篇随笔的时候，它的最新版本是 18.04，不过 18.10 快出来了。Ubuntu 已经放弃了 Unity 桌面，回归到 Gnome 3了。另外，我偶尔用一用 Fedora，目前最新的是 Fedora 28，估计 Fedora 29 也快出了，我选择的依然是 Gnome 3 版本。
 
是不是 Gnome 3 一定就是最优秀的呢？不一定。从美观的角度看，Gnome 3 不是最漂亮的，从功能的角度看，Gnome 3 也不是最强大的，从轻量级的角度看，Gnome 3 也不是运行速度最快的。那我为什么会选择它呢？我主要是从这样几个方面考虑。首先，市场占有率要大，这样，用这个版本的人就多，有问题也更容易被发现和修复。其次，要善于拥抱新技术、新观点，虽然 Gnome 2 的桌面可能用起来更顺手，某些程度上可能更漂亮，还可以使用 Compiz 进行美化和加速，但是我认为这在某些程度上也会造成 GUI 程序的分裂，改 GUI 主题的时候，既要考虑 GTK2，又要考虑 GTK3，如果整个系统都是 Gnome 3，底层库都是 GTK 3 的话，则整个系统会更加统一。我个人认为技术路线要专一，避免分化。再说，如果长期不能拥抱新技术的话，很容易落伍。

选择了 Gnome 3，就要去发掘它的优点。首先是在使用上，要充分了解 Gnome Shell 的特点和设计思路，熟记快捷键，知道按下 Super 键就可以唤出 OverView 界面，知道按下 Ctrl+Alt+↑ 或者 Ctrl+Alt+↓ 可以切换工作区，而且 Gnome 3 具有动态工作区的功能，当你把现有的工作区都占用的话，它会自动创建一个新的工作区。还要去 Gnome 3 的官网看一看，特别是开发者中心看一看文档，就会发现，Gnome Shell 桌面环境只是冰山露在水面上的一角，在界面之下，还有一个完整的技术链，除了 GTK，还有文件处理库、多媒体库、文档排版库、矢量绘图库、XML 和 XLST 解析库、Webkit2GTK 库等等。还有各种语言绑定，除了 C/C++，还可以使用 JavaScript、Python、Vala 等语言开发 GUI 程序。特别是 JavaScript 和 CSS，是我们编写 gnome-shell-extension 和 gnome-shell-theme 的重要工具。

再说一次，我主要使用的是 Ubuntu 的最新版本，偶尔使用 Fedora。到目前为止，它们的技术路线基本重合了，只有界面风格、软件包管理工具等少量差别了，在这两个发行版之间切换，基本不需要额外的学习成本。另外，这两个版本背后都有大公司支持，维护的软件仓库质量可靠。横向比较的话，可以了解不同流派 Linux 发行版的区别，纵向比较，可以了解不同年代的技术特点。例如，Fedora 是 Red Hat 公司支助的，新技术的试验场，版本更新快，和 Ubuntu 差不多都是每半年一个版本。而 Red Hat 公司的 Enterprise Linux 则追求稳定，更新很慢，约两年一个版本。Redhat Enterprise Linux 5 就是一个很老的版本，它在技术选型上和最新的 Fedora 就有很大的差别。

为了比较不同年代发行版、以及不同流派发行版在技术选型方面的差异，我同时安装了以下发行版。首先，是 CentOS 5.10，它代表的是比较老的 Redhat Enterprise Linux 发行版。这里需要说一下，Redhat Enterprise Linux 是商业版本，需要购买授权，而 CentOS 是它的社区复制版，可以免费使用，他们的内容是一样的。下图是CentOS 5.10:
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180828094738597-803209825.png)

下图是稍微新一点的 CentOS 6.11：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180828094745599-1415278747.png)

下图是最新的 CentOS 7：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180828094752215-258966624.png)

下图是最最新的 Fedora 28：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180828094809796-1557103318.png)

下图是 Ubuntu 18.04：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180827220628981-1032578469.png)

从上面几个图可以看出，越老的版本，其界面越丑。CentOS 7 的发布时间和 Fedora 21 的发布时间是差不多的，但是界面还是丑多了。只能说，Redhat Enterprise Linux 的重点还是服务器版本，根本就没有对桌面做任何美化，不管什么年代，总是把桌面环境做成一坨翔。

##玩转 Linux 系统的方法论##

前面说了，Linux 系统是一个具有一定门槛的专家系统，使用 Linux 还是有一定难度的。就算是有图形界面的桌面系统，也并不能完全消除这些障碍。在这里，我结合我自己多年使用 Linux 系统的经验，谈一谈玩转 Linux 系统的方法论。

###01、从教科书开始学习，但是要注意与时俱进###

如何使用 Linux 是一门比较系统的学问，所以教科书是很有必要看那么几本的。我最开始学习 Linux，是十几年前，那时天天抱着一本《Redhat Linux 9宝典》啃，看清楚哦，是 Linux 9，而不是 Enterprise Linux 9。从那个版本后，Redhat 开始发行 Enterprise Linux，每两年一个版本，现在已经到第 7 版了。我后来也相继买了不少 Linux 方面的书，如下图，是我书柜一角的照片：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180828101502000-45203758.png)

可以看到，那些书都是以第 5 版为蓝本进行讲解的。现在看来，这些内容应该过时了。目前市面上还有不少比较优秀的入门书籍，像《鸟哥的Linux私房菜馆》、《Linux就该这样学》，都能够与时俱进，它们都有针对 CentOS 7 的最新版。

除此之外，我再给大家推荐几本优秀的书籍。先看这两本：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180828101510637-1872802096.jpg)

这两本书重点讲的是全字符界面的 Linux，讲得特别好，特别系统。没有局限于哪一个特定的发行版，但是它里面讲的知识在每一个 Linux 发行版中都可以用到。对文件、用户、权限、Shell、管道这些知识讲得特别深入。就是通过这两本书，我学会了使用`man`命令。这两本书还包含一些我从未在别的 Linux 书籍中看到过的知识点，例如 tty。其实我们在使用键盘和屏幕操作 Linux 的时候，系统的响应模式是在不断变化的。有时，我们输入文字，马上可以得到回显，像输入命令的时候；有时，我们输入文字，完全没有回显，像输入密码的时候；有时，我们输入一行文字，按 Enter 键后，系统才执行我们的命令；有时，只要敲一个字符，不需要按 Enter，就会立即得到系统的响应，。以上这一切，都是由 tty 控制的。上面两本书，就讲到了 Linux 中的`stty`命令和 tty 编程。

除了教科书，我们还可以从 Linux 系统编程的角度去揣摩 Linux 系统的用法，所以下面几本书也值得读一读：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180828101517649-1740182049.jpg)

Linux 内核和内核模块的知识也很重要，也有助于我们对 Linux 桌面系统的理解。可以读一读下面这几本书：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180828101541549-579562338.jpg)

软件技术无时无刻不在进步，教科书上的知识也有过时的时候，所以我们一定要能够改变思想，拥抱新的变化。举几个常见的经典的例子。①如何使 Linux 系统开机后直接进入字符模式，不启动图形界面？教科书上的回答是：修改`/etc/inittab`文件，将运行级别更改为 3。然而，这个回答只适用于 Redhat Enterprise Linux 5 及之前的老版本，因为它们的 init 使用的是 SysVinit 程序，而最新的几个发行版，它们的 init 使用的是 systemd，所以，正确的做法是`sudo systemctl set-default multi-user.target`。②如何修改启动菜单，如何开启 Framebuffer，如何设置 Framebuffer 的分辨率？教科书上的回答是直接修改`/boot/menu.lst`文件。然而，新的发行版已经不再使用 Grub Legacy 了，而是使用 Grub2，在 Grub2 中，正确的做法是先修改`/etc/default/grub`文件，然后再使用`grub2-mkconfig`命令生成配置文件，Ubuntu 还提供了`update-grub`命令，更加方便。

还有字体的进步。从上面展示的图片可以看出，早期的 CentOS 5 中，字体发虚比较厉害，而且没有好的黑体字。在早期的 Linux 版本中，字体配置也很复杂。后来，好用的黑体字越来越多，先有 Droid Sans Fallback，再有文泉驿系列，现在又有思源黑体。而字体的配置，基本上也被 Fontconfig 这个软件包统一了。在后面的随笔中，我会有一篇专门讲 Linux 桌面中的字体配置，将 Linux 桌面打造成一个养眼的系统。

###02、使用一个命令时，要知道该命令属于哪个软件包###

使用 Linux 时，本质是通过运行 Linux 下的软件来完成工作的。要做什么，运行相应的命令就可以了。而相同的命令，有可能属于不同的软件包，不同的软件包，就会有不同的策略、不同的文档。所以，知道一个命令属于哪个软件包是我们要学会的基本功。

还是以前面提到的 init 程序为例进行讲解。先回顾一下 Linux 系统的启动过程：开机 → BIOS 启动 → BIOS 加载硬盘 MBR 中的 Grub → Grub 加载 Linux 内核和 initrd 镜像文件到内存中 → Grub 将控制权交给 Linux 内核，Linux 内核开始执行，进行初始化 → Linux 内核将控制权交给 init 程序 → init 程序负责启动后面的所有后台服务软件和前台界面软件。那么 init 程序怎么启动系统中那么多的服务和软件的呢？如果要增加开机启动的服务或者减少开机启动的服务应该怎么办呢？如果要停止某项服务或重启某项服务应该怎么办呢？这些功能取决于 init 所在的软件包提供的策略、脚本和命令行工具。所以知道 init 程序属于哪个软件包非常重要。

怎么找到一个程序属于哪个软件包呢？这个要因包管理软件而制宜。我上面介绍的系统可以分为两个流派，一个是 Red Hat 流派，包括 CentOS 和 Fedora，它们使用 rpm 包管理软件。一个是 Debian 流派，这里就是指 Ubuntu，它使用 dpkg 包管理软件。先看 CentOS 5，运行 `which init`可以看到 init 程序的路径是`/sbin/init`，然后使用`rpm -qf /sbin/init`命令，可以看到它所属的软件包是 SysVinit。这是一个非常经典的软件包，很多 Linux 教程上都会讲。回忆一下 RedHat EL 5 之前的系统，要让某个服务在系统启动时运行，我们需要把一些脚本文件放到`/etc/rc.d/init.d`目录中，然后在相应的`/etc/rc.d/rcX.d`目录中建立符号链接，并且这些脚本的命名还有讲究，脚本前的数字代表脚本启动或停止时的顺序什么的。同时，RedHat EL 5 之前的系统还提供了几个工具来简化我们的工作，它们是`service`命令和`chkconfig`命令。

到稍微新一点的 CentOS 6，用和前面完全相同的流程来了解一下 init 程序。运行`which init`，得到它的路径是`/usr/sbin/init`，再运行`rpm -qf /usr/sbin/init`，可以看到它所属的软件包是 upstart。在老一点的 Ubuntu 版本，例如 Ubuntu 14.04 中，init 也是属于`upstart`软件包。这个软件包相比 SysVinit 是有进步的，可以这么理解，在 SysVinit 时期，只能主动运行或停止服务脚本，而在 upstart 时期，可以通过捕捉硬件或内核发出的信号，动态地启动或停止服务脚本，而且这些服务在运行的时候，还可以发出信号，以便激活或停止其它的服务。upstart 教科书上讲得少，而且其管理工具往往设计得和 SysVinit 兼容，所以往往被学习 Linux 的人忽略。

在最新的 Ubuntu 18.04 和 Fedora 28 中，init 又属于哪个软件包呢？Fedora 28 是 Redhat 流派的，所以其考察方法同前。Ubuntu 使用 dpkg 包管理软件，其考察流程是这样的：运行`which init`，得到路径`/sbin/init`，再运行`dpkg -S /sbin/init`，得到其软件包是 systemd。从前面的截图可知，Fedora 28 的 init 程序也是属于 systemd。知道一个软件属于哪个软件包，我们才好做功课，不是吗？在这里，我们可以用搜索引擎搜 systemd 关键字，也可以在系统中使用`man systemd`查看它的文档。

通过文档可知，systemd 启动后，先根据`default.target`配置文件中的规则初始化系统。其实`default.target`是一个链接，如果它链接到`multi-user.target`，则启动字符界面，如果它链接到`graphical.target`，则启动图形界面。这个和传统的 SysVinit 中的运行级别有一定的相似性。systemd 中的 target 很多，它和传统的 SysVinit 中的运行级别对应关系如下：

| SysVinit中的运行级别 | systemd中的 target | 意义 |
|-------:|:------|:------|
| 0 | runlevel0.target, poweroff.target | 关闭系统。 |
| 1, s, single  | runlevel1.target, rescue.target | 单用户模式。 |
| 2, 4 | runlevel2.target, runlevel4.target, multi-user.target | 用户定义/域特定运行级别。默认等同于 3。|
| 3 | runlevel3.target, multi-user.target | 多用户，非图形化。用户可以通过多个控制台或网络登录。 |
| 5 | runlevel5.target, graphical.target | 多用户，图形化。通常为所有运行级别 3 的服务外加图形化登录。 |
| 6 | runlevel6.target, reboot.target | 重启。 |
| emergency | emergency.target | 紧急 Shell。 |

SysVinit 和 systemd 软件包都有管理系统服务的功能，但是它们提供的命令是不同的，其对比如下：

| SysVinit 命令 | Systemd 命令 | 意义 |
|:-------|:------|:------|
| service foo start | systemctl start foo.service | 用来启动一个服务 (并不会重启现有的)。 |
| service foo stop | systemctl stop foo.service | 用来停止一个服务 (并不会重启现有的)。 |
| service foo restart | systemctl restart foo.service | 用来停止并启动一个服务。 |
| service foo reload | systemctl reload foo.service | 当支持时，重新装载配置文件而不中断等待操作。 |
| service foo condrestart | systemctl condrestart foo.service | 如果服务正在运行那么重启它。 |
| service foo status | systemctl status foo.service | 汇报服务是否正在运行。 |
| ls /etc/rc.d/init.d/ | systemctl list-unit-files --type=service | 用来列出可以启动或停止的服务列表。 |
| chkconfig foo on | systemctl enable foo.service | 在下次启动时或满足其他触发条件时设置服务为启用。 |
| chkconfig foo off | systemctl disable foo.service | 在下次启动时或满足其他触发条件时设置服务为禁用。 |
| chkconfig foo | systemctl is-enabled foo.service | 用来检查一个服务在当前环境下被配置为启用还是禁用。 |
| chkconfig –list | systemctl list-unit-files --type=service | 输出在各个运行级别下服务的启用和禁用情况。 |
| chkconfig foo –list | ls /etc/systemd/system/\*.wants/foo.service | 用来列出该服务在哪些运行级别下启用和禁用。 |
| chkconfig foo –add | systemctl daemon-reload | 当您创建新服务文件或者变更设置时使用。 |
| telinit 3 | systemctl isolate multi-user.target | 改变至多用户运行级别。 |

在使用了 systemd 的系统中，电源管理也是由 systemd 接管的。systemd 电源管理的命令如下：

| 命令 | 操作 |
|:-----|:-----|
| systemctl reboot | 重启机器 |
| systemctl poweroff | 关机 |
| systemctl suspend | 挂起 |
| systemctl hibernate | 休眠 |
| systemctl hybrid-sleep | 混合休眠模式（同时休眠到硬盘并挂起） |

systemd 自带日志服务 journald，并且用二进制格式保存所有日志信息，用户使用`journalctl`命令来查看日志信息。

很多人可能非常想了解 systemd 在系统启动时启动了哪些服务？这些服务的启动顺序如何？每个服务启动花费了多少时间？如果单纯去查看 systemd 的文档和各个服务的脚本，是非常难以搞清楚以上问题的。幸好 systemd 提供了一个非常好的分析工具 systemd-analyze，它可以帮我们分析各个服务启动的顺序、时间等。这样运行该程序
```bash
systemd-analyze plot > init.svg
```
就可以以图形化的形式展示各服务启动的时间轴了，如下图：
![](http://images2015.cnblogs.com/blog/16576/201610/16576-20161010104459774-285353503.png)

###03、了解进程###

在前面，我讲到了 Linux 系统的启动过程，但是讲到 init 就噶然而止了。init 之后呢？我们的 Linux 桌面系统如此复杂，它又是由哪些软件组成的呢？这些软件之间是什么关系呢？谁先启动、谁后启动？谁管理谁？谁占用鼠标、键盘和显示器？要用好 Linux 桌面，这些关系最好都梳理清楚了，我们可以通过分析系统中的进程来回答以上问题。

了解系统中的进程，可以通过`ps`命令，`ps`命令具有很多不同的选项，我也是记不住的，但是没关系，使用`man ps`就可以查看它的文档。如果认真学过前面的教材，特别是编程手册的话，就会对进程的一些概念，例如，什么父进程、子进程、僵尸进程的概念，什么进程组、进程ID、组ID的概念，有更深刻的理解。使用`ps -ejH | less`命令的效果如下图：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830070554092-229869029.png)

另外一个命令`pstree`，可以显示系统中的进程树，如下图：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830070622138-433590063.png)

通过以上命令的输出，可以让我们对自己的系统有一个大概的了解。可以看到，有一些进程之间的关系是并列的，彼此之间没有父子关系，像系统中的各种服务进程。有一些进程具有严格的父子关系，像 systemd 就是所有其它进程的父进程，而且 systemd 的 PID 是 1。还可以看出，systemd 负责启动 GDM，GDM 负责启动 XServer 或 Wayland，GDM 也负责启动 Gnome Shell。通过这些信息，就可以大致分析出一个桌面系统由哪些组件组成，功力深厚的话，就可以自己定制 Linux 桌面系统。

说到 GDM，我就多谈几句。以前我使用 Linux 桌面的时候，总是有一个误区：认为只有 XServer 启动后，才能够访问到图形系统，否则只能访问字符界面。随着对 Linux 的认识逐步加深，才发现即使在 XServer 启动之前，图形界面也是无处不在的。例如，Grub 的系统启动菜单，可以是图形化的，还可以通过改背景和主题进行美化。再例如在 Linux 初始化过程中，有一个 PlyMouth 软件，可以直接通过内核的 DRM 模块访问图形硬件，从而显示一个图形化的启动界面和进度条，同理，PlyMouth 也是可以通过更改主题进行美化的。最后，当 Linux 初始化完成后，会给我们显示一个让我们登录的图形界面，这就是 DM（Display Manager），这个 DM 既是 XServer 的父进程，负责启动 XServer，又是一个 XClient，给出图形化的登录接口。登录成功后，它又是 Gnome Shell 的父进程，负责启动 Gnome Shell。我花了很长时间才理解什么是 DM （Display Manager，显示管理器），才把它和 Linux 桌面系统中的窗口管理器（Window Manager）区分开来。以前 Ubuntu 使用的 DM 是 lightdm，现在回归 Gnome 3 后，就统一使用 Gnome 的 GDM 了。我后面会有一篇随笔专讲 X Window，到时候再详细讲解 Display 的概念，理解了 Display，再理解 Display Manager 就不难了。还有，即使在纯字符界面下，也是可以使用 FrameBuffer 获得图形功能的，我后面也会有一篇随笔，专讲 Grub2、字符界面、FrameBuffer。

###04、学会查找和管理软件包###

前面提到了使用一个命令时，怎么找出这个命令属于哪个软件包，并针对该软件包进行学习。这里反过来，如果知道一个软件包的名字，我们应该怎样找到它、安装它，安装之后，怎么知道它安装到了文件系统中的什么地方，怎么知道这个软件包还提供哪些别的命令。

比较幸运的是，目前流行的 Linux 发行版都有比较好的软件包管理工具，而且有官方维护得比较好的软件仓库。例如，在 Ubuntu 中，可以使用 apt 来安装软件仓库中的软件包。我喜欢用 apt 更高层次的一个包装 aptitude，所以安装完系统后，我总是先使用`sudo apt-get install aptitude`安装 aptitude，以后统一使用 aptitude 管理软件包。如下图：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830070644326-547600852.png)

使用`sudo aptitude search`查找软件包，使用`sudo aptitude install`安装软件包，使用`sudo aptitude source`下载某个软件包的源代码，使用`sudo aptitude purge`删除软件包。在 RedHat 流派的 Linux 发行版中，也有专用的包管理软件，Fedora 21 之前是`yum`，之后是`dnf`。用法都是大同小异，我就不具体讲了。必要时可以使用`man dnf`查看它的文档。

安装某个软件包后，要能够找出文件都散落在系统中的哪些地方。可以使用`dpkg -L`命令来完成该工作。

###05、善于阅读软件的文档###

要善于阅读软件的文档。在 Linux 中，阅读文档非常方便，几乎所有命令，都可以使用`man`命令来查看它的命令行参数。同样，对于复杂的软件，使用`man`也可以学到非常系统的知识。如下图，我在学习 Bash 的时候，使用`man bash`命令阅读它的官方文档：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830071218918-1843178007.png)

我学习 FontConfig 的时候，也是靠`man fonts.conf`来学习关于字体配置的语法的，如下图：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830225825460-1243716136.png)

对于一些 GNU 提供的软件，有时提供的是 Info 格式的文档，可以使用`info`命令阅读。下面是我学习 Grub 时的截图，使用`info grub`就可以调出来。
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830071242768-814448944.png)

有时候，我也会找一些 PDF 格式的文档，把它们下载到手机中，空闲时间读一读，非常方便。[GNU Manuals Online](http://www.gnu.org/manual/manual.html) 就是一个不错的地方，我经常在里面找 PDF 格式的文档下载，GCC、Octave、Bash、Grub 的文档，这里都有。还有，当我安装完 TexLive 全家桶后，也有海量的 PDF 文档，对 LaTeX 有兴趣的朋友不妨读一读。

###06、必要时参考软件的源代码###

有时候，文档并不是万能的，像某些软件的文档不够完善啦，或者我们自己的需求超越了文档描述的范畴啦等情况。这时，我们可以直接参看软件的源代码，这就是开源系统的优势。源代码有各种各样的，有 C 语言的，也有 Bash 脚本语言的，还有 XML、CSS、JavaScript 的。这篇随笔的第一张截图，展示的就是使用 Vim 阅读 Linux 内核的源代码。

有些软件是编译好的，所以我们需要额外下载它的源代码包，下载源代码包可以使用`sudo aptitude source`命令。例如，在学习使用 OpenGL 的时候，必须使用 X Window 的 glx 扩展，但是 glx 的文档又语焉不详，怎么办呢？这时我就想到了 freeglut 这个库，可以参考一下这个库是如何实现的嘛。先使用`sudo aptitude search freeglut`搜一下，发现官方仓库里面确实有 freeglut，而且软件包的名字是 freeglut3，然后使用`sudo aptitude source freeglut3`命令就可以把它下载下来了。使用 Vim 阅读它的代码，我就不截图了。

需要注意的是，Linux 内核源代码是单独打包的，所以要下载 Linux 内核的源代码的话，需要使用`sudo aptitude install linux-source`命令。

Linux 系统中还有一些功能是由脚本提供支持的，这些软件的源代码读起来更加方便。例如，制作 initrd 镜像文件的工具就是 Bash 脚本，在 Ubuntu 系统中，它在文件系统中的位置是`/usr/sbin/mkinitramfs`，使用 Vim 就可以阅读，如下图：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830231519007-1480192326.png)

FontConfig 的配置文件是 XML 格式的，分别是`/etc/fonts/fonts.conf`文件和`/etc/fonts/conf.d/`目录下的所有文件。也可以直接使用 Vim 进行阅读和修改，如下图：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830231549270-1046786963.png)

最后，来看看 Gnome Shell 用来定义外观的 gnome-shell-theme 和 gnome-shell-extension。前者是 CSS 文件，后者是 JavaScript 程序。当然，这个 JavaScript 是专用于 Gnome 3 的 GJS，这里可以查看它的 wiki：[GJS: Javascript Bindings for Gnome](https://gitlab.gnome.org/GNOME/gjs/wikis/Home)

进入`/usr/share/gnome-shell`目录，可以看到这里有`theme`目录和`extensions`目录，分别看一下里面有哪些内容，如下图：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830230233290-1037494101.png)

使用`sudo vim /usr/share/gnome-shell/theme/gnome-shell.css`命令，可以查看这个  CSS 文件，如下图：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830230303319-2011143389.png)

最后再来学习一下 Gnome Shell 的扩展怎么写，这里选择一个最简单的 Hide Activities，就是掩藏左上角的那个“活动”按钮。进入`/usr/share/gnome-shell/extensions/Hide_Activities@shay.shayel.org`目录，使用 Vim 查看 extension.js，如下图：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180830230333212-640561048.png)

可以看到，这个 Extension 非常的简单，其中的`function enable()`和`function disable()`是一个 Extension 最基本的框架，而且它也只是调用了`indicator.container.hide()`和`indicator.container.show()`方法。我们可以先学这个简单的 Extension，再学别的复杂一点的 Extension，再结合 GJS 的 wiki 和 GTK 的文档，很容易就可以学会怎么编写 Gnome Shell 的 Extension。

###07、严重问题可查看 Log###

这个就属于比较高级的技巧了，主要在出现严重问题的时候用。例如，图形界面启动不了啊、系统崩溃啊之类的，实在找不到原因了，就去看看这些软件输出的 Log。这种事情我也不是经常碰到。所以这里就不深入展开了。

##总结##

玩转 Linux 系统的方法论，主要包含以下内容：

1. 从教科书开始学习，但是要注意与时俱进。
多读书，系统学习 Linux 的基础知识。多思考，想明白命令背后的根本原理。多实践，紧跟最新的 Linux 发行版不掉队。
2. 使用一个命令时，要知道该命令属于什么软件包
充分认识到 Linux 的功能是由众多的软件构建起来的。使用一个命令时，要知道这个命令属于什么软件包，再用软件包的名称作为关键字去做功课。需使用到`which`和`dpkg -S`。
3. 了解进程。
使用`ps`命令和`pstree`命令查看进程和进程之间的关系。通过系统中有哪些进程及这些进程之间的管理来分析复杂系统的构成。
4. 学会查找和管理软件包
充分利用 Linux 发行版官方维护的软件仓库。使用`sudo aptitude search`查找软件包，使用`sudo aptitude install`安装软件包，使用`dpkg -L`命令查看软件包安装后散落在文件系统的什么位置。
5. 善于阅读软件的文档
遇到困难记得使用`man`、`info`等命令。空闲时间可以利用手机阅读 PDF 格式的文档进行学习。
6. 必要时参考软件的源代码
编译过的软件包，可以使用`sudo aptitude source`命令下载源代码。脚本语言或标记语言编写的软件，可直接阅读它的代码。
7. 严重问题可查看Log
高级技巧，我也没用过几回。图形系统启动不了或者系统崩溃的时候用。

##求打赏##

我对这次写的这个系列要求是非常高的：首先内容要有意义、够充实，信息量要足够丰富；其次是每一个知识点要讲透彻，不能模棱两可含糊不清；最后是包含丰富的截图，让那些不想装 Linux 系统的朋友们也可以领略到 Linux 桌面的风采。如果我的努力得到大家的认可，可以扫下面的二维码打赏一下：
![](https://images2018.cnblogs.com/blog/16576/201808/16576-20180831154735325-1276475036.png)

##版权申明##

该随笔由京山游侠在2018年09月03日发布于博客园，引用请注明出处，转载或出版请联系博主。QQ邮箱：1841079@qq.com
