---
layout: post
mathjax: true
categories: media
title: "Real Analysis"
---

![Static Badge](https://img.shields.io/badge/Category-Notes-blue) ![Static Badge](https://img.shields.io/badge/Subject-Mathematics-forestgreen) ![Static Badge](https://img.shields.io/badge/Completed-orange) 

### <center>1 Sequence and Series of Functions</center>
#### §1.1 Interchange of Limit Processes
**Definition** (Pointwise convergence)**.** $$\{f_n\}$$ is a sequence of real-valued functions defined on a set $$E\subset\mathbb{R}$$. $$\forall x\in E$$, the sequence of numbers $$\{f_n(x)\}$$ converges. Define a function $$f$$ by

$$f(x)=\lim_{n\to\infty}f_n(x),\quad x\in E$$

and say $$\{f_n\}$$ **converges pointwise** to $$f$$ on $$E$$. That is, a sequence converges pointwise to $$f$$ on $$E$$ if $$\forall x\in E,\forall\epsilon>0, \exists N$$ such that $$n\geq N\Rightarrow |f_n(x)-f(x)|<\epsilon$$. Call $$f$$ the **limit** of $$\{f_n\}$$.        
A series $$\sum f_n(x)$$ converges pointwise on $$E$$ if the sequence $$\{s_n\}$$ of partial sums, $$\displaystyle s_n(x)=\sum_{i=1}^nf_i(x)$$ converges pointwise on $$E$$. If $$s$$ is the limit of $$\{s_n\}$$, 

$$s(x)=\sum_{n=1}^\infty f_n(x),\quad x\in E,$$

and call $$s$$ the **sum** of the series $$\sum f_n$$.

#### §1.2 Uniform Convergence


