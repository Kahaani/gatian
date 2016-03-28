# 安装方法〔Windows〕

{% include "./common_header.md" %}

在 Windows 上安装潮语拼音输入法，有两大步骤：（1）安装小狼毫输入法；（2）添加潮语拼音的方案和码表。

## 安装小狼毫输入法

从 Rime 的官网下载“小狼毫输入法”，最新版本是 0.9.30。不必下载“小狼毫拓展方案集”。

> http://rime.im/download

小狼毫输入法支持 Windows XP 和 Windows 7。在 Windows 8 和 Windows 10 下也可以使用，但存在兼容性问题，解决方法见下文。

![image-a1]

运行安装程序。输入法程序需要比较高的系统权限，如果被某些杀毒软件拦截，请允许放行。

![image-a2]

接下来是一系列的安装选项，可以不用修改。

![image-a3]

![image-a4]

安装后会弹出设定菜单，左边一栏列出了预设的输入方案，有各种常见的音码、形码输入法，还有粤语、吴语，甚至中古汉语的输入方案。其中“朙月拼音”就是全拼，下面以它为例。这项配置以后可以随时更改。

![image-a6]

选择界面风格，安装完毕。这个选项以后也可以更改。

![image-a7]

点击桌面右下角的语言栏，发现新增了两个选项：`小狼毫`和`小狼毫(TSF)`，这是 Windows 提供的两种输入法框架，下文会说明。这里先选择`小狼毫`。

![image-b1]

现在可以开始打字了。试着键入`han yu pin yin shu ru fa`，按回车键上屏。

![image-b2]

刚才输出的是繁体字。可以按`F4`或```Ctrl+` ```，唤出菜单，按`↑`和`↓`上下移动，按`PageUp`和`PageDown`前后翻页。第一页提供了基本选项，翻页后可以看到其他输入方案。这里选择`5`，切换到简化字模式。

![image-b3]

再次键入`han yu pin yin shu ru fa`，这回就是简化字了。

![image-b4]

小狼毫输入法还有很多功能，需要时可以查看官网的文档。

> http://rime.im/docs

## 添加潮语拼音的方案和码表

潮语拼音输入法支持 6 种口音，请任选一处链接，下载适合自己的口音版本。

> 百度网盘：http://pan.baidu.com/s/1kUJt5JL

各地的代号如下：

- 潮州：`dieziu`
- 汕头：`suantau`
- 澄海：`tenghai`
- 饶平：`riaupeng`
- 揭阳：`gekion`
- 潮阳：`dioion`

每个版本有两个文件，感兴趣的读者可以用任何一款文本编辑器查看其中的内容。

- 以`schema.yaml`结尾的文件定义了输入方案。
- 以`dict.yaml`结尾的文件定义了码表。

如果读者有兴趣，可以把 6 种版本同时添加到输入法，但是会增加后面的部署时间。建议第一次不要贪多，先选一个就好，这里以潮州音为例。

![image-c1]

打开文件浏览器，在地址栏输入`%appdata%\rime`，敲击回车键，系统会自动定向到合适的目录。比如在 Windows 7 下会跳转到`C:\Users\<username>\AppData\Roaming\Rime`。把`schema.yaml`和`dict.yaml`两个文件放到该目录下。

![image-c2]

![image-c3]

放好之后要告知小狼毫输入法。在开始菜单中，选择`【小狼毫】重新部署`。

![image-c4]

部署的速度取决于机器的性能，可能耗时几秒或几十秒。部署成功后没有提示信息，感兴趣的读者可以打开进程管理器，如果`WeaselDeploy.exe`进程消失了，说明部署过程结束。

![image-c5]

在开始菜单中，选择`【小狼毫】输入法设定`，唤出选项菜单。在左边一栏的最下方可以找到新增的“潮语拼音”，打勾选上。

![image-c6]

回到输入界面，按`F4`或```Ctrl+` ```唤出菜单，按`PageDown`翻页，切换到新增的“潮语拼音”。

![image-c7]

现在可以使用潮语拼音打字了。试着键入下列字符：

```
潮州：die ghv peng im
汕头：dio ghv peng im
澄海：die ghv peng ing
饶平：dio ghv peng im
揭阳：dio ghv peng im
潮阳：dio ghu peng im
```

![image-c8]

再试着键入下列字符。有些口音版本配置了模糊音规则，把`rip`打成`rik`，把`huap`打成`huak`也没有关系。

```
潮州：su rip huap / su rik huak
汕头：su rip huap / su rik huak
澄海：su rik huak
饶平：su rip huap
揭阳：su rip huap
潮阳：su rip huap
```

![image-c9]

输入法支持用汉语拼音反查潮语拼音。比如不知道“朝”字怎么读，可以按 \` 键（在 Tab 键的上方），然后键入汉语拼音`chao`，就可以查到“朝”字的潮语拼音。

![image-c10]

## 兼容性问题（Windows 8 和 10）

前面提到，安装小狼毫输入法之后，在语言栏会新增两个选项：`小狼毫`和`小狼毫(TSF)`。如果读者的系统是 Windows 8 或 10，我们建议在语言栏设置中把`小狼毫(TSF)`移除，只保留`小狼毫`。

这样子可以最大程度解决兼容性问题，在大多数场合下都可以正常使用，剩下的问题有：

- Office 软件：打开 Word 等软件时，如果文档处于保护状态，会弹出`小狼毫：服务进程启动不起来`。关掉弹框后，小狼毫输入法可以正常使用。
- Edge 浏览器：小狼毫输入法失效，不影响其他输入法的使用。
- 开始菜单的搜索栏：小狼毫输入法失效，不影响其他输入法的使用。

针对兼容性问题，Rime 的作者已经开发了一个新的框架，但目前处于试用阶段，尚未正式发布。

[image-a1]: http://ww1.sinaimg.cn/large/006mIeATjw1f2ai9l6mqyj30sg0lcwhd.jpg
[image-a2]: http://ww4.sinaimg.cn/large/006mIeATjw1f2ai9lmksdj30sg0lcn01.jpg
[image-a3]: http://ww4.sinaimg.cn/large/006mIeATjw1f2ai9mcrngj30sg0lcq6t.jpg
[image-a4]: http://ww4.sinaimg.cn/large/006mIeATjw1f2ai9msya4j30sg0lcwi7.jpg
[image-a5]: http://ww4.sinaimg.cn/large/006mIeATjw1f2ai9nloqkj30sg0lcwic.jpg
[image-a6]: http://ww4.sinaimg.cn/large/006mIeATjw1f2ai9o3rzqj30sg0lcn13.jpg
[image-a7]: http://ww1.sinaimg.cn/large/006mIeATjw1f2ai9ondg7j30sg0lcdjy.jpg
[image-a8]: http://ww3.sinaimg.cn/large/006mIeATjw1f2ai9p2lq0j30sg0lcwi2.jpg

[image-b1]: http://ww4.sinaimg.cn/large/006mIeATjw1f2aiempz48j30sg0lctaw.jpg
[image-b2]: http://ww3.sinaimg.cn/large/006mIeATjw1f2aien6s3sj30sg0lc76u.jpg
[image-b3]: http://ww4.sinaimg.cn/large/006mIeATjw1f2aienthpej30sg0lcgo5.jpg
[image-b4]: http://ww3.sinaimg.cn/large/006mIeATjw1f2aieo9qwoj30sg0lc0vc.jpg

[image-c1]: http://ww4.sinaimg.cn/large/006mIeATjw1f2aij8s6btj30sg0lc775.jpg
[image-c2]: http://ww4.sinaimg.cn/large/006mIeATjw1f2aij98ozyj30sg0lc77d.jpg
[image-c3]: http://ww2.sinaimg.cn/large/006mIeATjw1f2aij9qe5yj30sg0lcwjd.jpg
[image-c4]: http://ww4.sinaimg.cn/large/006mIeATjw1f2aija7gdjj30sg0lctca.jpg
[image-c5]: http://ww4.sinaimg.cn/large/006mIeATjw1f2aijasbf5j30sg0lcn17.jpg
[image-c6]: http://ww3.sinaimg.cn/large/006mIeATjw1f2aijbdxgij30sg0lcq5w.jpg
[image-c7]: http://ww3.sinaimg.cn/large/006mIeATjw1f2aijbv2u6j30sg0lc0vj.jpg
[image-c8]: http://ww2.sinaimg.cn/large/006mIeATjw1f2aijdze38j30sg0lcmzw.jpg
[image-c9]: http://ww3.sinaimg.cn/large/006mIeATjw1f2aijem663j30sg0lcdih.jpg
[image-c10]: http://ww1.sinaimg.cn/large/006mIeATjw1f2aijf2ylxj30sg0lc415.jpg
