<div align=center><img width="100" height="100" src="./jlu.png"/></div>

吉林大学学位论文Latex模板
=============================

### 声明
1. 基于[北京大学学位论文latex模板(pkuthss)](https://gitea.com/CasperVector/pkuthss)<br>
2. 本项目与吉林大学官方无关，输出格式未经吉林大学任何学院的教务部门以及相关单位认可，因使用该模板导致任何后果与该项目和项目的开发人员无关.<br>
3. 欢迎吉大校友帮忙完善改进，我们的最终目标是创建一个属于吉大人自己的、覆盖本硕博的通用论文模板。<br>
### 关键文件及其作用
1. `main.tex`用于安排全文各章节的顺序，也可以直接用于书写正文。<br>
2. `spine.tex`是论文封面。<br>
3. `jlutex-gbk.def`和`jlutex-utf8.def`是中文字符常量表。<br>
4. `*.bib`是参考文献表。<br>
5. `jlutex.cls`是文档类定义文件，用于自定义文档类、命令和环境。<br>
6. `./chap/`中是各个章节的独立文件。<br> 
7. `doc`文件夹中是`backup.tex`(没有实际作用)和pkuthss的文档。<br>
### build
1. texlive 2018 or 2019 or later.<br>
2. texstudio or vscode with LaTex Workshop extension<br>