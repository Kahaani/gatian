# 安装方法〔Windows〕

{% include "./common_header.md" %}

在 Windows 上安装潮语拼音输入法，有两大步骤：（1）安装小狼毫输入法；（2）添加潮语拼音的方案和码表。

## 安装小狼毫输入法

从 Rime 的官网下载“小狼毫输入法”。下面的截图来自版本 0.9.30，部分界面与最新版本略有差异。

> https://rime.im/download

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

点击桌面右下角的语言栏，切换到新增的输入法选项`小狼毫`。

![image-b1]

现在可以开始打字了。试着键入`han yu pin yin shu ru fa`，按空格键上屏。

![image-b2]

刚才输出的是繁体字。可以按`F4`或```Ctrl+` ```，唤出菜单，按`↑`和`↓`上下移动，按`PageUp`和`PageDown`前后翻页。第一页提供了基本选项，翻页后可以看到其他输入方案。这里选择`5`，切换到简化字模式。

![image-b3]

再次键入`han yu pin yin shu ru fa`，这回就是简化字了。

![image-b4]

小狼毫输入法还有很多功能，需要时可以查看官网的文档。

> https://rime.im/docs

## 添加潮语拼音的方案和码表

潮语拼音输入法支持 6 种口音，请任选一处链接，下载适合自己的口音版本。

> 百度网盘：https://pan.baidu.com/s/1kUJt5JL

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

接下来的几个步骤，要用到“开始”菜单中“小狼毫输入法”文件夹的三个选项，下面分步详述。

![image-c11]

首先，在开始菜单中，选择`【小狼毫】用户文件夹`，系统会打开一个文件夹。这个目录用于存放 Rime 的用户配置文件，我们把`schema.yaml`和`dict.yaml`两个文件放到该目录下。

![image-c3]

放好之后要告知小狼毫输入法。在开始菜单中，选择`【小狼毫】重新部署`。

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
汕头：su rip huak / su rik huak
澄海：su rik huak
饶平：su rip huap
揭阳：su rip huap
潮阳：su rip huap
```

![image-c9]

输入法支持用汉语拼音反查潮语拼音。比如不知道“朝”字怎么读，可以按 \` 键（在 Tab 键的上方），然后键入汉语拼音`chao`，就可以查到“朝”字的潮语拼音。

![image-c10]

[image-a1]: images/weasel/a1.jpg
[image-a2]: images/weasel/a2.jpg
[image-a3]: images/weasel/a3.jpg
[image-a4]: images/weasel/a4.jpg
[image-a5]: images/weasel/a5.jpg
[image-a6]: images/weasel/a6.jpg
[image-a7]: images/weasel/a7.jpg
[image-a8]: images/weasel/a8.jpg

[image-b1]: images/weasel/b1.jpg
[image-b2]: images/weasel/b2.jpg
[image-b3]: images/weasel/b3.jpg
[image-b4]: images/weasel/b4.jpg

[image-c1]: images/weasel/c1.jpg
[image-c2]: images/weasel/c2.jpg
[image-c3]: images/weasel/c3.jpg
[image-c4]: images/weasel/c4.jpg
[image-c5]: images/weasel/c5.jpg
[image-c6]: images/weasel/c6.jpg
[image-c7]: images/weasel/c7.jpg
[image-c8]: images/weasel/c8.jpg
[image-c9]: images/weasel/c9.jpg
[image-c10]: images/weasel/c10.jpg
[image-c11]: images/weasel/c11.jpg
