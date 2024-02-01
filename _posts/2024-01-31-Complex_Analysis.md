---
layout: post
mathjax: true
categories: media
title: "Complex Analysis"
---

![Static Badge](https://img.shields.io/badge/Category-Notes-blue) ![Static Badge](https://img.shields.io/badge/Subject-Mathematics-forestgreen) ![Static Badge](https://img.shields.io/badge/In_progress-orange) 

### <center>1  The Complex Plane</center>
## §1.1 Complex Numbers
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

**Definition.** The *complex conjugate* is the function $$\mathbf{C}\to\mathbf{C}$$ defined by $$\bar{a+bi}=a-bi.$$    
**Lemma.** If $$z$$ is real, then $$\bar z=z$$. If $$z$$ is purely imaginary, then $$\bar z=-z$$.    
 

**Theorem** (de Moivre)**.** $$\theta\in\mathbb{R},n\in\mathbf{Z}.$$ Then $$(\cos\theta+i\sin\theta)^n=\cos n\theta+i\sin n\theta.$$

