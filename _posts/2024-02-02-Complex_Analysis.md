---
layout: post
mathjax: true
categories: media
title: "Complex Analysis"
---

![Static Badge](https://img.shields.io/badge/Category-Notes-blue) ![Static Badge](https://img.shields.io/badge/Subject-Mathematics-forestgreen) ![Static Badge](https://img.shields.io/badge/In_progress-orange) 

### <center>1  The Complex Plane</center>
#### §1.1 Complex Numbers
**Definition.** Consider the real vector space $$\mathbb{R}^2$$ and a multiplication $$(a,b)(c,d)=(ac-bd,ad+bc)$$ for all $$a,b,c,d\in\mathbb{R}$$.
* Each element $$(a,b)$$ is called a *complex number*.
* $$(1,0)$$ is written as $$1$$, and $$(0,1)$$ is written as $$i$$. Thus $$(a,b)$$ is written as $$a+bi$$.
* The *set of all complex number* is denoted by $$\mathbb{C}=\{a+bi:a,b\in\mathbb{R}\}$$.

**Definition.** Given a complex number $$z=a+bi$$, $$a$$ is called the *real part* of $$z$$ and denoted by $$\text{Re}z=a$$, and $$b$$ is called the *imaginary part* of $$z$$ and denoted by $$\text{Im}z=b.$$

Arithmetic operations of complex numbers:

$$\begin{align*}
z+w &= (a+c)+(b+d)i,\\
z-w &= (a-c)+(b-d)i,\\
zw &=(ac-bd)+(ad+bc)i,\\
\frac{z}{w} &=\frac{ac+bd}{c^2+d^2}+\frac{bc-ad}{c^2+d^2}i,\quad w\neq 0.
\end{align*}$$

**Lemma.** $$\mathbf{C}$$ equipped with the above addition and multiplication is a field.

> Note that $$(\cos\theta+i\sin\theta)(\cos\phi+i\sin\theta)=\cos(\theta+\phi)+i\sin(\theta+\phi).$$

**Definition.** The *complex conjugate* is the function $$\mathbb{C}\to\mathbb{C}$$ defined by $$\widebar{a+bi}=a-bi.$$    
**Lemma.** If $$z$$ is real, then $$\bar z=z$$. If $$z$$ is purely imaginary, then $$\bar z=-z$$.    
**Lemma.** Given two complex numbers $$z,w\in\mathbb{C}$$, we have $$\widebar{z+w}=\bar{z}+\bar{w},\widebar{z-w}=\bar{z}-\bar{w},\widebar{zw}=\bar{z}\bar{w},\widebar{\frac{z}{w}}=\frac{\bar z}{\bar w}.$$ (The complex conjugate is a field isomorphism.)    
**Lemma.** Given a complex number $$z\in\mathbb{C}$$, we have $$z+\bar z=2\text{Re}z,z-\bar z=2i\text{Im}z.$$     
**Lemma.** For complex number $$z$$, $$z\bar z$$ is a non-negative real number and $$z\bar z=0$$ only when $$z=0$$.    
**Definition.** For $$z=a+bi\in\mathbb{C}$$, the *absolute value* (*modulus*) of $$z$$ is the non-negative real number defined by 

$$|z|=\sqrt{z\bar z}=\sqrt{a^2+b^2}.$$

**Lemma.** $$z\in\mathbb{C}$$, then $$|\text{Re}z|\leq|z|,|\text{Im}z|\leq|z|,|\bar z|=|z|$$.     
**Theorem** (Triangle inequality)**.** $$z,w\in\mathbb{C},|z+w|\leq|z|+|w|.$$     
**Corollary** (Triangle inequality)**.** $$z,w\in\mathbb{C}, \left||z|-|w|\right|\leq|z-w|.$$     
**Lemma.** For every $$z\in\mathbb{C}\backslash\{0\}$$, there is a unique $$\theta\in(-\pi,\pi]$$ such that $$z=|z|(\cos\theta+i\sin\theta)$$.     
**Definition.** $$\theta$$ is called the *principal argument* of $$z$$, denoted as $$\text{Arg}z=\theta.$$ The set of all *arguments* of $$z$$ is denoted as $$\text{arg}z=\{\theta+2n\pi:n\in\mathbb{Z}\}$$.     
**Theorem** (de Moivre)**.** $$\theta\in\mathbb{R},n\in\mathbb{Z}.$$ Then $$(\cos\theta+i\sin\theta)^n=\cos n\theta+i\sin n\theta.$$    
**Remark.** The set of all $$n$$th roots of a complex number $$a$$ is

$$\left\{\sqrt[n]{|a|}\left(\cos\frac{\text{Arg}a+2k\pi}{n}+i\sin\frac{\text{Arg}a+2k\pi}{n}\right):k=0,1,2,\cdots,n-1\right\}.$$

**Theorem** (Viète)**.** Let $$p$$ be a polynomial of degree $$n$$: $$p(z)=a_nz^n+a_{n-1}z^{n-1}+\cdots+a_1z+a_0$$. Suppose $$p$$ can be factored as $$p(z)=a_n(z-w_1)(z-w_2)\cdots(z-w_n),$$ so that $$w_1,w_2,\cdots,w_n$$ are $$n$$ roots of $$p$$. Then we have 

$$\begin{align*}\displaystyle w_1+w_2+\cdots+w_n&=-\frac{a_{n-1}}{a_n},\\
\displaystyle \sum_{j\neq k}w_jw_k&=\frac{a_{n-2}}{a_n},\\
&\vdots\\
w_1w_2\cdots w_n=(-1)^n\frac{a_0}{a_n}.
\end{align*}$$

>
> $$\sum_{1\leq i_1<i_2<\cdots i_k< n}\left(\prod_{j=1}^k w_{i_j}\right)=(-1)^k\frac{a_{n-k}}{a_n}.$$
>

#### §1.2 Sequence and series of complex numbers
**Definition.** (Convergence)Let $$(a_n)_{n\in\mathbb{N}}$$ be a sequence of complex numbers and $$L\in\mathbb{C}$$. The sequence *converges* to $$L$$ if $$\forall\epsilon>0$$, $$\exists N\in\mathbb{N}$$ such that $$n\geq N\Rightarrow|a_n-L|<\epsilon$$. We say $$L$$ is the *limit* of the sequence and $$\displaystyle\lim_{n\to\infty}a_n=L.$$    
**Lemma.** Let $$(a_n)$$ and $$(b_n)$$ be sequences of complex numbers and let $$L,M\in\mathbb{C}$$. Suppose that $$(a_n)$$ and $$(b_n)$$ *both converge* with $$\lim_{n\to\infty}=L$$ and $$\lim_{n\to\infty}b_n=M$$. Then
* $$(a_n+b_n)$$ and $$(a_n-b_n)$$ both converge and $$\displaystyle\lim_{n\to\infty}(a_n\pm b_n)=L\pm M$$.
* $$(a_nb_n)$$ converges, and $$\displaystyle \lim_{n\to\infty} a_nb_n=LM$$.
* If $$M\neq 0$$, then $$\left(\frac{a_n}{b_n}\right)$$ also converges and $$\displaystyle \lim_{n\to\infty}\frac{a_n}{b_n}=\frac{L}{M}$$.

**Lemma.** Let $$(a_n)$$ be a sequence of complex numbers and let $$L\in\mathbb{C}$$. Then $$\displaystyle \lim_{n\to\infty} a_n=L$$ iff $$\displaystyle\lim_{n\to\infty}\text{Re}a_n=\text{Re}L$$ and $$\displaystyle\lim_{n\to\infty}\text{Im}a_n=\text{Im}L$$ as sequences of real numbers.      
**Definition** (Cauchy sequence)**.**Let $$(a_n)_{n\in\mathbb{N}}$$ be a sequence of complex numbers. $$(a_n)$$ is called a *Cauchy sequence* if for each $$\epsilon>0$$, there exists a positive integer $$N$$ such that 

$$\forall m,n\geq N,\quad|a_n-a_m|<\epsilon.$$

**Theorem** (Completeness of complex numbers)**.** Each Cauchy sequence of complex numbers converges to some complex number.     
**Definition** (Series)**.** Let $$(a_n)$$ be sequence. The sequence 