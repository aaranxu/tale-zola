+++
title = "Math Typesetting"
description = "Introducing Doks, a Hugo theme helping you build modern documentation websites that are secure, fast, and SEO-ready — by default."
date = 2021-05-03T09:19:42+00:00
updated = 2021-05-03T09:19:42+00:00
draft = false

[taxonomies]
tags = ["KaTeX", "Math", "Sample"]

[extra]
katex = true
author = "Public"
+++

Mathematical notation in a project can be enabled by using third party JavaScript libraries.
<!-- more -->

In this example we will be using [KaTeX](https://katex.org/)

- Create a macro under `/template/macros.html` with a macro named `katex`.
- Within this macro reference the [Auto-render Extension](https://katex.org/docs/autorender.html) or host these scripts locally.
- Import the macro in your templates like so:  

```bash
{% import 'macros.html' as macros %}
{% if page.extra.katex or section.extra.katex or config.extra.katex %}
{{ macros::katex() }}
{% endif %}
```

- To enable KaTex globally set the parameter `extra.katex` to `true` in a project's configuration
- To enable KaTex on a per page basis include the parameter `extra.katex = true` in content files

**Note:** 

1. Use the online reference of [Supported TeX Functions](https://katex.org/docs/supported.html)

### Examples

<p>
Inline math: \(\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…\) 
</p>

Block math:
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$
