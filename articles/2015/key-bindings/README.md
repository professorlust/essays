聊聊vim，Emacs，Mac OS X与Intellij IDEA的键位绑定
===
如题，聊聊这些键位绑定，嗯，随便聊聊。

## 缘由
上个月的七夕，我从日亚海淘的HHKB键盘到手了。开箱即用，适应了一会之后，敲击体验非常之爽，感觉非常亲切，相见恨晚。第二天开始，就已经能够基本上适应全键盘操作了，除了系统设置和网页浏览这些应用主要还得依靠触控板。这个键盘最大的特点就是键位，**ESC**和**CONTROL**键位触手可及，也没有方向键（通过组合键可以达到目的），手腕无须移动，所有键位无远弗届（当然，两个下角的键位手腕不移动也并不是那么方便）非常适合操作。总之，我对这个键盘非常满意，甚至已经不习惯用自带的键盘了-_-#

既然是全键盘自然得熟悉操作系统的快捷键以及常用软件的快捷键，由此也引申出下面一些文字。

## vim
首先谈谈vim，这个被称作编辑器之神的东东。我是一个vimer，基本上所有的文本编辑都是在vim或其相关模式下的编辑器中完成的。vim对于键盘的利用可以说是达到了最大化，无需使用方向键，在命令模式下，几乎所有的的键都被拿来进行文本编辑操作，可以说是达到了文本处理效率的极致。vim的核心在于**模式编辑**，最关键在于熟记其键位映射，形成自己的第二反应后，文本编辑简直无往不利。

## Emacs与Mac OS X
Emacs，貌似被称作神的编辑器，是自由软件之父Stallman编写的（看过他用的键盘就是HHKB哦）。我不是Emacs的用户，也没有资格评论孰优孰劣，在这里只想谈谈它的键位绑定。稍微看了一下[Emacs键位绑定表][1]，发现Emacs有着相当多的绑定。她和vim最大的不同便是没有编辑模式，意味着要实现各种各样的文本编辑操作得使用相当多的辅助键位。比如说，vim在命令模式下，想要实现文本的编辑，只需要c，d，s，y，p等这些独立的字母键位，而Emacs则需要**CONTORL**，**OPTION**这些组合键。有人说，``Emacs = ESC + META + CONTROL + SHIFT``，这是有道理的。

接着说说Mac OS X，为什么要把这个系统和Emacs放在一块来谈谈呢？使用Mac已经两年多了，键位绑定或多或少都已熟悉。但是看了Emacs的键位绑定之后，才发现，OS X的一些键位绑定和Emacs居然是惊人的相似，尤其是以**CONTROL**作为组合键的时候，基本上是完全一致的。比如``^A``移动光标到行首，``^E``移动至行尾，``^D``向后删除等等。按照时间来看，Emacs无疑是先于OS X存在的，那么应该是OS X借鉴了Emacs的键位绑定了。后来[Google][2]了一下，果然如此，原来当年乔布斯离开Apple创办NeXTStep时，研发的操作系统便基于Unix。而在那个时候，Unix平台上对于程序员来说最强大的工具便是Emacs，NeXTStep的程序员非常熟悉Emacs，所以在实现操作系统时键位的绑定就借鉴了Emacs的。再后来，乔布斯回到了Apple，后面的事情你们都懂了。基本上，OS X上所有绑定**CONTROL**键位的文本操作快捷键都和Emacs保持一致，并且应用到了所有的应用程序中。比如在微信，qq，bash，iWork等等应用程序中，编辑文字时均可以使用这些键位绑定。详细的说明请参考苹果的[官方文档][3]。

那么这样一来，平台上所有的文本操作快捷键都统一了，熟练了之后对于效率有着不小的提升，简直是不能再好了。虽然这些键位不多，但是对于已经熟悉Emacs用户来说，简直是天作之合啊。另外，不管是OS X，还是Linux，默认的bash shell快捷键也是和Emacs一致的，简直了。我猜想，Emacs的键位设置和vim一样也是经过深思熟虑的并且得到了广大的程序员们认可的，不然也不至于整个操作系统的平台也都拿去借鉴。

至于为什么选用Emacs而不是vim的键位，我认为应该还是与模式编辑有关。这个从bash也可以设置vi模式看出来。bash默认是使用Emacs的键位的，但是你可以设置成vi的，``set -o vi``即可。然而，使用体验并不好。首先，你不确定处在什么模式之下，他不会像vi左下角有模式提示，默认情况下光标也没有变化；其次，命令一般就是输入一行，而且字符不会太多，体现不出vi在文本操作上的优势反而让人觉得模式切换的繁琐。相反，简明直接的Emacs快捷键更适合这种场合。btw，bash和vim基本上是给技术人用使用的。

大部分人并不懂得模式编辑，他们想要的就是一个输入的地方，他要输入，并且检查是否输入符合预期，否则就修改。我还记得第一次打开vim的时候，想输入，但是，噼里啪啦，按了几个键后屏幕都没有显示...对于不懂得vim的人来说，此刻他的内心是奔溃的。

计算机并不是技术人员的玩具。所以，基于Emacs的所见即所得的输入方式搭配其快捷键是更好的选择。这是Emacs的优势，会Emacs的同学可能觉得这系统简直是太亲切了，不会的同学也在某种程度上使用了Emacs，只是他不知道而已。然而，vim用户还是会使用vim，尽管整个大环境下都有Emacs的影子。

想到这里，我突然觉得，年轻的时候是不是选择Emacs更好一些，Stallman，Knuth（他曾经说敲击Emacs的键位就像弹奏乐曲一样）这些神的选择是有他的道理的，更不用说整个系统都有Emacs的影子了。也许以后我会尝试Emacs，但是现在，要谈谈Intellij IDEA了。

## Intellij IDEA
由于我的主要工作是Java与Android相关，离不开IDE。这里不讨论IDE与编辑器的好坏，也只是谈谈键位绑定。IDE集成了除编辑器之外的众多功能，所以有着相当多的键位绑定。我最开始用的是Eclipse配合eclim插件，那个时用得还是蛮爽的，但是在看到Intellj IDEA那些诱人丰富的细节功能，再加上在13年Goolge IO开始推出基于Intellij平台的Android Studio后，终于下定决心使用Intellij IDEA来开发。虽然IDEA本身提供了相当多套键位绑定使得从各种平台迁移到IDEA的同学更容易上手，比如Eclipse，Visual Studio的键位绑定，但是出于每个平台的键位绑定都有他的哲学，顺其自然可能更容易理解这个平台，就花了两三个晚上的时间熟悉新的键位绑定。说来也怪，感觉IDEA的键位是经过深思熟虑的，很快就适应了，并一直用到现在，非常爽。对于vim用户，自然少不了两个插件，一个是ideavim，另一个是relative number，基本上实现了绝大多数的vi键位，使用这两个插件会使得文本的编辑键步如飞！

IDEA默认就配备了Emacs键位，由于不是Emacs用户，所以没有去尝试。他在Mac上有着两套键位绑定，一个是[经典的键位][4]，另一个是更[通用的默认键位][5]。前者如前所述，和OS X系统更贴合，有Emacs的影子；后者由IDEA团队设计，有着跨平台的优势，在win，linux，mac之间键位基本上是相似的。本来还想尝试切换到经典的Mac键位，但是发现和vi的键位有太多的重合，使用起来很麻烦。再加上我已经熟悉了现有的键位，现有的键位设计得和ideavim的vi键位绑定几无重合，这套通用的键位绑定设计真的是g高瞻远瞩啊，既可以使用vi的键位，又可以使用其他众多的IDE键位，好棒！

## EOF
这篇文字花了几天时间写成，断断续续啰嗦了这么久，不知所云。最重要的是，找到自己喜欢的键位，提高工作效率的同时，留下更多的时间做自己喜欢的事情！

## One More Thing
很多时候我们需要调试API接口返回的JSON数据，有些时候我们需要把raw的JSON进行格式化方便查看。但是极少数情况，JSON字段是JSON字符串，这个时候格式化工具基本也就无能为力了！怎么样把JSON字符串转换为JSON呢，使用浏览器！

以Chrome为例，打开Developer Tools的Console标签，键入``var json = JSON.parse(your json string)``，即可将字符串转换为JSON对象，接下来再键入``JSON.stringify(json)``便可得到可格式化的字符串。

前几天调试时就遇到了这样的一个问题，某个字段里包含大量了JSON字符串，突然想到了现代的浏览器都带了__JSON.js__的，于是就用这种方式搞定了。

### EOF
```yaml
hide: false
license: cc-40-by
location: Shenzhen
summary: 不知所云。最重要的是，找到自己喜欢的键位，提高工作效率的同时，留下更多的时间做自己喜欢的事情！
tags:
- Equip
weather: ""
date: 2015-09-16T00:38:22+08:00
```


[1]: http://www.gnu.org/software/emacs/manual/html_node/emacs/Key-Bindings.html "Emacs Key Bindings"
[2]: http://apple.stackexchange.com/questions/76977/why-can-i-use-Emacs-shortcuts-in-many-os-x-programs "为什么我可以在OS X中使用很多Emacs的键位"
[3]: https://support.apple.com/en-us/HT201236 "Apple Key Bindings"
[4]: https://www.jetbrains.com/idea/docs/IntelliJIDEA_ReferenceCard_Mac.pdf "IDEA Mac Classic Key Bindings"
[5]: http://www.jetbrains.com/idea/docs/IntelliJIDEA_ReferenceCard.pdf "IDEA Default Key Bindings"

