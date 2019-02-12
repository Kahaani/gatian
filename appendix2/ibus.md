# 安装方法〔Linux〕

{% include "./common_header.md" %}

Rime 在 Linux 的两种输入法平台（IBus 和 Fcitx）上都有实现，下面以 Ubuntu 上的 ibus-rime 为例。分为两大步骤：（1）安装 ibus-rime；（2）添加潮语拼音的方案和码表。

## 安装 ibus-rime

在 Ubuntu (>= 12.10) 上，可以通过下面的命令安装 ibus-rime。

```
sudo apt-get install ibus-rime
```

默认预装有“朙月拼音”和“倉頡五代”两种输入方案，用户可以根据需要安装其他输入方案，具体请参考下面这份官方说明。其他 Linux 发行版的安装也请参考这份说明。

> https://github.com/rime/home/wiki/RimeWithIBus

安装完毕后，请将 ibus-rime 添加到语言栏的菜单中，并且切换到 Rime 输入法。

![image-a1]

现在可以开始打字了。试着键入`han yu pin yin shu ru fa`，按空格键上屏。

![image-a2]

刚才输出的是繁体字。按`F4`或```Ctrl+` ```唤出菜单，选择`漢字->汉字`，切换到简化字模式。

![image-a3]

再次键入`han yu pin yin shu ru fa`，这回就是简化字了。

![image-a4]

Rime 输入法还有很多功能，需要时可以查看官网的文档。

> https://rime.im/docs

## 添加潮语拼音的方案和码表

潮语拼音输入法支持 6 种口音，请从下列链接，下载适合自己的口音版本。

> 百度网盘：https://pan.baidu.com/s/1kUJt5JL

各地的代号如下：

- 潮州：`dieziu`
- 汕头：`suantau`
- 澄海：`tenghai`
- 饶平：`riaupeng`
- 揭阳：`gekion`
- 潮阳：`dioion`

每个版本有两个文件，不需要作修改。感兴趣的读者可以用任何一款文本编辑器查看其中的内容。

- 以`schema.yaml`结尾的文件定义了输入方案。
- 以`dict.yaml`结尾的文件定义了码表。

除此之外，还要下载`default.custom.yaml`文件。用文本编辑器打开这个文件，把不需要的输入方案删去，保留自己想要的。其中，“朙月拼音”就是全拼，建议保留。

如果读者有兴趣，可以把 6 种口音同时添加到输入法，但是会增加后面的部署时间。建议第一次不要贪多，先选一个就好。这里以潮州音为例，修改后的`default.custom.yaml`文件如下所示。

```
patch:
  schema_list:
    - schema: luna_pinyin    # 朙月拼音
    - schema: dieziu         # 潮語拼音·潮州
```

接下来，打开文件夹`~/.config/ibus/rime/`（0.9.1 以下版本为`~/.ibus/rime/`），这个目录用于存放 Rime 的用户配置文件，我们把刚才的三个文件放到该目录下。

```
dieziu.schema.yaml
dieziu.dict.yaml
default.custom.yaml
```

放好之后要告知 Rime 输入法。在语言栏菜单中，点击 ⟲ (Deploy) 按钮。部署的速度取决于机器的性能，可能耗时几秒或几十秒，部署成功后会有提示信息。

![image-b1]

如果找不到 ⟲ 按钮，也可以运行下面命令，会触发“重新部署”。

```
rm ~/.config/ibus/rime/default.yaml; ibus-daemon -drx
```

回到输入界面，按`F4`或```Ctrl+` ```唤出菜单，切换到新增的“潮语拼音”。

![image-b2]

现在可以使用潮语拼音打字了。试着键入下列字符：

```
潮州：die ghv peng im
汕头：dio ghv peng im
澄海：die ghv peng ing
饶平：dio ghv peng im
揭阳：dio ghv peng im
潮阳：dio ghu peng im
```

![image-b3]

再试着键入下列字符。有些口音版本配置了模糊音规则，把`rip`打成`rik`，把`huap`打成`huak`也没有关系。

```
潮州：su rip huap / su rik huak
汕头：su rip huak / su rik huak
澄海：su rik huak
饶平：su rip huap
揭阳：su rip huap
潮阳：su rip huap
```

![image-b4]

输入法支持用汉语拼音反查潮语拼音。比如不知道“朝”字怎么读，可以按 \` 键（在 Tab 键的上方），然后键入汉语拼音`chao`，就可以查到“朝”字的潮语拼音。

![image-b5]

[image-a1]: https://ww1.sinaimg.cn/large/006mIeATgw1f3w2sk9mixj30dw0b4wer.jpg
[image-a2]: https://ww2.sinaimg.cn/large/006mIeATgw1f3w2skoehbj30dw0b474q.jpg
[image-a3]: https://ww2.sinaimg.cn/large/006mIeATgw1f3w2slew6nj30dw0b4mxl.jpg
[image-a4]: https://ww2.sinaimg.cn/large/006mIeATgw1f3w2sm4khpj30dw0b4dge.jpg

[image-b1]: https://ww4.sinaimg.cn/large/006mIeATgw1f3w2sn2efdj30dw0b40t0.jpg
[image-b2]: https://ww1.sinaimg.cn/large/006mIeATgw1f3w2snhiscj30dw0b40tb.jpg
[image-b3]: https://ww3.sinaimg.cn/large/006mIeATgw1f3w2snz5v4j30dw0b4js4.jpg
[image-b4]: https://ww1.sinaimg.cn/large/006mIeATgw1f3w2sokg8kj30dw0b4mxv.jpg
[image-b5]: https://ww3.sinaimg.cn/large/006mIeATgw1f3w2sp37a4j30dw0b4q3o.jpg
