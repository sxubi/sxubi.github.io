---
layout: post
mathjax: true
categories: media
title: "Real Analysis"
---

![Static Badge](https://img.shields.io/badge/Category-Notes-blue) ![Static Badge](https://img.shields.io/badge/Subject-Mathematics-forestgreen) ![Static Badge](https://img.shields.io/badge/In_progress-orange) 

### <center>1 Sequence and Series of Functions</center>
#### §1.1 Interchange of Limit Processes
**Definition** (Pointwise convergence)**.** $$\{f_n\}$$ is a sequence of real-valued functions defined on a set $$E\subset\mathbb{R}$$. $$\forall x\in E$$, the sequence of numbers $$\{f_n(x)\}$$ converges. Define a function $$f$$ by

$$f(x)=\lim_{n\to\infty}f_n(x),\quad x\in E$$

and say $$\{f_n\}$$ *converges pointwise* to $$f$$ on $$E$$. That is, a sequence converges pointwise to $$f$$ on $$E$$ if for every point $$x\in E$$, $$\forall\epsilon>0, \exists N$$ such that $$n\geq N\Rightarrow |f_n(x)-f(x)|<\epsilon$$. Call $$f$$ the *limit* of $$\{f_n\}$$.        
A series $$\sum f_n(x)$$ converges pointwise on $$E$$ if the sequence $$\{s_n\}$$ of partial sums, $$\displaystyle s_n(x)=\sum_{i=1}^nf_i(x)$$ converges pointwise on $$E$$. If $$s$$ is the limit of $$\{s_n\}$$, 

$$s(x)=\sum_{n=1}^\infty f_n(x),\quad x\in E,$$

and call $$s$$ the *sum* of the series $$\sum f_n$$.

> Remark:    
> $$\displaystyle\lim_{t\to x}\lim_{n\to\infty}f_n(t)\neq \lim_{n\to\infty}\lim_{t\to x}f_n(t).$$        
> $$\displaystyle\lim_{n\to\infty}\lim_{t\to x}\frac{f_n(t)-f_n(x)}{t-x}\neq\lim_{t\to x}lim_{n\to\infty}\frac{f_n(t)-f_n(x)}{t-x}.$$      
> $$\displaystyle\lim_{n\to\infty}\int_a^b f_n(x)dx\neq\int_a^b\lim_{n\to\infty}f_n(x)\,dx.$$


#### §1.2 Uniform Convergence
**Defintion** (Uniform convergence)**.** Suppose $$\{f_n\}$$ is a sequence of real-valued functions defined on $$E\in \mathbb{R}$$. We say that $$\{f_n\}$$ *converges uniformly* to $$f$$ on $$E$$ if $$\forall\epsilon>0,\exists N$$ such that $$n\geq N$$ implies $$|f_n(x)-f(x)|<\epslion$$ for any $$x\in E$$. Also write $$f_n\to f$$ uniformly on $$E$$.     
A series $$\sum f_n(x)$$ converges uniformly on $$E$$ if the sequence $$\{s_n\}$$ of partial sums, $$s_n(x)=\displaystyle \sum_{k=1}^n f_k(x)$$, converges uniformly on $$E$$.      
> Converges uniformly on the set $$\Rightarrow$$ converges pointwise on the set.

**Theorem** (Cauchy criterion for uniform convergence)**.** The sequence of functions $$\{f_n\}$$ defined on $$E\subset\mathbb{R}$$ converges uniformly on $$E$$ iff it satisfies the *Cauchy Criterion* for uniform converges: $$\forall\epsilon>0, \exists N$$ such that $$m,n\geq N$$ implies $$|f_n(x)-f_m(x)|<\epsilon$$ for all $$x\in E$$.      
**Theorem** (Weierstrass M-Test)**.** Suppose $$\{f_n\}$$ is a sequence of functions defined on $$E\subset\mathbb{R}$$, and suppose there is a sequence of nonnegative numbers $$\{M_n\}$$ such that $$|f_n(x)|\leq M_n,n=1,2,3\cdots,$$ for all $$x\in E$$. Then $$\sum f_n$$ converges uniformly on $$E$$ if $$\sum M_n$$ converges.      
**Theorem** (Changing order of limits)**.** Suppose $$f_n\to f$$ uniformly on a set $$E\subset\mathbb{R}$$. Let $$x$$ be a limit point of $$E$$ and suppose that $$\displaystyle\lim_{t\to x}f_n(t)=A_n,n=1,2,3,\cdots.$$ Then $$\{A_n\}$$ converges, and $$\displaystyle\lim_{t\to x}f(t)=\lim_{n\to\infty} A_n$$, or equivalently, $$\displaystyle \lim_{t\to x}\lim_{n\to\infty} f_n(t)=\lim_{n\to\infty}\lim_{t\to x}f_n(t)$$.     
**Theorem** (Countinuity of the limit function)**.** If $$f_n\to f$$ uniformly on $$E\subset\mathbb{R}$$ and if $$\{f_n\}$$ is a sequence of continuous functions on $$E$$, then $$f$$ is continuous on $$E$$.    
