![img](https://luckly007.oss-cn-beijing.aliyuncs.com/images/20210226112340.png)



写这篇教程时间为2021年2月25日

最新版本3.9.2

中文文档：

https://docs.python.org/zh-cn/3/

每个编程语言的学习，第一个程序都是先向世界问好，Python 也不例外，这节我们先写下第一个 Python 程序 —— Hello World 。

# 一、Python 简介

Python 是著名的“龟叔” Guido van Rossum 在 1989 年圣诞节期间，为了打发无聊的圣诞节而编写的一个编程语言。牛人就是牛人，为了打发无聊时间竟然写了一个这么牛皮的编程语言。

现在，全世界差不多有 600 多种编程语言，但流行的编程语言也就那么 20 来种。不知道你有没有听说过 TIOBE 排行榜。

这是 2017 年 2 月编程语言排行榜 TOP20 榜单：

[![2 月编程语言排行榜 TOP20 榜单.png](https://camo.githubusercontent.com/e2bed835fc196afadcebf6dd20e721bbb934c8fa9df127f02484ba5c708fa59e/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30372d32322d3038303131382e6a7067)](https://camo.githubusercontent.com/e2bed835fc196afadcebf6dd20e721bbb934c8fa9df127f02484ba5c708fa59e/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30372d32322d3038303131382e6a7067)

还有就是 Top 10 编程语言 TIOBE 指数走势：

[![img](https://camo.githubusercontent.com/fc915932770d5c78a9be16ea7cd8a310f8c213f9b9eeb45ad046a687053df57f/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30372d32322d3038303134352e6a7067)](https://camo.githubusercontent.com/fc915932770d5c78a9be16ea7cd8a310f8c213f9b9eeb45ad046a687053df57f/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30372d32322d3038303134352e6a7067)

总的来说，这几种编程语言各有千秋，但不难看出，最近几年 Python 的发展非常的快，特别最近流行的机器学习，数据分析，更让 python 快速的发展起来。

Python 是高级编程语言，它有一个特点就是能快速的开发。Python 为我们提供了非常完善的基础代码库，覆盖了网络、文件、GUI、数据库、文本等大量内容，被形象地称作“内置电池（batteries included）”。用 Python 开发，许多功能不必从零编写，直接使用现成的即可。而且 Python 还能开发网站，多大型网站就是用 Python 开发的，例如 YouTube、Instagram，还有国内的豆瓣。很多大公司，包括 Google、Yahoo 等，甚至 NASA（美国航空航天局）都大量地使用 Python。

当然，任何编程语言有有点，也有缺点，Python 也不例外。那么 Python 有哪些缺点呢？

第一个缺点就是运行速度慢，和C程序相比非常慢，因为Python是解释型语言，你的代码在执行时会一行一行地翻译成CPU能理解的机器码，这个翻译过程非常耗时，所以很慢。而C程序是运行前直接编译成CPU能执行的机器码，所以非常快。

第二个缺点就是代码不能加密。如果要发布你的 Python 程序，实际上就是发布源代码。像 JAVA , C 这些编译型的语言，都没有这个问题，而解释型的语言，则必须把源码发布出去。

# 二、Python 的安装

因为 Python 是跨平台的，它可以运行在 Windows、Mac 和各种 Linux/Unix 系统上。目前，Python 有两个版本，一个是 2.x 版，一个是 3.x版，这两个版本是不兼容的。本草根安装的是 3.6.1 版本的。

至于在哪里下载，草根我建议大家最好直接官网下载，随时下载下来的都是最新版本。官网地址：https://www.python.org/

## 1、windows 系统下安装配置

如果是 windows 系统，下载完后，直接安装，不过这里记得勾上Add Python 3.6 to PATH，然后点 「Install Now」 即可完成安装。

这里要注意了，记得把「Add Python 3.9 to Path」勾上，勾上之后就不需要自己配置环境变量了，如果没勾上，就要自己手动配置。

![image-20210226134900993](https://gitee.com/itmxs/images/raw/master/20210226134901.png)

如果你一时手快，忘记了勾上 「Add Python 3.9 to Path」，那也不要紧，只需要手动配置一下环境变量就好了。

在命令提示框中 cmd 上输入 ：

```
path=%path%;C:\Python 
```

特别特别注意： `C:\Python` 是 Python 的安装目录，如果你的安装目录是其他地方，就得填上你对应的目录。

安装完成后，打开命令提示符窗口，敲入 python 后，出现下面的情况，证明 Python 安装成功了。

![image-20210226135000399](https://gitee.com/itmxs/images/raw/master/20210226135000.png)

而你看到提示符 `>>>` 就表示我们已经在 Python 交互式环境中了，可以输入任何 Python 代码，回车后会立刻得到执行结果。

## 2、Mac 系统下安装配置

MAC 系统一般都自带有 Python2.x 版本的环境，不过现在都不用 2.x 的版本了，所以建议你在 https://www.python.org/downloads/mac-osx/ 上下载最新版安装。

安装完成之后，如何配置环境变量呢？

先查看当前环境变量：

```
echo $PATH
```

然后打开 `~/.bash_profile(没有请新建)`

```
vi ~/.bash_profile
```

我装的是 Python3.7 ，Python 执行路径为：`/Library/Frameworks/Python. Framework/Versions/3.7/bin` 。于是写入

```
export PATH="/Library/Frameworks/Python. Framework/Versions/3.7/bin:$PATH"
```

[![img](https://camo.githubusercontent.com/bfb817d822bd0fdf413bd189580b2b21b5b023d2925e8361564aa743cccb2865/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30372d32322d3038343134392e706e67)](https://camo.githubusercontent.com/bfb817d822bd0fdf413bd189580b2b21b5b023d2925e8361564aa743cccb2865/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30372d32322d3038343134392e706e67)

最后保存退出，激活运行一下文件：

```
source ~/.bash_profile
```

# 三、第一个 Python 程序

好了，说了那么多，现在我们可以来写一下第一个 Python 程序了。

一开始写 Python 程序，个人不太建议用专门的工具来写，不方便熟悉语法，所以这里我先用 [VSCode](https://code.visualstudio.com/) 来写，后期可以改为用 PyCharm 。

第一个 Python 程序当然是打印 Hello Python 啦。

如果你没编程经验，什么都不懂，没关系，第一个 Python 程序，只要跟着做，留下个印象，尝试一下就好。

新建一个文件，命名为 `HelloPython.py` , 注意，这里是以 `.py` 为后缀的文件。

然后打开文件，输入 `print('Hello Python')`

[![img](https://camo.githubusercontent.com/83262e81d51e2e5f0ec173466063d233860d29522ea203b7fc7208b9545d16c5/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30382d31372d3037353934382e6a7067)](https://camo.githubusercontent.com/83262e81d51e2e5f0ec173466063d233860d29522ea203b7fc7208b9545d16c5/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30382d31372d3037353934382e6a7067)

最后就可以打开命令行窗口，把当前目录切换到 HelloPython.py 所在目录，就可以运行这个程序了，下面就是运行的结果。

[![img](https://camo.githubusercontent.com/2a25c6e6e6f13205dc0f12e4a7d8ac2e7a55bb803527b25224281f3858967f3c/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30382d31372d3037353935362e6a7067)](https://camo.githubusercontent.com/2a25c6e6e6f13205dc0f12e4a7d8ac2e7a55bb803527b25224281f3858967f3c/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30382d31372d3037353935362e6a7067)

当然，如果你是使用 [Sublime Text](http://www.sublimetext.com/) ，并且在安装 Python 的时候配置好了环境变量，直接按 Ctrl + B 就可以运行了，运行结果如下：

[![img](https://camo.githubusercontent.com/1b5485019ebcd0efd016b6f29d2c0ff0f6d8668fd0e47c137fcf80475eced8bd/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30382d31372d3038303031382e6a7067)](https://camo.githubusercontent.com/1b5485019ebcd0efd016b6f29d2c0ff0f6d8668fd0e47c137fcf80475eced8bd/687474703a2f2f74776f7761746572696d6167652e6f73732d636e2d6265696a696e672e616c6979756e63732e636f6d2f323031392d30382d31372d3038303031382e6a7067)

# 四、集成开发环境（IDE）: PyCharm

我本人一直是建议在学习周期使用文本编辑器或者是[VSCode](https://code.visualstudio.com/)  这个工具来写 Python 程序的，因为这样有利于我们了解整个流程。

当然，如果你有一定的编程基础，是可以使用集成的开发环境的，这样可以提高效率。这时，你可以选择 PyCharm ，PyCharm 是由 JetBrains 打造的一款 Python IDE，支持 macOS、 Windows、 Linux 系统。

PyCharm 下载地址 : https://www.jetbrains.com/pycharm/download/