---
title: Math Views with Tex Notations
date: 2020-03-31
---

## Preface
Hexo has a toolchain to automatically include Mathjax and almost correctly interpret tex commands to math formulas. The author is a VSCoder, and prefer built-in Markdown-viewer with extension "Markdown+Math" (ID: goessner.mdmath). Therefore the only purpose is to let both Hexo and VSCode display a common file well.

## Installation
Required renderers:
- hexo-renderer-kramed (or hexo-renderer-pandoc)

Installation
```bash
$ # check installed renderers, at the root of Hexo
$ grep "hexo-renderer-" ./package.json
$ # uninstall hexo-renderer-marked if exists
$ npm uninstall --save hexo-renderer-marked;
$ # install hexo-renderer-kramed if inexists
$ npm install --save hexo-renderer-kramed;
```

## Templates

~~~md
    <!-- inline formula -->
    $ formula-0 $

    <!-- formula block, centered -->
    $$
    formula-1 \\
    formula-2 \\
    ...
    formula-n \\
    $$
~~~

## Previews
### Fraction

$$
    x = \frac{a}{b} = \left( \frac{a}{b} \right) = \frac{1}{\frac{b}{a}} = \cfrac{1}{\cfrac{b}{a}}
$$

### Absolute
$$
    ||x|| = abs(x) \\
    \|x\| = \mathrm{abs}(x)
$$

$$
A = \left(
    \begin{array}{ccc}
      a & b & c \\
      d & e & f \\
      g & h & i
    \end{array}
  \right)
$$