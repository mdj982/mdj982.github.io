---
title: Math Views with Tex Notations
date: 2020-03-31
categories:
- HexoUsage
tags:
- TeX
- MathJax
---

Hexo can automatically include Mathjax and almost correctly interpret tex commands to math formulas. The author is a VSCoder, and prefer built-in Markdown-viewer with extension "Markdown+Math" (ID: goessner.mdmath). Therefore the only purpose is to let both Hexo and VSCode display a common file well.

## Installation
Required packages:
- hexo-math
- hexo-renderer-kramed (or hexo-renderer-pandoc)

```bash
$ #install hexo-math
$ npm install --save hexo-math
$ # check installed renderers, at the root of Hexo
$ grep "hexo-renderer-" ./package.json
$ # uninstall hexo-renderer-marked if exists
$ npm uninstall --save hexo-renderer-marked;
$ # install hexo-renderer-kramed if inexists
$ npm install --save hexo-renderer-kramed;
```

## Configuration

MathJax source link has been changed in 2017 (https://www.mathjax.org/cdn-shutting-down/). The link shown below is available.

```diff _config.yml
+ math:
+ engine: 'mathjax'
+ mathjax:
+ src: https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_CHTML
+ config:
+ tex2jax:
+ inlineMath: [ ['$','$'], ["\\(","\\)"] ]
+ displayMath: [ ['$$','$$'], ["\\[","\\]"] ]
```

## Templates

~~~md
    <!-- inline formula -->
    $formula-0$

    <!-- formula block, centered -->
    $$
    formula-1 \\
    formula-2 \\
    ...
    formula-n \\
    $$
~~~

## Previews

$$
    \|x\| = \mathrm{abs}(x)
$$
$$ 
    \sum_{k=1}^3 k = \prod_{k=1}^3 k
$$
$$
    f_k = \begin{cases}
      1 & (k = 0 \lor k = 1) \\
      f_{k - 1} + f_{k - 2} & (otherwise)
    \end{cases}
$$
$$
    \begin{eqnarray*}
      \binom{n}{k} 
      &=& \binom{n - 1}{k - 1} + \binom{n - 1}{k} \\
      &=& \binom{n - 2}{k - 2} + 2\binom{n - 2}{k - 1} + \binom{n - 2}{k}
    \end{eqnarray*}
$$
$$
    \overline{P \cup Q} = \overline{P} \cap \overline{Q}
$$
$$
    \varlimsup_{n \to \infty} A_n = \bigcap_{n \in \mathbb{N}}\bigcup_{k \ge n} A_k
$$
$$
    \iint_{\Omega} f(x,y) dxdy
$$
$$
    H = \frac{1}{\sqrt{2}}\left(
    \begin{array}{cc}
      1 & 1 \\
      1 & -1
    \end{array}
    \right)
$$


## Codes

```tex
$$
    \|x\| = \mathrm{abs}(x)
$$
$$
    \sum_{k=1}^3 k = \prod_{k=1}^3 k
$$
$$
    f_k = \begin{cases}
      1 & (k = 0 \lor k = 1) \\
      f_{k - 1} + f_{k - 2} & (otherwise)
    \end{cases}
$$
$$
    \begin{eqnarray*}
      \binom{n}{k} 
      &=& \binom{n - 1}{k - 1} + \binom{n - 1}{k} \\
      &=& \binom{n - 2}{k - 2} + 2\binom{n - 2}{k - 1} + \binom{n - 2}{k}
    \end{eqnarray*}
$$
$$
    \overline{P \cup Q} = \overline{P} \cap \overline{Q}
$$
$$
    \varlimsup_{n \to \infty} A_n = \bigcap_{n \in \mathbb{N}}\bigcup_{k \ge n} A_k
$$
$$
    \iint_{\Omega} f(x,y) dxdy
$$
$$
    H = \frac{1}{\sqrt{2}}\left(
    \begin{array}{cc}
      1 & 1 \\
      1 & -1
    \end{array}
    \right)
$$
```