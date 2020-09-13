---
title: Tikz annotation
tags: basic tikz
---

Sometimes we want to have some annotations around the text by drawing some arrows towards the text. By doing the following, we can have annotations around the text with tikz tricks.

```latex
\tikz[baseline=(a.base)]{
	\node[inner sep=1.5pt] (a) {$x$};
	\node[overlay,below =1em of a] (text) {\scriptsize\color{gray} set};
	\draw[overlay,->,shorten <=1pt, gray, line join=round, 
        decorate, decoration={zigzag, segment length=4,amplitude=1.2,post=lineto, post length=0.5pt}]
        (text.north) -- (a.south);
}
\in 
\tikz[baseline=(a.base)]{
	\node[inner sep=1.5pt] (a) {$Y$};
	\node[overlay,below =1em of a] (text) {\scriptsize\color{gray} class};
	\draw[overlay,->,shorten <=1pt, gray, line join=round, 
        decorate, decoration={zigzag, segment length=4,amplitude=1.2,post=lineto, post length=0.5pt}]  
        (text.north) -- (a.south);
}
```

The result can be viewed on section 1.2 of the [pmath 433 notes](https://notes.sibeliusp.com/pdfs/1209/pmath433.pdf). The squiggly arrows are inspired from [here](https://tex.stackexchange.com/a/12680) where we need `\usetikzlibrary{decorations.pathmorphing}`.
