# LaTeX

## How to typeset := correctly

```latex
\documentclass{standalone}
\usepackage{mathtools}
\begin{document}
\( b := 10 \) \emph{versus} \( b \coloneqq 10 \).
\end{document}
```

## How to make set complement

```latex
\overline{L}
```

## Use PSTRicks instead of tikz for automata

```latex
\usepackage{pstricks,pst-node,pst-tree}
```

When using together with Pandoc, make sure to compile it using `pandoc --pdf-engine=xelatex ...`.

## Lightning symbol

```latex
\usepackage{stmaryrd}

$\lightning$
```

Can then be used in math-mode.

## Write something on top of equal sign

```latex
$\stackrel{sometext}{=}$
```

If `def` is not available in math-mode, then use `\text{sometext}`.

## Insert checkmark arrow

```latex
\usepackage{amssymb}

\checkmark
```

## Specify correct hyphenation

```latex
\hyphenation{Transitions-tabelle}
```

## Add margin to block of text

```latex
\usepackage{scrextend}

\begin{addmargin}[1em]{2em}% 1em left, 2em right
...
\end{addmargin}
```

## Fancy headers

```latex
\usepackage{fancyhdr}
\pagestyle{fancy}
```

## Enumeration with roman letters

```tex
\usepackage{enumerate}

\begin{enumerate}[i.]
  \item One
  \item Two
  \item Three
\end{enumerate}
```

Use `[I.]` for capitalized roman letters.

## Linebreak inside big sum

```tex
\usepackage{amsmath}

\sum_{\substack{i \in S \\ i \in T}} i
```

## Enclose align with {}

```tex
\left\{
  \begin{align}
    1 \\ 2 \\ 3
  \end{align}
\right\}
```
