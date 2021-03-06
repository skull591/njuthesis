# 南京大学山寨LyX毕业论文模板

宗旨：**去你麻痹的国家标准。**

以国际惯例为基准、简洁美观为首要目标，大致保留国家标准要求。本模板参照自[NJU Thesis](https://github.com/Haixing-Hu/nju-thesis)模板并引入少部分代码，保持绝大部分视觉元素的兼容(包括论文所需的封面、摘要页等)。

p.s. 真佩服论文模版的原始作者njut的dalao能完成如此浩大的工程……

## 使用方法

确定以下内容已安装：

1. LyX (>= 2.2);
2. 能在命令行中使用的xelatex (macOS/Linux/Cygwin均支持);
3. 中文字体。可以在`thesis.yaml`中设置，模版使用的是Windows系字体;
4. Python (with yaml)。

使用前首先在`thesis.yaml`中进行设置，然后运行run.py生成必要的文件，在LyX中编辑论文。

如果用模版新建文件，在文档->选项: (1) 勾选non-TeX字体; (2) 输出格式为PDF (XeTeX)。如果拷贝一个example就没有问题了。

## 特性

* 小。总共只有300行TeX代码，其中还有一半是从NJU Thesis偷来的字号设置。
    * 所有论文相关设置都在`thesis.layout`文件。
    * 少量的宏包依赖，防止出现诡异的问题。
* 容易定制。想在标题页表格加一行？想调整摘要页格式？一分钟就能搞定，不需要看任何代码。
    * YAML格式元数据，人更容易阅读和修改。
    * 论文标题/作者等信息集中放置。
    * 定制字体/LaTeX导言区。
* 依托LyX：
    * 所见即所意(WYSIWYM)的可视化编辑。
    * 每个文件可以单独编译，不会丢失格式/排版。
    * 可以用LyX精调标题/摘要页的模版，无需阅读代码。
    * 即时预览和修改公式。公式编辑器支持LaTeX语法，可以定义全局宏。

## 定制

* 全局设置在`thesis.layout`中，主要是LaTeX导言区。
* 页眉/页脚设置在`frontmatter/frontmatter.lyx`。该文件包含标题页/摘要页/目录。
* 标题页文件为`frontmatter/title.lyx`。
* 摘要页文件为`frontmatter/abstract.lyx`。

## TODO

1. `\parindent`的设置是手工的，改成精确的。
2. 代码很乱，有心人请帮忙整理。
