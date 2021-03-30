<div align=center><img width="100" height="100" src="./jlu.png"/></div>

吉林大学学位论文Latex模板
=============================

### 声明
1. 基于[北京大学学位论文latex模板(pkuthss)](https://gitea.com/CasperVector/pkuthss)开发<br>
2. 本项目与吉林大学官方无关，输出格式未经吉林大学任何学院的教务部门以及相关单位认可，因使用该模板导致任何后果与该项目和项目的开发人员无关.<br>
3. 欢迎吉大校友帮忙完善改进，我们的最终目标是创建一个属于吉大人自己的、覆盖本硕博的通用论文模板。<br>
4. 吉林大学本科毕业论文（计算机学院）Latex模板请参考[JLU-CCST-Thesis](https://github.com/x86vk/JLU-CCST-Thesis).<br>
5. 该模板距离“完美”还有相当的距离，我们的最终目标是使该模板的输出效果满足学院对于学位论文的要求。<br>
6. 作者来自吉林大学计算机学院，该模板的格式来自于计算机学院的要求（2021年）。<br>

### 关键文件及其作用
1. `main.tex`用于安排全文各章节的顺序，也可以直接用于书写正文。<br>
2. `spine.tex`是论文封面。<br>
3. `jlutex-gbk.def`和`jlutex-utf8.def`是中文字符常量表。<br>
4. `*ref.bib`是参考文献表。<br>
5. `jlutex.cls`是文档类定义文件，用于自定义文档类、命令和环境。<br>
6. `./chap/`中是各个章节的独立文件。<br> 
7. `doc`文件夹中是`backup.tex`(没有实际作用)和pkuthss的文档。<br>
8. `cleanup.cmd`用来清除编译过程中产生的中间文件。<br>
### build
1. [texlive](https://tug.org/texlive/) 2019 or later.<br>
2. [texstudio](http://texstudio.sourceforge.net/) or [vscode](https://code.visualstudio.com/) with LaTex Workshop extension<br>
3. build cmd：
   ```bash
   pdflatex texfile  # texfile.tex is the main tex file
   biber -l zh__pinyin texfile
   pdflatex texfile
   pdflatex texfile
   ```
### references
1. [bibtex](http://www.bibtex.org/)<br>
2. [在线latex公式编辑器](https://www.codecogs.com/latex/eqneditor.php?lang=zh-cn)<br>
3. [公式和公式号之间用点连接](https://tex.stackexchange.com/questions/110088/how-to-get-dots-in-between-equation-and-equation-numbers-with-equation-is-centra)<br>
4. [重定义equation环境](https://tex.stackovernet.com/cn/q/122382)<br>

### 注意事项
1. 参考文献中的法文字母（带音标的英文字母）不能直接书写，请参考[bibtex](http://www.bibtex.org/)官网上关于特殊字符的描述。<br>
2. 无论英文还是中文人名，多个作者之间用`and`分隔，如果超过三个作者，会自动加“等”或者“et.al”，不需要自己处理。<br>
3. 插图时，`\caption{图片标题}`一定要放在`\label{图片引用标记}`的前面，否则会报错。<br>
4. 引用在线资源时，`urldate`字段必须是`XXXX-XX-XX`的形式，否则访问时间不会显示。<br>
5. 为了实现公式与公式编号用点连接的功能，对equation进行了重定义，该操作导致在某些情况下equation的行高增加.此外，点的左侧和右侧距离略有不同，并会导致公式略微偏左。如果对行间公式的行距、行高和公式后面的点同时持有最高标准的要求，或者您无法接受该效果，建议您放弃使用此模板，转而采用MathType和MS Office.<br>
6. 公式编号的括号为半角括号（即英文括号）.<br>
7. 暂时不支持参考文献列表中的中文条目使用英文符号，建议使用者尽量避免使用中文参考文献以最大限度的保证体例一致。<br>

### latex和MS word字号对照表

|word 字号|磅值(pt)|线宽(mm)|latex字号命令|
|:---:|:---:|:---:|:---:|
|7号  |5.25 |1.845 |\tiny        |
|6号  |7.875|2.768 |\scriptsize  |
|小5  |9    |3.163 |\footnotesize|
|5号  |10.5 |3.69  |\small       |
|小4  |12   |4.2175|\normalsize  |
|4号  |13.75|4.83  |\large       |
|3号  |15.75|5.53  |\Large       |
|小2  |18   |7.38  |\LARGE       |
|2号  |21   |7.38  |\LARGE       |
|1号  |27.5 |9.48  |\huge        |
|小初 |36   |12.65 |\Huge        |
|初号 |42   |14.76 |\HUGE        |

* 默认为宋体小四字号

### 特别鸣谢
感谢以下同学提出的修改建议：<br>
* [P_Lee](https://github.com/TobisLee)

### 重要更新日志
* 2020年3月25日：
  1. 使用`cmap`，如此生成的pdf文件在中英文混排下可以复制出正确的文字，转word也能识别（当然转word后排版不一定会变成什么样），这样的pdf能够直接用于查重。
  2. 切换到texlive2019。<br>
* 2021年3月30日：
  1. 根据2021年计算机科学与技术学院论文格式要求更新了模板样式，模板与参考格式高度相近。
  2. 添加了[Figure](./Figure)文件夹以存储论文图片，在[Chap](./Chap)文件夹中添加“作者简介及科研成果”。
  3. 在正文中添加了示例内容，方便同学们取用编写。
  4. 为不幸抽中盲审的同学添加了盲审版本[main_DBR.tex](./main_DBR.tex)。
  5. 我们注意到专硕论文封面与学硕有较多不同，因此添加了针对专硕的论文封面模板，但封面上专业（领域）的冒号未能和其他条目完美对其，目前还在解决中。