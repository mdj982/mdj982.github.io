---
title: About Markdown-Codeblocks
---

## Preface

Although it is easy to update pages via Hexo by editing markdown files, Markdown-codeblocks may cause trouble for displaying, since Markdown syntax is too weak (or ambiguous) to nest code blocks. This is an article to memorize a coding style that avoids such a trouble, and also corresponds to built-in Markdown viewer of VSCode.

## Common Styles between Hexo and VSCode

### Preview

Suppose you want to tell readers that your code will display in this way:

~~~md
<!-- code-block-0 -->
```md
Internal markdown code 0.
```
~~~
- Main List
    ~~~md
    <!-- code-block-1-1 -->
    ```md
    Internal markdown code 1-1.
    ```
    ~~~
    ~~~md
    <!-- code-block-1-2 -->
    ```md
    Internal markdown code 1-2.
    ```
    ~~~
    - Sub List
        ~~~md
        <!-- code-block-2 -->
        ```md
        Internal markdown code 2.
        ```
        ~~~

### The Code of the Preview

Then you tell readers the code can be like this: 

<figure class="highlight md">
<table>
<tr>
<td class="gutter">
<pre>
<span class="line">1</span>
<span class="line">2</span>
<span class="line">3</span>
<span class="line">4</span>
<span class="line">5</span>
<span class="line">6</span>
<span class="line">7</span>
<span class="line">8</span>
<span class="line">9</span>
<span class="line">10</span>
<span class="line">11</span>
<span class="line">12</span>
<span class="line">13</span>
<span class="line">14</span>
<span class="line">15</span>
<span class="line">16</span>
<span class="line">17</span>
<span class="line">18</span>
<span class="line">19</span>
<span class="line">20</span>
<span class="line">21</span>
<span class="line">22</span>
<span class="line">23</span>
<span class="line">24</span>
<span class="line">25</span>
<span class="line">26</span>
</pre>
</td>
<td class="code">
<pre>
<span class="line"><span class="code">~~~md</span></span>
<span class="line"><span class="code">&lt;!-- code-block-0 --&gt;</span></span>
<span class="line"><span class="code">```md</span></span>
<span class="line"><span class="code">Internal markdown code 0.</span></span>
<span class="line"><span class="code">```</span></span>
<span class="line"><span class="code">~~~</span></span>
<span class="line"><span class="bullet">- </span>Main List</span>
<span class="line"><span class="code">    ~~~md</span></span>
<span class="line"><span class="code">    &lt;!-- code-block-1-1 --&gt;</span></span>
<span class="line"><span class="code">    ```md</span></span>
<span class="line"><span class="code">    Internal markdown code 1-1.</span></span>
<span class="line"><span class="code">    ```</span></span>
<span class="line"><span class="code">    ~~~</span></span>
<span class="line"><span class="code">    ~~~md</span></span>
<span class="line"><span class="code">    &lt;!-- code-block-1-2 --&gt;</span></span>
<span class="line"><span class="code">    ```md</span></span>
<span class="line"><span class="code">    Internal markdown code 1-2.</span></span>
<span class="line"><span class="code">    ```</span></span>
<span class="line"><span class="code">    ~~~</span></span>
<span class="line"><span class="bullet">    - </span>Sub List</span>
<span class="line"><span class="line"><span class="code">        ~~~md</span></span>
<span class="line"><span class="code">        &lt;!-- code-block-2 --&gt;</span></span>
<span class="line"><span class="code">        ```md</span></span>
<span class="line"><span class="code">        Internal markdown code 2.</span></span>
<span class="line"><span class="code">        ```</span></span>
<span class="line"><span class="code">        ~~~</span></span>
</pre>
</td>
</tr>
</table>
</figure>

### The Code of "The Code of the Preview"

To put the above code, you should write it down in your markdown file. However it seems to be a painful task if done manually. Still, a raw html code can be emplaced in markdown file, and the grammar of this table is easy enough to allow a instant self-made code generator.

```html
<figure class="highlight md">
<table>
<tr>
<td class="gutter">
<pre>
<span class="line">1</span>
<span class="line">2</span>
<span class="line">3</span>
<span class="line">4</span>
<span class="line">5</span>
<span class="line">6</span>
<span class="line">7</span>
<span class="line">8</span>
<span class="line">9</span>
<span class="line">10</span>
<span class="line">11</span>
<span class="line">12</span>
<span class="line">13</span>
<span class="line">14</span>
<span class="line">15</span>
<span class="line">16</span>
<span class="line">17</span>
<span class="line">18</span>
<span class="line">19</span>
<span class="line">20</span>
<span class="line">21</span>
<span class="line">22</span>
<span class="line">23</span>
<span class="line">24</span>
<span class="line">25</span>
<span class="line">26</span>
</pre>
</td>
<td class="code">
<pre>
<span class="line"><span class="code">~~~md</span></span>
<span class="line"><span class="code">&lt;!-- code-block-0 --&gt;</span></span>
<span class="line"><span class="code">```md</span></span>
<span class="line"><span class="code">Internal markdown code 0.</span></span>
<span class="line"><span class="code">```</span></span>
<span class="line"><span class="code">~~~</span></span>
<span class="line"><span class="bullet">- </span>Main List</span>
<span class="line"><span class="code">    ~~~md</span></span>
<span class="line"><span class="code">    &lt;!-- code-block-1-1 --&gt;</span></span>
<span class="line"><span class="code">    ```md</span></span>
<span class="line"><span class="code">    Internal markdown code 1-1.</span></span>
<span class="line"><span class="code">    ```</span></span>
<span class="line"><span class="code">    ~~~</span></span>
<span class="line"><span class="code">    ~~~md</span></span>
<span class="line"><span class="code">    &lt;!-- code-block-1-2 --&gt;</span></span>
<span class="line"><span class="code">    ```md</span></span>
<span class="line"><span class="code">    Internal markdown code 1-2.</span></span>
<span class="line"><span class="code">    ```</span></span>
<span class="line"><span class="code">    ~~~</span></span>
<span class="line"><span class="bullet">    - </span>Sub List</span>
<span class="line"><span class="line"><span class="code">        ~~~md</span></span>
<span class="line"><span class="code">        &lt;!-- code-block-2 --&gt;</span></span>
<span class="line"><span class="code">        ```md</span></span>
<span class="line"><span class="code">        Internal markdown code 2.</span></span>
<span class="line"><span class="code">        ```</span></span>
<span class="line"><span class="code">        ~~~</span></span>
</pre>
</td>
</tr>
</table>
</figure>
```

## Afterword

All the above codes are able to be previewed in VSCode built-in markdown viewer. Actually VSCode's viewer has a slightly better parser than Hexo's, and there is another better way to resolve this problem. Anyway, when you encounter a complicatedly collapsed preview in Hexo (while it goes well in VSCode, GitHub, etc.), emplacement of raw html code is the surest way.