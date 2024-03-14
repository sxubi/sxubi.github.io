---
layout: post
mathjax: true
categories: media
title: "Real Analysis"
---

![Static Badge](https://img.shields.io/badge/Category-Notes-blue) ![Static Badge](https://img.shields.io/badge/Subject-Mathematics-forestgreen) ![Static Badge](https://img.shields.io/badge/In_progress-orange) 

### <center>1  Sequence and Series of Functions</center>
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
**Theorem** (Interchange the limit and the differentiation)**.** Suppose $$\{f_n\}$$ is a sequence of differentiable functions on $$[a,b]$$ such that $$\{f_n(x_0)\}$$ converges for some $$x_0\in[a,b]$$. If $$\{f_n'\}$$ converges uniformly on $$[a,b]$$, then $$\{f_n\}$$ converges uniformly on $$[a,b]$$ to a function $$f$$ and 

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

### <center>2  Power Series and Fourier Series</center>
#### §2.1 Power Series
**Definition** (Power series)**.** Given a fixed complex number $$z_0$$ and a sequence $$\{c_n\}$$ of complex number, the series $$\displaystyle\sum_{n=0}^\infty c_n(z-z_0)^n$$ is called a *power series* centered at $$z_0$$, where $$z\in\mathbb{C}$$. The numbers $$c_n$$ are called the *coefficients* of the series.     
A function $$f$$ is called *analytic* on an open set $$D$$ in the complex plane if for any $$z_0\in D$$ one can write

$$f(z)=\sum_{n=0}^\infty c_n(z-z_0)^n,$$

where the coefficients $$\{c_n\}$$ are complex numbers and the series is convergent to $$f(z)$$ for $$z$$ in a neighborhood of $$z_0$$. If we replace "complex" with "real", then the function is called *real analytic.*    
**Theorem** (Radius of convergence)**.** Given the power series $$\sum_{k=0}^\infty c_n(z-z_0)^n$$, put $$\displaystyle\alpha = \lim_{n\to\infty}\sqrt[n]{|c_n|}, R=\frac{1}{\alpha}\in[0,\infty)\cup\{\infty\}.$$ Then the series converges if $$|z-z_0|<R$$ and diverges if $$|z-z_0|>R$$. $$R$$ is called the *radius of convergence* of the power series. The inequality $$|z-z_0|<R$$ is called the *disk of convergence*.        
**Theorem** (Analyticity of power series)**.** 1. Suppose $$\displaystyle f(z)=\sum_{n=0}^\infty c_n(z-z_0)^n$$ for $$|z-z_0|<R,$$ where $$\{c_n\},z,z_0$$ are complex numbers. Then $$f$$ is analytic in $$|z-z_0|<R$$. More explicitly, if $$|z_1-z_0|<R$$, then for some complex numbers $$\{d_n\}$$, $$\displaystyle f(z)=\sum_{n=0}^\infty d_n(z-z_1)^n,|z-z_1|<R-|z_1-z_0|.$$      
&emsp; 2. Suppose $$\displaystyle f(x)=\sum_{n=0}^\infty c_n(x-x_0)^n$$ for $$|x-x_0|<R$$, where $$\{c_n\},x,x_0$$ are real numbers. Then $$f$$ is real analytic in $$|x-x_0|<R$$. More explicitly, if $$|x_1-x_0|<R$$, then for some real numbers $$\{d_n\}$$, $$\displaystyle f(x)=\sum_{n=0}^\infty d_n(x-x_1)^n,|x-x_1|<R-|x_1-x_0|.$$     
**Proposition** (Uniqueness of power series)**.** Suppose $$\sum a_n(z-z_0)^n$$ and $$\sum b_n(z-z_0)^n$$ converge in $$S=\{z:|z-z_0|<R\}$$ for some $$R>0$$. Let $$E$$ be the set of all $$z\in S$$ at which 

$$\sum_{n=0}^\infty a_n(z-z_0)^n=\sum_{n=0}^\infty b_n(z-z_0)^n.$$

If $$E$$ has a limit point in $$S$$, then $$a_n=b_n$$ for $$n=0,1,2,\cdots$$,i.e. the power series obtained from different methods are the same by this proposition.       
**Theorem** (Uniform convergence of power series)**.** Suppose the real series $$\displaystyle\sum_{n=0}^\infty c_n(x-x_0)^n$$ converges for $$|x-x_0|<R$$, where $$\{c_n\},x,x_0$$ are real. Then for any $$\varepsilon>0$$, the series converges uniformly on the interval $$[x-(R-\varepsilon),x_0+(R-\epsilon)].$$ Moreover, if we define $$\displaystyle f(x)=\sum_{n=0}^\infty c_n(x-x_0)^n,\quad |x-x_0|<R,$$ then $$f$$ is continuous and differentiable in $$(x_0-R,x_0+R)$$ and $$\displaystyle f'(x)=\sum_{n=1}^\infty nc_n(x-x_0)^{n-1},|x-x_0|<R.$$    
**Corollary.** Following the above theorem, $$f$$ has derivative of all orders in $$(x_0-R,x_0+R)$$ and

$$f^{(k)}(x)=\sum_{n=k}^\infty n(n-1)\cdots(n-k+1)c_n(x-x_0)^{n-k}.$$

In particular, $$f^{(k)}(x_0)=k!c_k,k=0,1,2,\cdots$$.    
**Theorem** (Properties of the exponential functions)**.** For a complex number $$z$$, denote $$\displaystyle E(z)=\sum_{n=0}^\infty\frac{z^n}{n!}$$. Then for any real $$x$$, $$E(x)=e^x$$, where $$e^x=\sup e^p$$ with the sup being taken over all rational $$p$$ such that $$p\leq x$$. Equivalently,

$$e^x=\sum_{n=0}^\infty\frac{x^n}{n!},\quad -\infty<x<\infty.$$

**Theorem** (Properties of the logarithmic functions)**.** For positive $$x$$, let $$L(x)=\ln x$$ be the inverse function of $$E(x)=e^x$$. Then for any $$x>0$$ and any real $$\alpha$$, $$E(\alpha L(x))=x^\alpha,$$ where the right-hand side is defined as $$x^\alpha=\sup x^p,x>1$$ with the sup being taken over all rational $$p$$ such that $$p\leq\alpha$$ for $$0<x<1$$, defined $$x^\alpha=(x^{-1})^{-\alpha}$$. Equivalently, 

$$x^\alpha = e^{\alpha\ln x},\quad 0<x<\infty.$$

**Theorem** (Properties of the trigonometric functions)**.** For real $$x$$, denote

$$C(x)=\frac{1}{2}[E(ix)+E(-ix)],\quad S(x)=\frac{1}{2i}[E(ix)-E(-ix)].$$

Then for real $$x$$, $$C(x)=\cos x,S(x)=\sin x$$. And the Euler's formula holds

$$E(ix)=C(x)+iS(x).$$

Or equivalently,

$$e^{ix}=\cos x+i\sin x.$$

> We have $$\displaystyle\cos x=\sum_{k=0}^\infty\frac{(-1)^k x^{2k}}{(2k)!},\sin x=\sum_{k=0}^\infty\frac{(-1)^k x^{2k+1}}{(2k+1)!}$$

#### §2.2 Fourier Series
**Definition** (Fourier series)**.** Let $$\{\phi_n\},n=1,2,3,\cdots$$ be a sequence of complex functions on $$[a,b]$$ such that 

$$\int_a^b\phi_n(x)\overline{\phi_m(x)}dx=0,\quad n\neq m.$$

Then $$\{\phi_n\}$$ is said to be an *orthogonal system* of functions on $$[a,b]$$. In addition, if 

$$\int_a^b|\phi_n(x)|^2\,dx=1$$

for all $$n$$, then $$\{\phi_n\}$$ is said to be *orthonormal.* Let $$\{\phi_n\}$$ be orthonormal on $$[a,b]$$. Put $$\displaystyle \int_a^b f(t)\cdot\overline{\phi_n(t)}dt,n=1,2,3,\cdots$$ and write

$$f(x)\sim\sum_{n=1}^\infty c_n\phi_n(x)$$

We call this series the *Fourier series* of $$f$$ relative to $$\{\phi_n\}$$ and $$c_n$$ the $$n$$th *Fourier coefficient* of $$f$$.    
**Lemma.**  Let $$\{\phi_n\}$$ be orthonormal on $$[a,b]$$. Suppose $$\displaystyle s_n=\sum_{m=1}^n c_m\phi_m(x)$$ is the $$n$$th partial sum of the Fourier series of $$f$$. Then

$$\int_a^b |f-s_n|^2dx\leq\int_a^b |f-t_n|^2dx$$

for any $$\displaystyle t_n(x)=\sum_{m=1}^n\gamma_m\phi_m(x)$$. The equality holds iff $$\gamma_m=c_m,m=1,\cdots,n$$.      
> Among all polynomials of the same degree, $$s_n$$ gives the best possible mean square approximation to $$f$$.

**Theorem** (Bessel's inequality)**.** Suppose $$\{\phi_n\}$$ is orthonormal on $$[a,b]$$. If $$f\in\mathscr{R}$$ on $$[a,b]$$ and if 

$$f(x)\sim\sum_{n=1}^\infty c_n\phi_n(x),$$

then Bessel's inequality holds

$$\sum_{n=1}^\infty|c_n|^2\leq\int_a^b |f(x)|^2dx.$$

In particular, $$\displaystyle\lim_{n\to\infty}c_n=0.$$     
**Definition** (Trigonometric series)**.** Consider the orthonormal system on $$[-\pi,\pi]$$: $$\{(2\pi)^{-1/2}e^{inx}\},n=0,\pm1,\pm2,\cdots$$. Assume that $$f$$ is a Riemann-integrable function on $$[-\pi,\pi]$$. The Fourier series of $$f$$ is given by

$$f(x)\sim\sum_{n=-\infty}^\infty c_ne^{inx},\quad c_n=\frac{1}{2\pi}\int_{-\pi}^\pi f(x)e^{-inx}.$$

Let $$s_N(x)=s_N(f;x)=\displaystyle\sum_{n=-N}^N c_ne^{inx}$$ be the $$N$th partial sum of the Fourier series of $f$$.      
**Definition** (Dirichlet kernel)**.** The *Dirichlet kernel* is defined by

$$D_N(x)=\sum_{n=-N}^N e^{inx}.$$

Then

$$D_N(x)=\frac{\sin\left(N+\frac{1}{2}\right)x}{\sin\left(\frac{1}{2}x\right)}.$$

Furthermore, if $$f\in\mathscr{R}$$ on $$[-\pi,\pi]$$ and $$2\pi$$-periodic, then

$$\begin{align*}s_N(f;x)&=\frac{1}{2\pi}\int_{-\pi}^\pi f(t)D_N(x-t)dt,\\
&=\frac{1}{2\pi}\int_{-\pi}^\pi f(x-t)D_N(t)dt.\end{align*}$$

**Theorem** (Bessel inequality of trigonometric series)**.** Let $$\displaystyle c_n=\frac{1}{2\pi}\int_{-\pi}^\pi f(x)e^{-inx}$$. Then the Bessel's inequality holds:

$$\sum_{n=-\infty}^\infty |c_n|^2\leq\frac{1}{2\pi}\int_{-\pi}^\pi |f(x)|^2dx,$$

and

$$\lim_{n\to\infty}\int_{-\pi}^\pi f(x)\cos nx\,dx=\lim_{n\to\infty}\int_{-\pi}^\pi f(x)\sin nx\,dx=0.$$

> **Remark.** A trigonometric series ofern refers to
>
> $$\frac{a_0}{2}+\sum_{n=1}^\infty (a_n\cos nx+b_n\sin nx),$$
>
> generated by the orthonormal system
>
> $$\frac{1}{\sqrt{2\pi}},\frac{\cos x}{\sqrt{\pi}},\frac{\sin x}{\sqrt{\pi}},\frac{\cos 2x}{\sqrt{\pi}},\frac{\sin 2x}{\sqrt{\pi}}.$$
>

**Theorem** (Pointwise convergence of Fourier series)**.** Suppose $$f\in\mathscr{R}$$ on $$[-\pi,\pi]$$ and $$2\pi$$-periodic. If for some $$x$$, both $$f(x-)$$ and $$f(x+)$$ exist, and there exists a constant $$\delta>0$$ and $$M<\infty$$ such that

$$|f(x+t)-f(x)|\leq M|t|$$

for all $$t\in(-\delta,\delta)$$, then $$\displaystyle\lim_{N\to\infty}s_N(f;x)=f(x).$$      
**Theorem** (Localization theorem)**.** If $$f(t)=g(t)$$ for all $$t$$ in some neighberhood of $$x$$, then as $$N\to\infty$$, 

$$s_N(f;x)-s_N(g;x)=s_N(f-g;x)\to0.$$

**Theorem** (Uniform approximation by trigonometric polynomials)**.** Suppose that $$f$$ is continuous and $$2\pi$$-periodic. Then for any $$\varepsilon>0$$, there is a trigonometric polynomial $$P$$ such that for all $$x$$,

$$|f(x)-P(x)|<\varepsilon.$$

**Theorem** (Uniform convergence of Fourier series)**.** If $$f\in\mathscr{R}$$ and $$2\pi$$-periodic, then $$s_N\to f$$ uniformly.    
**Theorem** (Parseval's identity)**.** Suppose $$f\in\mathscr{R}$$ on $$[-\pi,\pi]$$ and $$2\pi$$-periodic. Let

$$f(x)\sim\sum_{n=-\infty}^\infty c_n e^{inx}.$$

Then

$$\lim_{N\to\infty}\frac{1}{2\pi}\int_{-\pi}^\pi |f(x)-s_N(f;x)|^2dx=0,$$

which gives the Parseval's identity:

$$\frac{1}{2\pi}\int_{-\pi}^\pi |f(x)|^2dx=\sum_{n=-\infty}^\infty|c_n|^2.$$

**Theorem** (Parseval's identity)**.** Suppose $$f$$ is a real function, $$f\in\mathscr{R}$$ on $$[-\pi,\pi]$$ and $$2\pi$$-periodic. Let

$$f(x)\sim\frac{a_0}+\sum_{n=1}^\infty (a_n\cos nx+b_n\sin nx),$$

where

$$\begin{align*}
a_n&=\frac{1}{\pi}\int_{-\pi}^\pi f(t)\cos nt\,dt,\quad n\geq 0;\\
b_n&=\frac{1}{\pi}\int_{-\pi}^\pi f(t)\sin nt\,dt,\quad n\geq 1.\end{align*}$$

The Parseval's identity holds

$$\frac{1}{\pi}\int_{-\pi}^\pi[f(x)]^2=\frac{a_0^2}{2}+\sum_{n=1}^\infty(a_n^2+b_n^2).$$

### <center>3  Functions of Several Variables</center>
#### §3.1 Linear Transformations
**Definition** (Vector operations in a vector space)**.** A nonempty set $$X\subset\mathbb{R}^n$$ is a *vector space* if $$\mathbf{x}+\mathbf{y}\in X$$ and $$c\mathbf{x}\in X$$ for all $$\mathbf{x},\mathbf{y}\in X$$ and for all scalars $$c$$.       
If $$\mathbf{x}_1,\cdots, \mathbf{x}_k\in X$$ and $$c_1,\cdots, c_k$$ are scalars, the vector $$c_1\mathbf{x}_1+\cdots+c_k\mathbf{x}_k$$ is called a *linear combination* of $$\mathbf{x}_1,\cdots, \mathbf{x}_k$$. If $$S\subset\mathbb{R}^n$$ and if $$E$$ is the set of all linear combinations of elments of $$S$$, we say that $$S$$ spans $$E$$, we say that $$S$$ spans $$E$$, or that $$E$$ is the *span* of $$S$$. Every span is a vector space.          
A set consisting of vectors $$\mathbf{x}_1,\cdots,\mathbf{x}_k$$ is said to be *linearly independent* if the relation $$c_1\mathbf{x}_1+\cdots+c_k\mathbf{x}_k=\mathbf{0}$$ implies that $$c_1=\cdots=c_k=0$$.        
If a vector space $$X$$ contains an independent set of $$r$$ vectors but contains no independent set of $$r+1$$ vectors, we say that $$X$$ has *dimension* $$r$$ and write $$\text{dim }X=r.$$ The set consisting of $$\mathbf{0}$$ alone is a vector space and its dimension is $$0$$.      
An independent subset of a vector space which spans $$X$$ is called a *basis* of $$X$$. The *standard basis* of $$\mathbb{R}^n$$ is the set $$\{\mathbf{e}_1,\cdots,\mathbf{e}_n\}.$$       
**Proposition** (Dimension of vector space)**.** Suppose $$X$$ is a vector space.     
&emsp;(1) If $$X$$ is spanned by a set of $$r$$ vectors, then $$\text{dim }X\leq r$$.       
&emsp;(2) If $$\text{dim }X=k$$, then a set $$E$$ of $$k$$ vectors in $$X$$ spans $$X$$ iff $$E$$ is independent.         
**Definition** (Linear transformation)**.** A mapping $$A$$ if a vector space $$X$$ into a vector $$Y$$ is a *linear transformation* if 

$$A(c_1\mathbf{x}_1+c_2\mathbf{x}_2)=c_1A\mathbf{x}_1+c_2A\mathbf{x}_2$$

for all $$\mathbf{x}_1,\mathbf{x}_2\in X$$ and all scalars $$c_1,c_2$$.      
A linear transformation of $$X$$ into $$X$$ is called a *linear operator* on $$X$$.      
If $$A$$ is a linear operator on $$X$$ which is one-to-one and onto, then we say that $$A$$ is *invertible* and define the inverse $$A^{-1}$$ on $$X$$ by requiring $$A^{-1}(A\mathbf{x})=\mathbf{x}$$ for all $$\mathbf{x}\in X$$.    
> The identity operator $$I$$ is linear and invertible.       
> A linear operator on a vector space $$X$$ is one-to-one iff it is onto.     
Denote $$L(X,Y)$$ the set of all linear transformations of the vector space $$X$$ into the vector space $$Y$$. For simplicity, write $$L(X)$$ for $$L(X,X)$$.     
&emsp;(1) For $$A_1,A_2\in L(X,Y)$$ and $$c_1,c_2$$ are two scalars, define $$c_1A_1+c_2A_2$$ by $$(c_1A_1+c_2A_2)\mathbf{x}=c_1A_1\mathbf{x}+c_2A_2\mathbf{x},\mathbf{x}\in X$$. And $$c_1A_1+c_2A_2\in L(X,Y)$$.      
&emsp;(2) If $$X,Y,Z$$ are vector spaces, and if $$A\in L(X,Y)$$ and $$B\in L(Y,Z)$$, define their product $$BA$$ to be the composition of $$A$$ and $$B$$: $$(BA)\mathbf{x}=B(A\mathbf{x}),\mathbf{x}\in X.$$ And $$BA\in L(X,Z)$$.      
**Proposition** (Norm of linear transformtaions and its properties)**.** 