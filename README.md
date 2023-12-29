# Quick-LaTeX 模板

Quick-LaTeX 是一个为 LaTeX 初学者设计的简洁中文模板，旨在帮助初学者快速上手使用 LaTeX，而不用再辛辛苦苦手动配置各种宏包和命令。该模板包含了一系列预先配置的宏包和自带的例子，使得文档排版、字体设置、代码高亮、图表插入等变得更加容易上手。

## 功能说明

- **数学支持**：配置了 `amsmath`, `bm`, `lmodern` 等宏包，用于数学公式编辑，使用了更美观的 Latin Modern 数学字体。

- **代码高亮**：配置了 `listings` 宏包和详细的代码高亮设置，特别优化了 Python 代码的显示效果。

- **算法伪代码**：通过 `algorithm2e` 宏包提供了算法伪代码的编写支持，包含了行号、自定义注释样式等特性。

- **参考文献样式**：使用 `BibTeX`，默认为 `ieeetr` 格式。

- **链接和引用**：通过 `hyperref` 宏包设置了合理的彩色链接和引用，将 citecolor 改成了不瞎眼的CVPR Blue。

- **图表和子图**：配置了 `subcaption` 宏包，用于插入子图。

- **表格增强**：`booktabs` 和 `multirow` 宏包提供了三线表和单元格合并功能。

## 使用方法

1. **安装**：将 `quicklatex.sty` 文件放置到您的 LaTeX 项目目录中。

2. **引用样式文件**：在您的 LaTeX 文档的导言区（`\documentclass{}` 命令之后，`\begin{document}` 命令之前）使用以下命令来引用 `quicklatex.sty` 样式文件：

   ```latex
   \usepackage{quicklatex}
   ```

3. **编译**：使用 `XeLaTeX` 编译器编译您的 LaTeX 文档，对于带参考文献的文档，编译流程为 `XeLaTeX` -> `BibTeX` -> `XeLaTeX` -> `XeLaTeX`。

4. **自定义**：根据需要，您可以通过修改 `quicklatex.sty` 文件来添加或修改预定义的宏包选项和自定义命令。

5. **Overleaf**：您可以点击 [这里](https://www.overleaf.com/read/sjzyrjzvwmzm#cfc355) 在 Overleaf 上使用该模板，Overleaf 上的模板会自动与 GitHub 保持同步。

## 示例

以下是一个使用 Quick-LaTeX 模板的简单 LaTeX 文档示例：

```latex
\documentclass[UTF8]{ctexart}
\usepackage{quicklatex}

\begin{document}

\title{您的文档标题}
\author{您的名字}
\date{\today}
\maketitle

\section{引言}
这是一个使用 Quick-LaTeX 模板的示例文档。

\section{数学}
\begin{equation}
    e^{i\pi} + 1 = 0
\end{equation}

\section{代码}
\begin{lstlisting}[style=python]
def hello_world():
    print("Hello, world!")
\end{lstlisting}

\end{document}
```

## License

该项目采用 MIT 许可证。有关详细信息，请查看 LICENSE 文件。

## 致谢

本项目参考了以下文献和资源：

- [[2212.10156] Planning-oriented Autonomous Driving](https://arxiv.org/abs/2212.10156)， `main.tex` 中的表格示例来源于该论文。

- [[2005.12872] End-to-End Object Detection with Transformers](https://arxiv.org/abs/2005.12872)， `main.tex` 中的图片示例来源于该论文。

- 感谢张皓在知乎上发布的文章 [《论文格式细节整理汇总》 - 知乎](https://zhuanlan.zhihu.com/p/30944610)，这篇文章提供了很多关于 LaTeX 排版细节的干货，强烈推荐大家阅读。

- 感谢 M. Downes 编写的《Short math guide for LaTeX》, 可以在 [CTAN](https://tug.ctan.org/info/short-math-guide/short-math-guide.pdf) 上免费获取。
