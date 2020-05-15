---
title: Enumerate
tags: basic
---

Using `\usepackage{enumitem}` will allow you to customize the enumerate environment label.

- `\arabic*` for 1, 2, 3...
- `\alph*` for a, b, c...
- `\Alph*` for A, B, C...
- `\roman*` for i, ii, iii...
- `\Roman*` for I, II, III...

For example, the following code:

```latex
\begin{enumerate}[label=(\arabic*)]
    \item first item
    \item second item
\end{enumerate}
```

will produce

![](https://www.sibeliusp.com/old/other/latex-examples/enumitem.png)

Circled label will be a bit trickier:

```latex
\begin{enumerate}[label=\large\protect\textcircled{\small\arabic*}]
    \item First item
    \item Second item
    \item Third item
    \item Fourth item
\end{enumerate}

    \textcircled{\small{2}}

or

    {\large \textcircled{\small 2}}

or

    {\Large \textcircled{\normalsize 2}}                  
```

will produce

![](https://www.sibeliusp.com/old/other/latex-examples/circled_item.png)
