# 重装系统备忘录
最近一段时间电脑总是正用着突然出现电脑卡顿，半天没反应，甚至蓝屏或者司机，之前从没想到可能是硬盘出问题，直到前两天启动不了了系统，以为系统坏了，就重装了系统，谁知昨天直接就找不到硬盘了，即使进入BIOS里也找不到了，查了下看来很有可能是固态硬盘的掉盘问题，硬盘有问题了。还好在第一次重装系统的时候把数据都移出来了（其实还有个ubuntu，里面也有些文件没有移出来，不过应该不是很重要）。通过京东申请了售后，发现硬盘过了三年质保，没办法只能再买一个了，昨晚下单了一个金士顿的A2000 nvme 500G的，今天送到后开始着手安装。
## Windows 10的安装
首先再msdn.itellyou.cn上下载了最新的win10专业版的iso，然后用老白桃U盘PE系统做了一个系统盘，之后通过PE系统进行了安装。

这里需要注意的地方是对于win10这样的系统，需要一个ESP引导分区，而这个需要分区表从传统的MBR改为GPT。

之后给Windows系统分类300G空间。安装就不细说了，下面说一下安装后做的事情。
### 激活
这里用了一个cmd脚本（MAS_1.0_CRC32_1D90323C.cmd）非常棒，一次就成功了。

### 迅雷
为了快速的下载下面要安装的软件，就先下载了这个。
### WPS
本来我一般是不安装这个的，工作原因，急需，就装了这个校园版，感觉一般用途非常不错，支持国产。
### 微信客户端
工作需要直接就安装了
### Everything
已经是必需品了
### 7-Zip
也已经是必需品了
### Chrome
这个直接下载安装程序然后直接装就可以了，但是奇怪的是每次我安装的都是繁体版本的。

装好后，进入设置-高级-语言-语言-添加语言-中文简体-设为以这种语言显示就可以了。关键是怎么登陆我的Google账户同步之前安装的扩展，关键是SwitchyOmega，用来爬墙。但是这里有一个悖论，登录Google需要爬墙。爬墙现在我用的是Trojan，目前看来还算好，这个目前已经设置好了，关于这个以后有时间再讲，关键是Trojan用的是Socks5代理，Win10系统自带没法设置，需要借助外界的，这里我用的是V2Ray。
### V2RayN
下载最新版的V2RayN[https://github.com/2dust/v2rayN/releases/download/3.19/v2rayN-Core.zip](https://github.com/2dust/v2rayN/releases/download/3.19/v2rayN-Core.zip),使用V2Ray建立全局Socks5代理。
* 下载后解压缩，然后运行v2rayN.exe
* 选择服务器-添加[Socks]服务器
* 服务器地址填127.0.0.1，服务区端口填1070
* v2rayN图标上点右键-Http代理-选择全局模式
然后就可以爬墙了，这个时候就可以同步Chrome了。

V2rayN的作用也结束了。
### Xshell，Xshell，Xftp
工作用，看到官网上有测试版，测试版不需要购买，就先用了。

### Office
正式用还得用这个。
这次安装使用了[Office Tool Plus](https://otp.landian.vip/zh-cn/download.html)这个软件，非常不错。
参考这个（[https://www.jianshu.com/p/3d1fffd0bdb2](https://www.jianshu.com/p/3d1fffd0bdb2)）安装教程。
* 选择部署
* 增加产品-选择Office专业增强版2019-批量版
* 语言包为简体中文
* 体系结构：x64-通道：Office2019企业长期版-安装方式：在线安装-安装模块：Office部署工具
* 看到下面又iSlide，以前没用过，搜了下感觉不错，也选上了
#### 开始部署
然后就开始下载安装了，速度很快，应该不到20分钟
之后就可以激活了
#### 激活
* 选择激活
* 选择许可证：ProPlus2019Volume
* 安装许可证
* KMS管理：选择kms.03k.org
* 激活成功
**成功**
### VSC
为了查看一些文本文档，所以安装了这个软件。
但是下载安装后发现界面是英文的。
按照以下办法切换为中文
* Ctrl+Shift+P
* 输入configure display language
* 点击 Add language
* 安装简体中文
* 重启即可
### 百度网盘
为了下载MaterialsStudio
### MaterialsStudio2019
为了构造模型方便
#### 激活
* 安装时候到configure license，勾去掉
* 修改ms2019.lic第一行，替换this_host为计算机名
* 复制许可证文件ms2019.lic到如下路径中（默认路径）
> C:\Program Files (x86)\BIOVIA\LicensePack\Licenses\
> C:\Program Files (x86)\BIOVIA\LicensePack\share\data\
> C:\Program Files (x86)\BIOVIA\LicensePack\win32\bin\

### Oringlab
画图Origin还是少不了，以前一直用的破解的，想着现在新装系统了，看看有没有最新的，搜了下普遍的是2019b，但是看到很多人说这个破解版本很不稳定，经常崩溃。

同时搜到的过程中发现origin近些年也变化很大，版本更新很快，还有了官方中文版，甚至Originlab为中国学生提供了[免费半年的学习版](https://my.originlab.com/forum/topic.asp?TOPIC_ID=22328)，只要有edu邮箱就可以，这个不错。

跟着步骤申请下来，然后邮箱里就会收到一封邮件，里面包括：
* 一个百度网盘链接，包含最新版的orgin
* 一个序列号
* 一个激活码
然后下载安装，安装过程中输入序列号，安装完打开的时候会提示输入激活码。

安装正版的感觉还是不错的，如果origin不贵的话，还真想用正版的。

### QQ
QQ还是少不了的，直接下载安装即可。

### Virtual NanoLab 2017.2
这个是ATK的图形化界面，不过这个建模型也是非常方便的。

不过不爽的是，之前VNL的license是可以免费申请的，2016版的时候申请了，2017的又不能用了，但2017的我没有申请，后来ATK被收购了，没法免费申请了。之前学院购买了ATK，买了两年的更新授权，但是ATK那边说我们买的是浮动授权，没法给独立的授权。所以现在装上去了，没有授权，没法用。气愤！

### DeviceStudio 2020A
这个是鸿之微公司开发的一款建模软件，也不错

### 企业微信
工作所需

### 搜狗拼音输入法 智慧版3.0
开始用的微软自带的，用一段后还是装了搜狗输入法，习惯了。

### Teamviewer
远程协助朋友解决一些问题，还是这个更方便些。

### 钉钉
上网课，工作所需

### Zotero
之前管理文献主要用Endnote，这次重装系统后又需要装，就去找最新版的破解的，突然觉得不想折腾了，之前也接触过Zotero，免费开源，有很多插件，还支持Webdav，可以方便的存储文献，因此决定就用这个了。

不过用这个还是需要折腾一下，之前的都是Endnote，需要把文献导入到Zotero里。这次我是用的是通过Everything搜索Endnote的存储目录里的所有pdf文件，然后通过导入pdf功能全部导入到Zotero，然后再获取pdf元数据建立。

因为原来的pdf有上千个，所以获取元数据的时间有点长，现在还在获取。获取完之后再更新如何设置Webdav以及重命名pdf文件方面的信息。

### Keepass
进行密码管理的软件，随着年龄增大，记忆力越来越比不过从前了，在登录各种网站的时候发现有些密码经常忘记，因此想起来了进行密码管理。

很多年前的时候曾经用过一段时间，后来没继续用。在进行Zotero的Webdav的时候，登陆了以前注册的box.net的账户，竟然发现了2012年的keepass文件，因此下载了keepass，然后导入了，还好记得以前设置的密码。

不过在搜索密码管理的过程中，发现现在有一些更好的，在线的密码管理方法，经过选择，使用了lastpass

### lastpass
这个软件可以在线使用，支持Chrome插件，功能很强大，因此决定现在是用这个。

### Vesta
查看晶体结构3D模型以及电荷密度处理等所需。

### PDF.XChange.EditorPlus.7Portable_x64
看PDF用。


## Manjaro 20.0.3
之前的系统是win10+ubuntu18.04，听说现在manjaro成第一流行的发行版了，基于archlinux，之前玩过一阵archlinux，确实挺不一样的，archlinux的AUR非常丰富，安装软件比较方便，因此决定安装这个发行版玩玩。

这个发行版据说kde的界面最漂亮，很久没用过kde的了，之前一直是GNOME。参考这篇教程[https://www.cnblogs.com/HGNET/p/12712977.html](https://www.cnblogs.com/HGNET/p/12712977.html)
- 首先下载[安装镜像](https://manjaro.org/download/)
- 然后下载rufus，记得下载低版本的，现在的版本，3.11的没法选择分区类型。我下载的是3.5p免安装版
- 选择GPT，DD模式写入镜像
- 之后使用U盘启动进行安装
- 我建了三个分区，/分区，swap分区和/boot/efi分区，记住/boot/efi分区要和win10的ESP分区是同一个分区
