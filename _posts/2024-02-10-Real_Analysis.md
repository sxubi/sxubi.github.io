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

> **Remark**:    
> &emsp;$$\displaystyle\lim_{t\to x}\lim_{n\to\infty}f_n(t)\neq \lim_{n\to\infty}\lim_{t\to x}f_n(t).$$        
> &emsp;$$\displaystyle\lim_{n\to\infty}\lim_{t\to x}\frac{f_n(t)-f_n(x)}{t-x}\neq\lim_{t\to x}\lim_{n\to\infty}\frac{f_n(t)-f_n(x)}{t-x}.$$      
> &emsp;$$\displaystyle\lim_{n\to\infty}\int_a^b f_n(x)dx\neq\int_a^b\lim_{n\to\infty}f_n(x)\,dx.$$


#### §1.2 Uniform Convergence
**Defintion** (Uniform convergence)**.** Suppose $$\{f_n\}$$ is a sequence of real-valued functions defined on $$E\in \mathbb{R}$$. We say that $$\{f_n\}$$ *converges uniformly* to $$f$$ on $$E$$ if $$\forall\epsilon>0,\exists N$$ such that $$n\geq N$$ implies $$|f_n(x)-f(x)|<\epsilon$$ for any $$x\in E$$. Also write $$f_n\to f$$ uniformly on $$E$$.     
A series $$\sum f_n(x)$$ converges uniformly on $$E$$ if the sequence $$\{s_n\}$$ of partial sums, $$s_n(x)=\displaystyle \sum_{k=1}^n f_k(x)$$, converges uniformly on $$E$$.      
> Converges uniformly on the set $$\Rightarrow$$ converges pointwise on the set.

**Theorem** (Cauchy criterion for uniform convergence)**.** The sequence of functions $$\{f_n\}$$ defined on $$E\subset\mathbb{R}$$ converges uniformly on $$E$$ iff it satisfies the *Cauchy Criterion* for uniform converges: $$\forall\epsilon>0, \exists N$$ such that $$m,n\geq N$$ implies $$|f_n(x)-f_m(x)|<\epsilon$$ for all $$x\in E$$.      
**Theorem** (Weierstrass M-Test)**.** Suppose $$\{f_n\}$$ is a sequence of functions defined on $$E\subset\mathbb{R}$$, and suppose there is a sequence of nonnegative numbers $$\{M_n\}$$ such that $$|f_n(x)|\leq M_n,n=1,2,3\cdots,$$ for all $$x\in E$$. Then $$\sum f_n$$ converges uniformly on $$E$$ if $$\sum M_n$$ converges.      
**Theorem** (Changing order of limits)**.** Suppose $$f_n\to f$$ uniformly on a set $$E\subset\mathbb{R}$$. Let $$x$$ be a limit point of $$E$$ and suppose that $$\displaystyle\lim_{t\to x}f_n(t)=A_n,n=1,2,3,\cdots.$$ Then $$\{A_n\}$$ converges, and $$\displaystyle\lim_{t\to x}f(t)=\lim_{n\to\infty} A_n$$, or equivalently, $$\displaystyle \lim_{t\to x}\lim_{n\to\infty} f_n(t)=\lim_{n\to\infty}\lim_{t\to x}f_n(t)$$.     
**Theorem** (Countinuity of the limit function)**.** If $$f_n\to f$$ uniformly on $$E\subset\mathbb{R}$$ and if $$\{f_n\}$$ is a sequence of continuous functions on $$E$$, then $$f$$ is continuous on $$E$$. (With uniform convergence, the limit of continuous functions is continuous.)      
**Theorem** (Dini's theorem)**.** Suppose $$K\subset\mathbb{R}$$ is compact, and (1) $$\{f_n\}$$ is a sequence of continuous functions on $$K$$, (2) $$\{f_n\}$$ converges pointwise to a continuous function $$f$$ on $$K$$. (3) $$f_n(x)\geq f_{n+1}(x)$$ for all $$x\in K,n=1,2,3,\cdots$$ Then $$f_n\to f$$ uniformly on $$K$$.     
**Theorem** (Interchange of the limit and the integration)**.** Suppose $$f_n\to f$$ uniformly on $$[a,b]$$. If $$f_n\in\mathscr{R}[a,b]$$ for $$n=1,2,3,\cdots$$, then $$f\in\mathscr{R}[a,b]$$ and 

$$\int_a^b f\,dx=\lim_{n\to\infty}\int_a^b f_n\,dx,$$

that is,

$$\int_a^b \lim_{n\to\infty}f_n\,dx=\lim_{n\to\infty}\int_a^b f_n\,dx.$$

(With uniform convergence, the limit of the integrals equals to the integral of the limit.)      
**Corollary.** If $$f_n\in\mathscr{R}[a,b]$$, and $$\sum_{n=1}^\infty f_n(x)=f(x)$$ uniformly on $$[a,b]$$, then $$\int_a^b f\,dx=\sum_{n=1}^\infty\int_a^b f_n\,dx.$$      
**Theorem** (Interchange the limit and the differentiation)**.** Suppose $$\{f_n\}$$ is a sequence of differentiable functions on $$[a,b]$$ such that $$\{f_n(x_0)}$$ converges for some $$x_0\in[a,b]$$. If $$\{f_n'\}$$ converges uniformly on $$[a,b]$$, then $$\{f_n\}$$ converges uniformly on $$[a,b]$$ to a function $$f$$ and 

$$f'(x)=\lim_{n\to\infty}f'_n(x),\quad\lim_{t\to x}\lim_{n\to\infty}\frac{f_n(t)-f_n(x)}{t-x}=\lim_{n\to\infty}\lim_{t\to x}\frac{f_n(t)-f_n(x)}{t-x}.$$

(With uniform convergence of $$\{f_n\}$$ and $$\{f_n'\}$$, the limit of the derivatives equals to derivative of the limit.)

#### §1.3 Approximation in Function Space
**Definition** (Cartesian product of sets)**.** The *Cartesian product* of 2 sets $$A$$ and $$B$$, denoted $$A\times B$$, is defined as

$$A\times B=\{(a,b):a\in A,b\in B\}.$$

Simply called the *product* of $$A$$ and $$B$$.      
**Definition** (Metric space)**.** A set $$X$$, whose elements are called *points*, is said to be a *metric space* if there exists an association function $$d:X\times X\to\mathbb{R}$$, called the *distance* from point $$p$$ to $$q$$ such that    
&emsp;(1) $$d(p,q)\geq 0$$ and $$d(p,q)=0$$ iff $$p=q$$.     
&emsp;(2) $$d(p,q)=d(q,p)$$.          
&emsp;(3) $$d(p,q)\leq d(p,r)+d(r,q)$$ for any $$r\in X$$.      
Call $$d$$ a *metric* or *distance function* on $$X$$. Use the notation $$(X,d)$$ for the metric space with the distance function $$d$$. If every Cauchy sequence in a metric space $$(X,d)$$ has a limit that is also in $$X$$, then $$(X,d)$$ is said to be *complete.*       
**Definition** (Metric space $$\mathscr{C}(X)$$)**.** Let $$X$$ be a metric space. Define $$\mathscr{C}(X)$$ to be the set of all real-valued, continuous, bounded functions with domain $$X$$. Associate with each $$f\in\mathscr{C}(X)$$ its *supremum norm*

$$\Vert f\Vert=\sup_{x\in X}|f(x)|.$$

This gives an induced metric on $$\mathscr{C}(X)$$:

$$d(f,g)=\Vert f-g\Vert=\sup_{x\in X}|f(x)-g(x)|,\quad f,g\in\mathscr{C}(X).$$ 

$$\mathscr{C}(X)$$ is a complete metric space.      
**Theorem** (Weierstrass approximation theorem)**.** If $$f$$ is a real continuous function on $$[a,b]$$, there exists a sequence of polynomials $$\{P_n\}$$ such that

$$\lim_{n\to\infty}P_n(x)=f(x)$$

uniformly on $$[a,b]$$.



