# 线性代数习题课整理稿

本工程依据 `1班习题课#1.pdf` 至 `1班习题课#13.pdf` 的手写内容整理。原稿为图像型 PDF，整理过程中对数学符号、矩阵、行列式和证明结构进行了人工校订，并将重复的初等行变换适度压缩。文档追求内容与论证等价，不追求逐页、逐行复刻。

## 文件结构

- `main.tex`：统一导言区、符号、定理环境和总目录，并按顺序使用 `\input` 引入十三个分文件。
- `sections/01.tex` 至 `sections/13.tex`：分别对应原始的 `1班习题课#1.pdf` 至 `1班习题课#13.pdf`。
- `main.pdf`：已经编译并检查过的成稿。
- `Makefile`：提供编译与清理命令。

## 编译

需要支持中文的 XeLaTeX 环境。推荐使用较完整的 TeX Live 安装，并在工程根目录运行

```bash
latexmk -xelatex -interaction=nonstopmode -halt-on-error main.tex
```

也可运行

```bash
make
```

若不使用 `latexmk`，至少执行两遍

```bash
xelatex main.tex
xelatex main.tex
```

以生成完整目录与交叉引用。
