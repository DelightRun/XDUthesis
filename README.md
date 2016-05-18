# XDUthesis 西安电子科技大学学位论文模板
---
Xidian University thesis template
---
## v0.1.6 版本更新，详情如下：
- 修正目录中章的索引符为空问题，修正为点。感谢 [git4xuan](https://github.com/git4xuan) 同学。
- 修正章节标题错误加粗问题 By [XDXX](https://github.com/XDXX) 同学。
- 修该原来图表编号后冒号为大空格，符合工作手册的样例。感谢 [git4xuan](https://github.com/git4xuan) 同学。
- 其他若干问题修复。
### 关于参考文献使用的解释
[git4xuan](https://github.com/git4xuan) 同学在 issues 里面提到了一些关于参考文献的疑问，个人觉得很有意义。但是有些没有在工作手册中找到相关规定。不敢直接进行修改。特在此说明一下。

对于参考文献样式，本模板提供了XDUbib.bst样式，以及对应不排序的样式。个人以为基本符合工作手册要求。如有同学觉得有问题，可以参考齐飞老师的模板使用IEEEtran的参考文献样式。使用方法，将Demo.tex文件里的

	\bibliographystyle{XDUbibunsrt}

代码修改为

	\bibliographystyle{IEEEtran}

即可。
### 关于封面以及诚信说明书
模板里自动生成的封面以及诚信声明书不具有权威价值，暂时仅供展示，大家以学校教务处官方提供的表格为准。下载地址：[http://sjjx.xidian.edu.cn/down/html/?26.html](http://sjjx.xidian.edu.cn/down/html/?26.html)

## v0.1.5 版本更新，详情如下：

- 首先，添加页面边距的装订线距离（之前忽略了，汗-_-||）

- 添加了新参数 `WordOneHalf` 可选参数，可将行距设置为Word版同等高度

	在本次更新中，设置为了默认选上了，详情 Main.tex 文件。

- 新添加不排序的参考文献样式 `XDUbibunsrt.bst` 文件，同样本次更新默认为它（应广大用户需求，按照引用次序列表参考文献）

## v0.1.4 版本更新，详情如下：
- 首先，修复了生成后的PDF复制乱码问题；

- 默认使用者为Windows系统

- 默认使用华文中宋（STZhongsong）作为中易宋体（SimSun）的粗体
	
	原因是中易宋体根本没有粗体，强制对其加粗会造成一些问题。word的处理很投机，它对正常宋体进行了差值再计算（详情见http://blog.csdn.net/windtailljj/article/details/7422344），华文中宋与中易宋体的word加粗版很像，故而采用之。
	
- 对于其他系统以及不想使用华文中宋作为中易宋体粗体的用户，还添加`Fandol`参数以使用[Fandol](https://github.com/clerkma/fandol-fonts)字体族。
	
	Windows用户注意，启用此命令就没有了隶书（`\lishu`），幼圆（`\youyuan`），微软雅黑（`\yahei`）三个字体的预定义命令了，本文提供的范例很有可能会编译不通过；不用担心，将Chapters.tex中使用的相关命令删掉即可，如果使用批处理编译的话强行回车也行。

- 添加`nologo`参数，封面不使用Logo

- 修复封面标题英文未加黑体问题，感谢[lanthree](https://github.com/lanthree)同学

- 修复英文摘要关键词名称不对的问题，感谢[lanthree](https://github.com/lanthree)同学

- 此外，感谢自本模板发布以来，一直关注本模板的同学们。如果对本次的更新不满意，v0.1.3版本的做了Release，可以继续使用。

---

本模板目前还处于测试阶段，纯属个人爱好制作；仅仅含有本科版；

鉴于作者还是 LaTeX 的入门者；正在努力学习；会不定期维护。

## 写在前面

西安电子科技大学学位论文模板已有我校**齐飞**老师制作 [xduthesis](https://github.com/fredqi/xduthesis).

本人制作基于[ctex套件v2.0.2](https://github.com/CTeX-org/ctex-kit) 中的 ctexbook, TeXLive2015 制作；

制作之初，面向 LaTeX 半个小白用户以及刚入门用户；因此生成好了 **XDUthesis.cls** 和 **XDUthesis.cfg**
文件。下载后即可使用；

## 使用方法

### Windows用户

> 为方便 Windows 用户，专门写好了两种编译脚本；还有示例可供学习使用。

**使用前，请仔细阅读 XDUthesis.pdf 模板用户手册！**

`MakeTemplate.bat`是根据`XDUthesis.dtx`和`XDUthesis.ins`生成模板文档类`XDUthesis.cls`和模板配置文件`XDUthesis.cfg`的。由于本人已经为小白用户生成好了，下载后无需再运行了。

`MakeManual.bat`根据`XDUthesis.dtx`来生成用户说明文档的，由于本人已经为小白用户生成好了，下载后无需再运行了。

### Linux/Mac用户

#### 生成模板

```bash
$ make template
```

#### 生成用户说明手册

```bash
$ make manual
```

#### 生成示例

使用`XeLaTeX`:

```bash
$ make xelatex
```

使用`LaTeXMk`:

```bash
$ make latexmk
```

#### 清理文件夹

```bash
$ make clean
```

## 模板文件介绍

### 模板文件

+ XDUthesis.dtx - 模板文档类与说明文档混排文件
+ XDUthesis.ins - 模板驱动文件
+ XDUthesis.cls - 模板文档类
+ XDUthesis.cfg - 模板配置文件
+ XDUthesis.pdf - 用户手册
+ XDUbib.bst - 参考文献样式

### 示例文件

+ Code/ 源代码存放文件夹
+ Figure/ 图片存放文件夹
+ ThesisFiles/ 模板章节、参考文献、附录等文件夹
+ Demo.tex - 模板示例文档主文件

> 注：文件夹内容不再介绍。

### 编译脚本

#### For Windows

+ MakeManual.bat - 生成用户手册的脚本
+ MakeByXeLaTeX.bat - 使用XeLaTeX 生成实例
+ MakeByLaTeXMk.bat - 使用LaTeXMk生成例子 
+ MakeTemplate.bat - 生成模板的脚本
+ Clean.bat 模板中间文件清除脚本

#### For Linux/Mac

+ Makefile - Linxu/Mac用的Makefile
