$$
\newcommand{\scal}[1]{#1}                 % 标量
\newcommand{\vect}[1]{\mathbf{#1}}        % 向量 (英文字母)
\newcommand{\vectg}[1]{\boldsymbol{#1}}   % 向量 (希腊字母)
\newcommand{\matr}[1]{\mathbf{#1}}        % 矩阵
\newcommand{\matri}[1]{\boldsymbol{#1}}   % 矩阵 (斜体)
\newcommand{\tens}[1]{\bm{\mathsf{#1}}}   % 张量
$$
# LaTeX基础
[LaTeX --- 维基百科, 自由的百科全书](https://zh.wikipedia.org/wiki/LaTeX)
[LaTeX数学符号手册（中文版）](https://lixingcong.github.io/2016/04/04/LaTex-intro/)
# LaTeX数学符号表示规范
## 正体与斜体
默认情况下，LaTeX 数学模式里的字母是斜体。一般约束**变量用斜体，非变量用正体**。  
通常在以下情况下使用正体：
- 前后缀/标签，如 $E_{\text{k}}$，其中 $\text{k}$ 代表 kinetic 动能，是标签。
- 特殊常数，如 $\text{e}^{\text{i}\pi} + 1 = 0$。
- 微分算子，如 $\int x \, \text{d}x$。
## 标量、矢量/向量、矩阵
标量使用**斜体字母**，矢量/向量使用**加粗的正体或斜体小写字母（现代科技论文）**、**带箭头的字母（传统物理学）**，矩阵使用**加粗的正体或斜体大写字母**。   
在本笔记中，

- 标量使用斜体字母，如 $x$。
- 矢量使用加粗的斜体小写字母，如 $\vectg{x}$。
- 矩阵使用加粗的斜体大写字母，如 $\vectg{X}$。
## 标准数学函数
所有标准的数学函数名（如 sine, log, limit, expectation 等）都**必须用直立正体**，并且前后要有适当的间距。如期望 $\text{E}\{x\}$，正弦 $\sin{x}$ 等。
## 集合与数域
表示特定的数学集合（如实数集、复数集、矩阵空间）时，不能用普通的字母，需要使用特定的花体。
- 风格 A：**空心黑体**。用于表示经典的数域（实数、整数、自然数等）。如实数集 $\mathbb{R}$，实数空间 $\mathbb{R}^{n \times m}$，自然数集 $\mathbb{N}$。
- 风格 B：**花体**。通常用于表示一般的集合、样本空间、或者机器学习中的损失函数、分布族。如样本空间 $\mathcal{S}$，假设空间 $\mathcal{H}$，损失函数 $\mathcal{L}$。
## 括号缩放
当括号中存在分式、矩阵或积分时，需要拉伸括号的高度，如 $\left(\frac{1}{2}\right)$。只要括号内部的高度超过了一行，就要配对使用 `\left(` 和 `\right)`（或者 `\left[` / `\right]`），LaTeX 会自动把括号拉伸到合适的高度。
## 转置符号与埃尔米特共轭 (Transpose)
矩阵的转置符号**必须是正体**，因为它是操作符，不是变量。如 $\mathbf{A}^{\text{T}}$ 。