[![构建状态](https://github.com/DeadlyBossMods/DBM-MoP/workflows/CI/badge.svg)](https://github.com/DeadlyBossMods/DBM-MoP/actions?workflow=CI)
[![DeadlyBossMods 在 Discord 上](https://img.shields.io/badge/discord-DeadlyBossMods-738bd7.svg?style=flat)](https://discord.gg/DeadlyBossMods) 

<p><img src="http://mysticalos.com/images/DBM/support_on_patreon.png" width="408" height="80" /></p>
<p><a href="https://www.patreon.com/deadlybossmods">https://www.patreon.com/deadlybossmods</a></p>

Deadly Boss Mods: 语音包演示
============================

需求
----
在我们开始之前，你需要准备一些工具。

1. 一个合适的文本编辑器。（我在 Windows 上使用 Notepad++，在 Mac 上使用 Atom。）
2. 可以输出 ogg 文件的录音工具。可以是某些软件或物理录音设备，只要你能将你的声音转换为 ogg 格式即可。

就是这样。简单吧？

如何创建语音包
---------------

1. 将此包中的“DBM-VPDemo”文件夹复制到你的工作区。工作区是指另一个文件夹位置，以防你做错了什么事然后想要将整个东西恢复到初始状态。

2. 决定你想要使用的语音包名称，并将文件夹重命名为“DBM-VPYourPackName”。它必须以“DBM-VP”开头，区分大小写。

3. 进入文件夹并将文件“DBM-VPDemo.toc”重命名为与你刚才命名的文件夹相同的名称，所以应该为“DBM-VPYourPackName.toc”。不要意外地更改扩展名“.toc”。

4. 现在用文本编辑器打开你在步骤3中重命名的 toc 文件。
    1. 前三行是插件版本信息。除非未来魔兽世界大版本发布，否则无需修改它们。
    2. 第3行是你的语音包标题，将显示在魔兽世界插件列表中。所以只需将“Voicepack Demo”更改为“Voicepack YourPackName”。
    3. 第4和5行是标题的台湾和中文翻译。如果你不讲这些语言，直接删除这两行。或者如果你正在为其他语言制作，请在此添加你的语言。
    4. “RequiredDeps”，“DefaultState”不要修改。
    5. 将“Author: Iceoven”更改为“Author: YourName”。
    6. “Version”，通常从1.0开始（如果仍在alpha/beta状态则为0.1），并随着语音包的发展而增加。（注意：如果你在 Curse 发布，每次发布时请提高此数字，以便 Curse 客户端知道。）
    7. “X-DBM-Voice”不要修改。
    8. “X-DBM-Voice-Name”是在/dbm选项中显示的名字。
    9. “X-DBM-Voice-ShortName”应始终与“DBM-VP”之后的“YourPackName”匹配。所以在这个例子中，它是“DBM-VPDemo”中的“Demo”。
    10. “X-DBM-Voice-Version”如果需要，可能会随 DBM 版本更改。每次更新时请按照此示例中的值进行操作。
    11. “X-DBM-Voice-HasCount” 1 表示你有一个包含1-11个 .ogg 文件的“count”文件夹，否则为 0。
        完成。

5. 恭喜，现在唯一剩下的就是录制你的 ogg 文件。参见[此处](https://github.com/DeadlyBossMods/DBM-Voicepack-Demo/blob/master/DBM-VPDemo/!VoiceText.txt)了解文件名和我们使用的词语列表。
    1. 你可以搜索并找到你想要自定义的文件，或者简单地录制所有文件并替换现有文件。
    2. 进阶用法：如果你了解 Lua 和插件开发，你可以进入每个 DBM 模块并找到调用语音文件的位置，从而更好地理解它何时被触发。
