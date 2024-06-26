---
layout: post
mathjax: true
categories: media
title: "Complex Analysis"
---

![Static Badge](https://img.shields.io/badge/Category-Notes-blue) ![Static Badge](https://img.shields.io/badge/Subject-Mathematics-forestgreen) ![Static Badge](https://img.shields.io/badge/Completed-red) 

(Symbol ★ means that the theorem is important.)


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

**Lemma.** $$\mathbb{C}$$ equipped with the above addition and multiplication is a field.

> Note that $$(\cos\theta+i\sin\theta)(\cos\phi+i\sin\theta)=\cos(\theta+\phi)+i\sin(\theta+\phi).$$

**Definition.** The *complex conjugate* is the function $$\mathbb{C}\to\mathbb{C}$$ defined by $$\overline{a+bi}=a-bi.$$    
**Lemma.** If $$z$$ is real, then $$\bar z=z$$. If $$z$$ is purely imaginary, then $$\bar z=-z$$.    
**Lemma.** Given two complex numbers $$z,w\in\mathbb{C}$$, we have $$\overline{z+w}=\bar{z}+\bar{w},\overline{z-w}=\bar{z}-\bar{w},\overline{zw}=\bar{z}\bar{w},\overline{\frac{z}{w}}=\frac{\bar z}{\bar w}.$$ (The complex conjugate is a field isomorphism.)    
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

**Lemma.** Let $$(a_n)$$ be a sequence of complex numbers and let $$L\in\mathbb{C}$$. Then $$\displaystyle \lim_{n\to\infty} a_n=L$$ iff $$\displaystyle\lim_{n\to\infty}\text{Re }a_n=\text{Re }L$$ and $$\displaystyle\lim_{n\to\infty}\text{Im }a_n=\text{Im }L$$ as sequences of real numbers.      
**Definition** (Cauchy sequence)**.**Let $$(a_n)_{n\in\mathbb{N}}$$ be a sequence of complex numbers. $$(a_n)$$ is called a *Cauchy sequence* if for each $$\epsilon>0$$, there exists a positive integer $$N$$ such that 

$$\forall m,n\geq N,\quad|a_n-a_m|<\epsilon.$$

**Theorem** (Completeness of complex numbers)**.** Each Cauchy sequence of complex numbers converges to some complex number.     
**Definition** (Series)**.** Let $$(a_n)$$ be sequence. The sequence $$\displaystyle(\sum_{k=1}^na_k)_{n\in\mathbb{N}}$$ is called a *series*. This series and its limit (if exists) are denoted as $$\displaystyle\sum_{k=1}^\infty a_k.$$      
**Theorem** (Geometric series)**.** Let $$a$$ and $$z$$ be a pair of complex numbers with $$a\neq 0$$. Let $$a_n=az^{n-1}$$, then $$(a_n)$$ is a geometric sequence. The geometric series $$\displaystyle \sum_{k=1}^\infty a_k=a\sum_{k=0}^\infty z^k$$ converges iff $$|z|<1$$. In this case $$\displaystyle \sum_{k=1}^\infty a_k=\frac{a}{1-z}.$$        
**Lemma** (Term test for convergence)**.** If the complex series $$\displaystyle \sum_{k=1}^\infty a_k$$ converges, then $$\displaystyle\lim_{n\to\infty} a_n=0$$. If $$(a_n)$$ does not converge to $$0$$, then the series $$\displaystyle \sum_{k=1}^\infty a_k$$ diverges.    
**Definition** (Absolutely and conditionally convergence)**.** $$\displaystyle \sum_{k=1}^\infty a_k$$ *converges absolutely* if the series $$\displaystyle \sum_{k=1}^\infty |a_k|$$ converges. Otherwise $$\displaystyle \sum_{k=1}^\infty a_k$$ *converges conditionally*.     
**Theorem** (Absolute convergence test)**.** If a series of complex numbers $$\displaystyle \sum_{k=1}^\infty a_k$$ converges absolutely, then it converges.    
**Theorem** (Root test)**.** Let $$(a_n)$$ be a sequence of complex numbers.     
&emsp;1. If $$\displaystyle\lim_{n\to\infty}\sqrt[n]{|a_n|}<1$$, then $$\sum_{k=1}^\infty a_k$$ converges absolutely.    
&emsp;2. If $$\displaystyle\lim_{n\to\infty}\sqrt[n]{|a_n|}>1$$, then $$\sum_{k=1}^\infty a_k$$ diverges.      
**Theorem** (Ratio test)**.** Suppose that $$a_n\neq 0$$ for every sufficiently large $$n$$.     
&emsp;1. If $$\displaystyle\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|<1$$, then $$\sum_{k=1}^\infty a_k$$ converges absolutely.    
&emsp;2. If $$\displaystyle\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|>1$$, then $$\sum_{k=1}^\infty a_k$$ diverges.      
**Definition** (Complex exponential)**.** Let $$z$$ be a complex number. The *exponential* of $$z$$, denoted by $$e^z$$ or $$\exp z$$ is defined by

$$e^z=\sum_{k=0}^\infty\frac{z^k}{k!}.$$

**Theorem** (Euler's formula)**.** Let $$\theta\in\mathbb{R}$$. Then

$$e^{i\theta}=\cos\theta+i\sin\theta.$$

**Corollary** (Euler's identity)**.** $$e^{i\pi}+1=0$$. 
> Any complex number could be written as $$z=re^{i\theta}.$$

**Theorem.** $$z,w\in\mathbb{C}. e^{z+w}=e^ze^w.$$      
**Corollary.** Let $$z$$ be a complex number. Then      
&emsp;1. $$(e^z)^n=e^{nz}$$ for every integer $$n$$.    
&emsp;2. $$e^{x+iy}=e^xe^{iy}=e^x(\cos y+i\sin y)$$ for every $$x,y\in\mathbb{R}$$.     
&emsp;3. $$e^{z+2\pi i}=e^z.$$ That is $$\exp$$ is a periodic function with period $$2\pi i$$.     
&emsp;4. $$|e^z|=e^{\text{Re }z}.$$        
&emsp;5. $$e^z\neq 0.$$     
**Definition.** $$a$$ is a positive real number and $$z$$ is a complex number. Define $$a^z=e^{(\ln a)z}$$.    
**Corollary.** Let $$a,b$$ be positive real numbers and $$z,w$$ be complex numbers. Then      
&emsp;1. $$(a^z)^n=a^{nz}$$ for every integer $$n$$.    
&emsp;2. $$a^{z+w}=a^za^w.$$       
&emsp;3. $$|a^z|=a^{\text{Re }z}.$$     
&emsp;4. $$a^z\neq 0$$.      
&emsp;5. $$(ab)^z=a^zb^z.$$  


#### §1.3 Point-Set Topology of $$\mathbb{C}$$
**Definition.** Let $$a\in\mathbb{C}$$ and $$r>0$$.

$$\begin{align*}
D(a;r) &=\{z\in\mathbb{C}:|z-a|<r\},\\
\overline{D(a;r)} &=\{z\in\mathbb{C}:|z-a|\leq r\},\\
\partial D(a,r) &=\{z\in\mathbb{C}:|z-a|<r\},
\end{align*}$$ 

are the *open disk*, *closed disk* and *circle* centered at $$a$$ with radius $$r$$ respectively.      
**Definition** (Interior, exterior and boundary)**.**Let $$U$$ be a set of $$\mathbb{C}$$ and $$z\in\mathbb{C}$$ be a complex number.      
&emsp;1. $$z$$ is an *interior point* of $$U$$ if it is the center of a disk which is contained entirely in $$U$$, i.e.$$\exists\varepsilon>0$$ such that $$D(z;\varepsilon)\subseteq U.$$ The set of all interior points of $$U$$ is called the *interior* of $$U$$, denoted by $$U^\circ$$.       
&emsp;2. $$z$$ is called a *boundary point* of $$U$$ if every disk centered at $$z$$ contains some point in $$U$$ and some point not in $$U$$, i.e. $$\forall \varepsilon>0$$, $$D(z,\varepsilon)\cap$$ and $$D(z;\varepsilon)\cap(\mathbb{C}\backslash U)$$ are non-empty. The set of all boundary points of $$U$$ is called the *boundary* of $$U$$ and is denoted as $$\partial U$$.         
&emsp;3. $$z$$ is called an *exterior point* of $$U$$ if it is an interior point of $$\mathbb{C}\backslash U$$, i.e. $$\exists\varepsilon>0$$ such that $$D(z;\varepsilon)\subseteq \mathbb{C}\backslash U.$$ The set of all exterior points of $$U$$ is called the *exterior* of $$U$$ and is denoted as $$(\mathbb{C}\backslash U)^\circ.$$

> **Remark.**    
> If $$z$$ is an interior point of $$U$$, then $$z\in U$$ ($$U^\circ\subseteq U$$).     
> If $$z$$ is boundary point of $$U$$, then $$z$$ may or may not belong to $$U$$.       
> If $$z$$ is an exterior point of $$U$$, then $$z\not\in U$$.     
> The interior, boundary and the exterior of $$U$$ form a disjoint partition of $$\mathbb{C}$$.

**Definition** (Open and close)**.** $$U$$ is a subset of $$\mathbb{C}$$.     
&emsp;1. $$U$$ is *open* if every point in $$U$$ is an interior point of $$U$$, i.e. $$U\subseteq U^\circ$$.      
&emsp;2. $$U$$ is *closed* if it contains all its boundary points, i.e. $$\partial U\subseteq U.$$      
> **Remark:** Openness and closedness are not opposite concepts.

**Theorem.** Let $$U$$ be a subset of $$\mathbb{C}$$. $$U$$ is closed iff $$\mathbb{C}\backslash U$$ is open.      
**Theorem.** 1. The *union* of finitely or infinitely many open sets is open.    
&emsp; 2. The *intersection* of finitely many open sets is open.       
**Corollary.** 1. The *intersection* of finitely or infinitely many closed sets is closed.    
&emsp; 2. The *intersection* of finitely many closed sets is closed.     
**Lemma.** Let $$U$$ be a subset of $$\mathbb{C}$$. $$U$$ is closed iff for every convergent sequence $$(a_n)$$ of complex numbers in $$U$$, theh limit $$a$$ is also in $$U$$.      
**Definition** (Closure)**.**Let $$U$$ be a subset of $$\mathbb{C}$$. The *closure* of $$U$$ is the set $$\bar U=U\cup \partial U.$$        
**Definition** (Open cover)**.** Let $$U$$ be a subset of $$\mathbb{C}$$.      
&emsp;1. An *open cover* of $$U$$ is a collection of open sets $$\{U_\alpha\}_{\alpha\in I}$$ indexed by a set, such that $$U\subseteq\bigcup_{\alpha\in I}U_\alpha.$$     
&emsp;2. A *subcover* of this open cover is a subcollection $$\{U_\alpha\}_{\alpha\in J}$$ where $$J\subseteq I$$, such that $$U\subseteq\bigcup_{\alpha\in J}U_\alpha.$$     
&emsp;3. If the index set is finite, we say that the open cover is *finite*.     
**Definition** (Compact)**.** Let $$U$$ be a subset of $$\mathbb{C}$$. $$U$$ is *compact* if every open cover of $$U$$ has a finite subcover.     
**Definition** (Bounded)**.** Let $$U$$ be a subset of $$\mathbb{C}$$. $$U$$ is *bounded* if it is completely contained in some disk, i.e. $$\exists r>0$$ such that $$U\subseteq D(0;r).$$      
**Theorem.** $$U$$ be a subset of $$\mathbb{C}$$. The following statement are equivalent.     
&emsp;1. $$U$$ is compact.       
&emsp;2. $$U$$ is closed and bounded.       
&emsp;3. Every sequence in $$U$$ has a subsequence which converges to some limit in $$U$$.    
> **Remark.** A subset of $$\mathbb{C}$$ is *compact* iff it is closed and bounded.      

**Theorem** (Cantor intersection theorem)**.** Let $$K_1,K_2,\cdots$$ be non-empty compact subsets of $$\mathbb{C}$$ such that $$K_{n+1}\subseteq K_n$$ for every $$n\in\mathbb{N}$$. Then

$$\bigcap_{n=1}^\infty K_n\neq \emptyset.$$

> That is, the nested non-empty compact sets is non-empty.

**Definition** (Connect)**.** Let $$U$$ be a subset of $$\mathbb{C}$$.    
&emsp;1. $$U$$ is *disconnected* if it is contained separately in two disjoints open sets, i.e. there exist two disjoint open sets $$V$$ and $$W$$, $$V\cap W=\emptyset$$, such that

$$U\cap V\neq\emptyset,\quad U\cap W\neq\emptyset,\quad U\subseteq V\cup W.$$

&emsp;2. $$U$$ is *connected* if $$U$$ is not disconnected.       
**Definition.** Let $$U$$ be a subset of $$\mathbb{C}$$. $$U$$ is *polygonally path-connected* if each pair of points in $$U$$ can be joined by a "polygonal path" in $$U$$, i.e. a path consisting of finitely many line segments contained in $$U$$.    
**Theorem.** Let $$U$$ be an open subset of $$\mathbb{C}$$. Then $$U$$ is connected iff $$U$$ is polygonally path-connected.       
**Definition.** Let $$U$$ be a subset of $$\mathbb{C}$$. A non-empty subset $$V\subseteq U$$ is called a *connected component* of $$U$$ if $$V$$ is a "maximal" connected subset of $$U$$, i.e.    
&emsp; 1. $$V$$ is connected;    
&emsp; 2. Whenever $$W$$ is a connected set such that $$V\subseteq W\subseteq U, V=W$$.     
**Lemma.** Let $$U$$ be a subset of $$\mathbb{C}$$. If $$V$$ and $$W$$ are connected components of $$U$$, then either $$V=W$$ or $$V\cap W=\emptyset$$.    
**Lemma.** Every subset of $$\mathbb{C}$$ is the union of its connected components. 



### <center>2  Holomorphic Functions</center>
#### §2.1 Functions of a Complex Variable
**Definition** (Complex function)**.** A *function of a complex variable* (*complex function*) is a function $$f:U\to\mathbb{C}$$ whose domain $$U$$ is a subset of $$\mathbb{C}$$.    
> $$f(x+iy)=u(x,y)+iv(x,y)$$, $$u$$ and $$v$$ are called the *real part* and the *imaginary part* of the function $$f$$.

**Definition.** Let $$U$$ and $$V$$ be sets and $$f:U\to V$$ be a function.    
&emsp; 1. Given a set $$A\subseteq U$$, the *direct image* of $$A$$ via $$f$$ is the set 

$$f(A)=\{w\in V:w=f(z)\text{ for some } z\in A\}.$$

&emsp; 2. Given a set $$B\subseteq U$$, the *direct image* of $$B$$ via $$f$$ is the set 

$$f^{-1}(B)=\{z\in U:f(z)\in B\}.$$

#### §2.2 Limits and Continuity
**Definition** (Limit)**.** Let $$U\in\mathbb{C}$$ be an open set, let $$a\in\bar{U}$$, let $$f:U\to\mathbb{C}$$ be a function and let $$L$$ be a complex number. If for any $$\varepsilon>0$$, there exists $$\delta>0$$ such that

$$|f(z)-L|<\varepsilon,\quad \text{whenever }z\in U\text{ and }0<|z-a|<\delta,$$

then $$L$$ is a *limit* of $$f(z)$$ as $$z$$ tends to $$a$$.    
**Lemma.** The limit of a function is unique. Write

$$\lim_{z\to a}f(z)=L.$$

**Lemma** (Sequential limit theorem)**.** Let $$U\subseteq\mathbb{C}$$ be an open set, let $$a\in\bar U$$, let $$f:U\to\mathbb{C}$$ be a function and let $$L$$ be a complex number. Then the following statements are equivalent.    
&emsp;1. $$\displaystyle\lim_{z\to a}f(z)=L.$$    
&emsp;2. For every sequence $$(a_n)$$ in $$U\backslash\{a\}$$ that converges to $$a$$, we have $$\displaystyle\lim_{n\to\infty}f(a_n)=L.$$     
**Theorem.** Let $$U\in\mathbb{C}$$ be an open set, let $$a\in\bar{U}$$, let $$f,g:U\to\mathbb{C}$$ be functions. If $$\displaystyle\lim_{z\to a}f(z)=L$$ and $$\displaystyle\lim_{z\to a}g(z)=M$$ both exists as complex numbers. Then    
&emsp;1. $$\displaystyle\lim_{z\to a}[f(z)\pm g(z)]=L\pm M.$$     
&emsp;2. $$\displaystyle\lim_{z\to a} f(z)g(z)=LM.$$     
&emsp;3. $$\displaystyle\lim_{z\to a}\frac{f(z)}{g(z)}=\frac{L}{M}$$ if $$M\neq 0$$.    
> **Two-path test.** If a function has different limits along two different paths of approach to the same point, then the limit doesn't exist (a direct consequence of the sequential limit theorem). Can also be rephrased using the $$\varepsilon-\delta$$ language.        

**Definition** (Infinite limit)**.** Let $$U\subseteq\mathbb{C}$$ be an open set, let $$a\in\bar U$$, let $$f:U\to\mathbb{C}$$ be a function. If for any $$\varepsilon>0$$, there exists $$\delta >0$$ such that

$$|f(z)|>\varepsilon,\quad \text{whenever }z\in U\text{ and }0<|z-a|<\delta,$$

then we say that $$f(z)$$ has *infinite limit* as $$z$$ tends to $$a$$, or 

$$\lim_{z\to a}f(z)=\infty.$$

**Theorem.** Let $$U\subseteq\mathbb{C}$$ be an open set, let $$a\in\bar U$$, let $$f:U\to\mathbb{C}$$ be a function. Then

$$\lim_{z\to a}f(z)=\infty\quad\text{iff}\quad\lim_{z\to a}\frac{1}{f(z)}=0.$$

**Definition** (Limit at infinity)**.** Let $$U\subseteq\mathbb{C}$$ be an open set, let $$a\in\bar U$$, let $$f:U\to\mathbb{C}$$ be a function and let $$L$$ be a complex number. If for any $$\varepsilon>0$$, there exists $$\delta >0$$ such that

$$|f(z)-L|<\varepsilon,\quad \text{whenever }z\in U\text{ and }|z|>\delta,$$

then we say $$L$$ is the *limit* of $$f(z)$$ as $$z$$ tends to $$\infty$$, or

$$\lim_{z\to\infty}f(z)=L.$$

If for any $$\varepsilon>0$$, there exists $$\delta >0$$ such that

$$|f(z)|>\varepsilon,\quad \text{whenever }z\in U\text{ and }|z|>\delta,$$

then we say $$f(z)$$ has *infinite limit* as $$z$$ tends to $$\infty$$, or

$$\lim_{z\to\infty}f(z)=\infty.$$

**Theorem.** Let $$U\subseteq\mathbb{C}$$ be an open set, let $$a\in\bar U$$, let $$f:U\to\mathbb{C}$$ be a function and let $$L$$ be a complex number. Then

$$\lim_{z\to\infty}f(z)=L\quad\text{iff}\quad\lim_{z\to 0}f\left(\frac{1}{z}\right)=L,$$

and

$$\lim_{z\to\infty}f(z)=0\quad\text{iff}\quad\lim_{z\to 0}\frac{1}{f(1/z)}=0.$$

**Definition** (Continuity)**.** Let $$U\subseteq\mathbb{C}$$ be an open set and let $$f:U\to\mathbb{C}$$ be a function.     
&emsp;1. Given $$a\in\bar U$$, we say that $$f$$ is *continuous* at $$a$$ if

$$\lim_{z\to a}f(z)=f(a).$$

i.e. for any $$\varepsilon>0,\exists\delta>0$$ such that $$|f(z)-f(a)|<\varepsilon$$ whenever $$z\in\bar U,|z-a|<\delta$$.    
&emsp;2. For a subset of $$V\subseteq\bar U$$, we say that $$f$$ is *continuous* on $$V$$ if it is continuous at every point in $$V$$.      
&emsp;3. $$f$$ is *continuous* if it is continuous on its whole domain.       
**Corollary.** Let $$U\subseteq\mathbb{C}$$ be an open set and let $$f,g:U\to\mathbb{C}$$ be continuous functions. Then $$f+g,f-g,fg$$ are all continuous, and $$\frac{f}{g}$$ is continuous at every number except at those $$a\in\bar U$$ where $$g(a)=0$$.    
> Note that $$\text{Re},\text{Im}$$, complex conjugate and absolute value are all continuous.    
> The inverse image of an open set via a continuous function is open.    
> The inverse image of an closed set via a continuous function is closed.    
> The direct image of an compact set via a continuous function is compact.     
> The direct image of an connected set via a continuous function is connected.      

**Lemma.** A function $$f:\mathbb{C}\to \mathbb{C}$$ is continuous iff for every open set $$U$$, $$f^{-1}(U)$$ is open.    
**Corollary.** Let $$f:\mathbb{C}\to\mathbb{C}$$ be a continuous function and let $$a\in\mathbb{C}$$. If $$f(a)\neq 0$$, then there exists $$r<0$$ such that $$f(z)\neq 0$$ for every $$z\in D(a;r)$$.    
**Corollary.** A function $$f:\mathbb{C}\to\mathbb{C}$$ is continuous iff for every closed set $$U$$, $$f^{-1}(U)$$ is closed.    
**Corollary.** The composition of continuous function is continuous.    
**Theorem** (Extreme value theorem)**.** Let $$K$$ be a compact subset of $$\mathbb{C}$$ and $$f:K\to\mathbb{C}$$ be a continuous function. Then $$f(K)$$ is compact.      
**Corollary** (Extreme value theorem)**.** Let $$K$$ be a compact subset of $$\mathbb{C}$$. If $$g:K\to\mathbb{R}$$ is a continuous function, then there exists $$a\in K$$ such that $$g(z)\leq g(a)$$ for all $$z\in K$$. In particular, if $$f:K\to\mathbb{C}$$ is a continuous function, then there exists $$a\in K$$ such that $$|f(z)|\leq |f(a)|$$ for all $$z\in K$$.    
**Definition** (Uniform continuous)**.** Let $$U\subseteq\mathbb{C}$$ and let $$f:U\to\mathbb{C}$$ be a function. We say that $$f$$ is *uniformly continuous*
on $$U$$ if for any $$\varepsilon>0$$, there exists $$\delta>0$$ such that

$$|f(z)-f(w)|<\epsilon,\quad\text{whenever }z,w\in U\text{ and }|z-w|<\delta.$$

**Theorem.** Let $$K$$ be a compact subset of $$\mathbb{C}$$ and $$f:K\to\mathbb{C}$$ be a continuous function. Then $$f$$ is uniformly continuous.     
**Theorem** (Intermediate value theorem)**.** Let $$U$$ be a connected subset of $$\mathbb{C}$$ and $$f:U\to\mathbb{C}$$ be a continuous function. Then $$f(U)$$ is connected.

#### §2.3 Complex Differentiability, Holomorphic Functions
**Definition** (Differentiability)**.** Let $$U\subseteq\mathbb{C}$$ be an open set, let $$a\in U$$ and $$f:U\to \mathbb{C}$$ be a function. We say that $$f$$ is *(complex) differentiable* at $$a$$ if the limit

$$\lim_{z\to a}\frac{f(z)-f(a)}{z-a}=\lim_{h\to 0}\frac{f(a+h)-f(a)}{h}$$

exists as a complex number. This limit is called the *derivative* of $$f$$ at $$a$$, and is denoted as $$f'(a)$$.    
**Lemma.** Let $$U\subseteq\mathbb{C}$$ be an open set, let $$a\in U$$ and $$f:U\to \mathbb{C}$$ be a function which is differentiable at $$a$$. Then $$f$$ is continuous at $$a$$.    
**Lemma.** Let $$U\subseteq\mathbb{C}$$ be an open set, identified as a subset of $$\mathbb{R}^2$$. Let $$(a_1,a_2)\in U$$ and let $$u,v:U\to\mathbb{R}$$ be functions of two real variables. If the function $$f:U\to\mathbb{C}$$ defined by

$$f(x+iy)=u(x,y)+iv(x,y)$$

is differentiable at $$a=a_1+ia_2$$, then    
&emsp;(i) The partial derivative of $$u$$ and $$v$$ both exist at $$(a_1,a_2)$$ and satisfy 

$$\frac{\partial u}{\partial x}(a_1,a_2)=\frac{\partial v}{\partial y}(a_1,a_2),\quad \frac{\partial v}{\partial x}(a_1,a_2)=-\frac{\partial u}{\partial y}(a_1,a_2).$$

&emsp;(ii) $$u$$ and $$v$$ are both (real) differentiable at $$(a_1,a_2)$$.       
> **Remark.** The PDE $$\displaystyle\frac{\partial u}{\partial x}=\frac{\partial v}{\partial y},\quad \frac{\partial v}{\partial x}=-\frac{\partial u}{\partial y}$$ are called **Cauchy-Riemann equations**. If those equations are not satisifed at some point, then $$f$$ is not differentiable at these points.      
> The logic is: solving the PDEs, find the solutions, then at the other points in $$\mathbb{C}$$ are not differentiable.

**Lemma.** Let $$U\subseteq\mathbb{C}$$ be an open set, identified as a subset of $$\mathbb{R}^2$$. Let $$(a_1,a_2)\in U$$ and let $$u,v:U\to\mathbb{R}$$ be functions of two real variables. If    
&emsp;(i) $$u$$ and $$v$$ satisfy the Cauchy-Riemann equations at $$(a_1,a_2)$$, and     
&emsp;(ii) $$u$$ and $$v$$ are both (real) differentiable at $$(a_1,a_2)$$,     
then the function $$f:U\to\mathbb{C}$$ defined by $$f(x+iy)=u(x,y)+iv(x,y)$$ is differentiable at $$a=a_1+ia_2$$.    
**Corollary.** Let $$U\subseteq\mathbb{C}$$ be an open set, identified as a subset of $$\mathbb{R}^2$$. Let $$(a_1,a_2)\in U$$ and let $$u,v:U\to\mathbb{R}$$ be functions of two real variables. If the function $$f:U\to\mathbb{C}$$ defined by $$f(x+iy)=u(x,y)+iv(x,y)$$ is differentiable at $$a=a_1+ia_2$$, then its derivative at $$a$$ is given by

$$f'(a)=u_x(a_1,a_2)+iv_x(a_1,a_2)=u_x(a_1,a_2)-iu_y(a_1,a_2).$$

> **Theorem.** Let $$u$$ be a function of two real variables and let $$D$$ be an open disk in $$\mathbb{R}^2$$. If the partial derivative $$u_x$$ and $$u_y$$ are continuous on $$D$$, then $$u$$ is differentiable at every point in $$D$$.    

**Definition** (Holomorphic function)**.** Let $$U\subseteq\mathbb{C}$$ be an open set and let $$f:U\to\mathbb{C}$$ be a function. We say that $$f$$ is *holomorphic* at a point $$a\in U$$ if $$f$$ is differentiable on some open disk centered at $$a$$. We say that $$f$$ is *holomorphic* on $$U$$ if $$f$$ is differentiable at every point in $$U$$. A function $$f:\mathbb{C}\to\mathbb{C}$$ which is holimorphic on $$\mathbb{C}$$ is also called an *entire* function.     
**Corollary** (Cauchy-Riemann)**.** Let $$U\subseteq\mathbb{C}$$ be an open set, identified as a subset of $$\mathbb{R}^2$$. If $$u,v:U\to\mathbb{R}$$ are functions having continuous partial derivative on $$U$$ and they satisfy the *Cauchy-Riemann* equations on $$U$$, then the function $$f:U\to\mathbb{C}$$ defined by $$f(x+iy)=u(x,y)+iv(x,y)$$ is holomorphic on $$U$$.        
**Theorem.** Let $$U$$ be a region in $$\mathbb{C}$$ (open and connected) and let $$f:U\to\mathbb{C}$$ be a function. If $$f$$ is holomorphic on $$U$$ and $$f'=0$$ on $$U$$, then $$f$$ is a constant function.         
**Lemma.** Let $$U\subseteq\mathbb{C}$$ be an open set, and let $$f,g:U\to\mathbb{C}$$ be holomorphic functions. Then      
&emsp;(i) $$f\pm g$$ and $$fg$$ are holomorphic on $$U$$, with $$(f\pm g)'=f'\pm g'$$ and $$(fg)'=f'g+fg'$$.     
&emsp;(ii) $$f/g$$ is holomorphic on the open set $$U\backslash g^{-1}(\{0\})=\{z\in U:g(z)\neq 0\}$$ with 

$$\left(\frac{f}{g}\right)'=\frac{f'g-fg'}{g^2}.$$

> For non-negative integer $$n$$, if $$f(z)=z^n$$ then $$f'(z)=nz^{n-1}$$. Thus all polynomials are entire. And all rational functions are holomorphic everywhere except at the roots of the denominators.

**Theorem** (Chain rule)**.** Let $$U,V\subseteq\mathbb{C}$$ be open sets. If $$f:V\to\mathbb{C}$$ and $$g:U\to V$$ are holomorphic functions, then $$f\circ g:U\to\mathbb{C}$$ is also a holomorphic function. Moreover,

$$(f\circ g)'(z)=f'(g(z))g'(z)$$

for every $$z\in U$$.      
**Definition.** The complex *cosine* and *sine* functions are defined by

$$\cos z=\frac{e^{iz}+e^{-iz}}{2},\quad \sin z=\frac{e^{iz}-e^{-iz}}{2i}.$$

> $$\cos$$ and $$\sin$$ are entire functions. The derivatives are the same as the real versions. Trigonometric formulas are also the same.

**Theorem** (L'Hôpital’s rule)**.** Let $$a\in \mathbb{C}$$ and let $$f,g$$ be complex functions that are both holomorphic at $$a$$ with $$f(a)=g(a)=0$$ but $$g'(a)\neq 0$$. Then

$$\lim_{z\to a}\frac{f(z)}{g(z)}=\frac{f'(a)}{g'(a)}.$$

#### §2.4 Power Series
**Definition.** Let $$U\subseteq \mathbb{C}$$, let $$(f_n)_{n\in\mathbb{N}}$$ be a sequence of functions $$f_n:U\to \mathbb{C}$$ and let $$f:U\to\mathbb{C}$$ be a function. We say that the sequence of functions $$(f_n)$$ *converges pointwise* on $$U$$ to the function $$f$$ if for each $$\varepsilon>0$$ and for each $$z\in U$$, there exists $$N\in\mathbb{N}$$ such that

$$|f_n(z)-f(z)|<\varepsilon,\quad \text{whenever }n\geq N.$$

In other words,

$$\lim_{n\to\infty}f_n(z)=f(z)\quad\text{for each }z\in U.$$

**Definition.** Let $$U\subseteq \mathbb{C}$$, let $$(f_n)_{n\in\mathbb{N}}$$ be a sequence of functions $$f_n:U\to \mathbb{C}$$ and let $$f:U\to\mathbb{C}$$ be a function. We say that the sequence functions $$(f_n)$$ *converges uniformly* on $$U$$ to the function if for each $$\varepsilon>0$$, there exists $$N\in \mathbb{N}$$ such that for all $$z\in U$$ and all $$n\geq N$$

$$|f_n(z)-f(z)|<\varepsilon.$$

In other words

$$\lim_{n\to\infty}\sup\{|f_n(z)-f(z)|:z\in U\}=0.$$

**Corollary** (Uniform convergence $$\Rightarrow$$ pointwise convergence)**.** Let $$U\substeq \mathbb{C}$$ and $$(f_n)$$ be a sequence of functions $$f_n:U\to\mathbb{C}$$. If $$(f_n)$$ converges uniformly on $$U$$, then $$(f_n)$$ converges pointwise on $$U$$.     
**Corollary** (Uniform limit $$\equiv$$ pointwise limit)**.** Let $$U\subseteq \mathbb{C}$$ and $$(f_n)$$ be a sequence of functions $$f_n:U\to\mathbb{C}$$. If $$(f_n)$$ converges uniformly on $$U$$ and converges pointwise on $$U$$ to a function $$f:U\to\mathbb{C}$$, then $$(f_n)$$ converges uniformly on $$U$$ to the same limit function $$f$$.     
**Theorem.** Let $$U\subseteq \mathbb{C}$$ and $$f_n:U\to\mathbb{C}$$ be continuous functions. If $$(f_n)$$ converges uniformly on $$U$$ to a function $$f:U\to \mathbb{C}$$, then $$f$$ is continuous. In other words, the uniform limit of a sequence of continuous functions is also continuous.    
> Then pointwise limit of a sequence of continuous functions may not be continuous.     

**Theorem** (Cauchy criterion)**.** Let $$U\subseteq \mathbb{C}$$ and $$f_n:U\to\mathbb{C}$$ be sequence of functions $$f_n:U\to \mathbb{C}$$. $$(f_n)$$ converges uniformly on $$U$$ iff for each $$\varepsilon>0$$, there exists $$N\in\mathbb{N}$$ such that for all $$z\in U$$ and all $$m,n\geq N$$,

$$|f_n(z)-f_m(z)|<\varepsilon.$$

**Definition** (Series)**.** Let $$U\subseteq \mathbb{C}$$ and let $$(f_n)$$ be a sequence of functions $$f_n:U\to\mathbb{C}$$. A *series* of functions, denoted by $$\displaystyle\sum_{k=0}^\infty f_k$$ is defined as the sequence of its partial sums. We say that a series *converges pointwise* (or *uniformly*) on $$U$$ if it converges pointwise (or uniformly) on $$U$$ as a sequence.       
**Definition.** Let $$U\subseteq \mathbb{C}$$ and let $$(f_n)$$ be a sequence of functions $$f_n:U\to\mathbb{C}$$. We say that the series of functions $$\displaystyle\sum_{k=0}^\infty f_k$$ is      
&emsp;(i) *pointwise absolutely-convergent* on $$U$$ if $$\displaystyle\sum_{k=0}^\infty |f_k|$$ converges pointwise on $$U$$, i.e. the series of complex numbers $$\displaystyle\sum_{k=0}^\infty |f_k(z)|$$ converges for each $$z\in U$$;      
&emsp;(ii) *uniformly absolutely-convergent* on $$U$$ if $$\displaystyle\sum_{k=0}^\infty |f_k|$$ converges uniformly on $$U$$.     
**Lemma.** A series of functions converges pointwise (or uniformly) on a set if it is pointwise (or uniformly) absolute-convergent on the set.    
**Theorem** (Weierstrass' M-test)**.** Let $$U\subseteq  \mathbb{C}$$, let $$(M_n)$$ be a sequence of non-negative real numbers and let $$(f_n)$$ be a sequence of functions $$f_n:U\to\mathbb{C}$$ such that $$f_n$$ is bounded above by $$M_n$$ for each $$n$$, i.e.

$$|f_n(z)|\leq M_n$$

for every $$z\in U$$. If the series of real numbers $$\displaystyle\sum_{k=0}^\infty M_k$$ converges, then the series of functions $$\displaystyle\sum_{k=0}^\infty$$ is uniformly absolutely-convergent on $$U$$.     
**Definition.** Let $$a\in\mathbb{C}$$ and let $$(a_n)$$ be a sequence of complex numbers. A *power series* is a series of functions of the form 

$$f(z)=\sum_{k=0}^\infty a_k(z-a)^k.$$

The number $$a$$ is called the *center* of the power series $$f$$, and the $$a_n$$'s are called the *coefficients* of $$f$$.     
**Definition.** Let $$a\in\mathbb{C}$$ and let $$(a_n)$$ be a sequence of complex numbers. The *radius of convergence* of the power series $$\displaystyle\sum_{k=0}^\infty a_k(z-a)^k$$ is the number $$R\in[0,+\infty]$$ defined by

$$R=\frac{1}{\limsup_n|a_n|^{\frac{1}{n}}}.$$

The *disk of convergence* of the power series $$\displaystyle\sum_{k=0}^\infty a_k(z-a)^k$$ is     
&emsp;(i) $$D(a;R)$$ if $$0<R<+\infty$$;      
&emsp;(ii) $$\mathbb{C}$$ if $$R=+\infty$$;     
&emsp;(iii) the singleton $$\{a\}$$ if $$R=0$$.    
**Corollary.** Let $$a\in\mathbb{C}$$ and let $$(a_n)$$ be a sequence of complex numbers. If $$\displaystyle\lim_{n\to+\infty}\left|\frac{a_n}{a_{n+1}}\right|$$ exists (either as a non-negative real number or $$+\infty$$), then the radius convergence of the power series $$\displaystyle\sum_{k=0}^\infty a_k(z-a)^k$$ is also given by

$$R=\lim_{n\to+\infty}\left|\frac{a_n}{a_{n+1}}\right|.$$

**Theorem** (Cauchy-Hadamard)**.** Let $$a\in\mathbb{C}$$ and let $$(a_n)$$ be a sequence of complex numbers. Let $$R$$ be the radius of convergence of the power series $$\displaystyle\sum_{k=0}^\infty a_k(z-a)^k$$. Then      
&emsp;(i) this power series is uniformly absolutely-convergent on every compact subset of $$D(a;R)$$;     
&emsp;(ii) this power series diverges at every point in $$\mathbb{C}\backslash\overline{D(a;R)}.$$         
**Theorem.** Let $$a\in\mathbb{C}$$ and let $$(a_n)$$ be a sequence of complex numbers. If the power series $$\displaystyle\sum_{k=0}^\infty a_k(z-a)^k$$ has a positive radius of convergence $$R>0$$, then the function $$f:D(a;R)\to\mathbb{R}\to\mathbb{C}$$ defined by

$$f(z)=\sum_{k=0}^\infty a_k(z-a)^k$$

is holomorphic, and its derivative is given by another power series

$$f'(z)=\sum_{k=1}^\infty ka_k(z-a)^{k-1}=\sum_{k=0}^\infty (k+1)a_{k+1}(z-a)^k.$$

**Corollary.** A power series is infinitely many times differentiable on its disk of convergence.    
**Corollary.** If a power series $$\displaystyle f(z)=\sum_{k=0}^\infty a_k(z-a)^k$$ has a positive radius of convergence $$R>0$$, then for each $$n\in\mathbb{N}$$, we have

$$f^{(n)}(a)=n!a_n.$$

**Theorem** (Uniqueness of power series)**.** Let $$a\in\mathbb{C}$$ and let $$\displaystyle f(z)=\sum_{k=0}^\infty a_k(z-a)^k$$ be a power series centered at $$a$$. If there exists a sequence of complex numbers $$\{z_n\}$$ converging to $$a$$ such that $$z_n\neq a$$ for all $$n\in\mathbb{N}$$ and

$$f(z_n)=0$$

for all $$n\in\mathbb{N}$$, then $$f$$ must be the zero power series, i.e. $$a_n=0$$ for all $$n$$.         
**Theorem** (Uniqueness of power series)**.** Let $$a\in\mathbb{C}$$ and let $$\displaystyle f(z)=\sum_{k=0}^\infty a_k(z-a)^k$$ and $$\displaystyle g(z)=\sum_{k=0}^\infty b_k(z-a)^k$$ be power series both centered at $$a$$. If there exists a sequence of complex numbers $$\{z_n\}$$ converging to $$a$$ such that $$z_n\neq a$$ for all $$n\in\mathbb{N}$$ and

$$f(z_n)=g(z_n)$$

for all $$n\in\mathbb{N}$$, then $$f$$ and $$g$$ must be the same power series, i.e. $$a_n=b_n$$ for all $$n$$.  


### <center>3  Line Integrals</center>
#### §3.1 Line Integrals
**Definition** (Integral)**.** Let $$[a,b]$$ be a bounded closed interval in $$\mathbb{R}$$ and let $$g:[a,b]\to\mathbb{C}$$ be a bounded function. The *integral* of $$g$$ over $$[a,b]$$ is defined by

$$\int_a^b g(t)dt = \int_a^b\text{Re }g(t)dt+i\int_a^b\text{Im }g(t)dt$$

if the Riemann integrals on the right-hand side both exist. In this case we also say that $$g$$ is *Riemann integrable* on $$[a,b]$$.      
**Lemma** (Triangle inequality)**.** Let $$[a,b]$$ be a bounded closed interval in $$\mathbb{R}$$ and $$g:[a,b]\to\mathbb{C}$$ be a function. If $$g$$ is Riemann integrable on $$[a,b]$$, then $$|g|$$ is also Riemann integrable on $$[a,b]$$ and we have $$\displaystyle \left|\int_a^b g(t)dt\right|\leq\int_a^b |g(t)|dt.$$        
**Definition** ($$C^1$$ curve)**.** Let $$[a,b]$$ be an interval in $$\mathbb{R}$$ and let $$U\subseteq\mathbb{C}$$.         
&emsp;(1) A continuous function $$\gamma:[a,b]\to U$$ is called a *curve* in $$U$$.      
&emsp;(2) A curve $$\gamma:[a,b]\in U$$ is called a $$C^1$$ curve in $$U$$ if its derivative $$\gamma'$$ is continuous on $$[a,b]$$ and $$\gamma'(t)\neq 0$$ for any $$t\in[a,b]$$.         
★**Definition** (Line integral along $$C^1$$ curve)**.** Let $$U\subseteq\mathbb{C}$$, $$\gamma:[a,b]\to U$$ be a $$C^1$$ curve and let $$f:U\to\mathbb{C}$$ be a continuous function. The *line integral* (*path integral* or *contour integral*) of $$f$$ along $$\gamma$$ is defined by

$$\int_\gamma f(z)dz=\int_a^b f(\gamma(t))\gamma'(t)dt.$$

**Lemma.** Let $$U\subseteq\mathbb{C}$$, $$f,g:U\to\mathbb{C}$$ be continuous functions, let $$c\in\mathbb{C}$$ and let $$\gamma:[a,b]\to U$$ be a $$C^1$$ curve. Then     
&emsp;(1) $$\displaystyle \int_\gamma(f+g)(z)dz=\int_\gamma f(z)dz+\int_\gamma g(z)dz.$$       
&emsp;(2) $$\displaystyle\int_\gamma (cf)(z)dz=c\int_\gamma f(z)dz.$$      
**Definition** (Reparametrization)**.** Let $$U\subseteq\mathbb{C}$$, let $$\gamma:[a,b]\to U$$ be a $$C^1$$ curve and let $$g:[g^{-1}(a),g^{-1}(b)]\to[a,b]$$ be a differentiable and strictly increasing function. Then $$\gamma\circ g:[g^{-1}(a),g^{-1}(b)]\to U$$ is called a *reparametrization* of the curve $$\gamma$$.    
**Lemma.** Let $$U\subseteq\mathbb{C}$$, $$f:U\to\mathbb{C}$$ be a continuous function and let $$\gamma:[a,b]\to U$$ be a $$C^1$$ curve. Then the line integral of $$f$$ along $$\gamma$$ does not depend on the parametrization of $$\gamma$$. In other words, if $$g:[g^{-1}(a),g^{-1}(b)]\to[a,b]$$ is differentiable and strictly increasing, then

$$\int_{\gamma\circ g}f(z)dz=\int_\gamma f(z)dz.$$

**Definition** (Reversal)**.** Let $$U\subseteq\mathbb{C}$$ and let $$\gamma:[a,b]\to U$$ be a curve in $$U$$. The *reversal* of $$\gamma$$ is the curve $$-\gamma:[-b,-a]\to U$$ defined by $$(-\gamma)(t)=\gamma(-t)$$ for every $$t\in[-b,-a]$$.        
**Lemma.** Let $$U\subseteq\mathbb{C}$$, $$f:U\to\mathbb{C}$$ be a continuous function and let $$\gamma:[a,b]\to U$$ be a $$C^1$$ curve in $$U$$. Then 

$$\int_{-\gamma}f(z)dz=-\int_\gamma f(z)dz.$$

**Definition** (Concentration)**.** Let $$U\subseteq\mathbb{C}$$, let $$\gamma_1:[a,b]\to U$$ and $$\gamma_2:[c,d]\to U$$ be curves such that the terminal point of $$\gamma_1$$ is the same terminal point of $$\gamma_1$$ is the same as the initial point of $$\gamma_2$$, i.e. $$\gamma_1(b)=\gamma_2(c)$$. The *concentration* of $$\gamma_1$$ and $$\gamma_2$$, denoted as $$\gamma_1*\gamma_2$$ is the curve in $$U$$ obtained by going along $$\gamma_1$$ followed by $$\gamma_2$$, i.e. $$\gamma=\gamma_1*\gamma_2:[a,b-c+d]\to U$$ is defined by $$\gamma(t)=\gamma_1(t)$$ if $$t\in[a,b]$$ and $$\gamma_2(t-b+c)$$ if $$t\in[b,b-c+d]$$. A curve $$\gamma$$ is called a *piecewise* $$C^1$$ curve if it is a concentration of finitely many $$C^1$$ curves $$\gamma_1,\gamma_2, \cdots,\gamma_N$$ joining end-to-end, i.e. $$\gamma=\gamma_1*\cdots*\gamma_N.$$    
**Definition** (Line integral along piecewise $$C^1$$ curve)**.** Let $$U\subseteq\mathbb{C}$$ and let $$\gamma_1,\gamma_2, \cdots,\gamma_N$$ joining end-to-end, let $$\gamma=\gamma_1*\cdots*\gamma_N$$, and let $$f:U\to\mathbb{C}$$ be a continuous function. The *line integral* of $$f$$ along $$\gamma$$ is defined by

$$\int_{\gamma}f(z)dz=\int_{\gamma_1}f(z)dz+\int_{\gamma_2}f(z)dz+\cdots+\int_{\gamma_N}f(z)dz.$$

**Definition** (Arc length)**.** Let $$U\subseteq\mathbb{C}$$ and let $$\gamma:[a,b]\to U$$ be a $$C^1$$ curve. The *arc-length* of $$\gamma$$ is the real number defined by $$L=\int_a^b |\gamma'(t)|dt.$$        
★**Corollary** (Cauchy ML-estimate)**.** Let $$U\subseteq \mathbb{C}$$, let $$f:U\to\mathbb{C}$$ be a continuous function and let $$\gamma;[a,b]\to U$$ be  $$C^1$$ curve in $$U$$ with arc-length $$L$$. If $$|f(z)|\leq M$$ for all $$z\in\text{image }\gamma$$, then $$\left|\int_\gamma f(z)dz\right|\leq ML.$$      
**Corollary.** Let $$U\subseteq\mathbb{C}$$, let $$\gamma:[a,b]\to U$$ be a $$C^1$$ curve in $$U$$, and let $$(f_n)$$ be a sequence of continuous functions $$f_n:U\to\mathbb{C}$$ which converges to a function $$f:U\to\mathbb{C}$$ uniformly on every compact subset of $$U$$. Then

$$\lim_{n\to +\infty}\int_\gamma f_n(z)dz=\int_\gamma f(z)dz.$$

#### §3.2 Cauchy-Goursat Theorem
**Definition.** Let $$U\subseteq\mathbb{C}$$ be a region and let $$f:U\to\mathbb{C}$$ be a function. An antiderivative of $$f$$ is a holomorphic function.       
**Theorem** (Fundamental theorem of Calculus)**.** Let $$U\subseteq\mathbb{C}$$ be a region and $$\gamma:[a,b]\to U$$ be a $$C^1$$ curve. If $$f:U\to \mathbb{C}$$ is a continuous function which has an antiderivative $$F:U\to\mathbb{C}$$, then

$$\int_\gamma f(z)dz=F(\gamma(b))-F(\gamma(a)).$$

**Definition** (Closed curve)**.** A curve $$\gamma:[a,b]\to \mathbb{C}$$ is called a *closed curve* if its initial point and terminal point are the same point, i.e. $$\gamma(a)=\gamma(b)$$.
> The line integral of a continuous function $$f$$ along a closed curve is denoted as $$\oint_\gamma f(z)dz.$$

**Corollary.** Let $$U\subseteq \mathbb{C}$$ be a region, $$f:U\to\mathbb{C}$$ be a continuous function having an antiderivative on $$U$$ and $$\gamma:[a,b]\to U$$ be a closed $$C^1$$ curve. Then

$$\oint_\gamma f(z)dz=0.$$

**Definition.** A closed curve $$\gamma:[a,b]\to\mathbb{C}$$ is called a *simple closed curve* if it does not have any self-intersection, i.e. if $$\gamma(t_1)\neq\gamma(t_2)$$ for any distinct $$t_1,t_2\in[a,b]$$, except when $$t_1=a, t_2=b$$.        
**Theorem** (Jordan curve theorem)**.** The image of a simple closed curve in $$\mathbb{C}$$ divides the whole plane $$\mathbb{C}$$ into two regions. One of these regions is bounded, and the other one is unbounded.         
**Definition** (Interior and exterior)**.** Let $$\gamma$$ be a simple closed curve in $$\mathbb{C}$$. The bounded region as described in the above Jordan curve theorem is called the *interior* of $$\gamma$$. The other unbounded region is called the *exterior* of $$\gamma$$.       
**Definition** (Simply connected region)**.** Let $$U\subseteq \mathbb{C}$$ be a region. We say that $$U$$ is a *simply connected region* if for every simple closed curve $$\gamma$$ in $$U$$, the interior of $$\gamma$$ also lies completely in $$U$$.        
> A simply connected region in $$\mathbb{C}$$ can be regarded as no "holes".     

★**Theorem** (Cauchy-Goursat)**.** Let $$U\subseteq \mathbb{C}$$ be a simply connected region, $$f:U\to\mathbb{C}$$ be a holomorphic function and $$\gamma$$ be a closed $$C^1$$ curve in $$U$$. Then

$$\oint_\gamma f(z)dz=0.$$

> **Proof of the theorem:**         
> **Lemma.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, $$f:U\to\mathbb{C}$$ be a holomorphic function and $$\gamma$$ be a triangle in $$U$$. Then $$\int_\gamma f(z)dz=0.$$     
> **Lemma.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, $$f:U\to\mathbb{C}$$ be a continuous function. If $$\oint_\gamma f(z)dz=0$$ for every triangle $$\gamma$$ in $$U$$, then $$\oint_\gamma f(z)dz=0$$ for every polygonal closed curve $$\gamma$$ in $$U$$.       
> **Lemma.** Let $$U\subseteq \mathbb{C}$$ be a region and $$f:U\to \mathbb{C}$$ be a continuous function. If $$\oint_\gamma f(z)dz=0$$ for every polygonal closed curve $$\gamma$$ in $$U$$, then $$f$$ has an antiderivative on $$U$$.    
> **Theorem.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region and $$f:U\to\mathbb{C}$$ be a holomorphic function. Then $$f$$ has an antiderivative of $$U$$.    

★**Theorem** (Cauchy-Goursat)**.** Let $$U\subseteq\mathbb{C}$$ be a region and $$f:U\to\mathbb{C}$$ be a holomorphic function. If $$\gamma,\gamma_1,\cdots,\gamma_n$$ are simple cosed curves in $$U$$ oriented counterclockwise such that      
&emsp;(1) $$\text{image }\gamma_1,\cdots,\text{image }\gamma_n$$ are in interior of $$\gamma$$,      
&emsp;(2) the interiors of $$\gamma_1,\cdots,\gamma_n$$ are mutually disjoint,    
&emsp;(3) $$U$$ contains the intersection of the interior of $$\gamma$$ and all the exteriors of $$\gamma_1,\cdots,\gamma_n$$,     
then

$$\oint_\gamma f(z)dz=\sum_{k=1}^\infty \oint_{\gamma_k} f(z)dz.$$

<center><img src="http://sxubi.github.io/photos/cauchy_goursat.png" width = "200"/></center>

In particular, if $$\gamma_1,\gamma_2$$ are simple closed curves in $$U$$ oriented counterclockwise such that    
&emsp;(1) $$\text{image }\gamma_2$$ is in the interior of $$\gamma_1$$ and     
&emsp;(2) $$U$$ contains the intersection of the interior of $$\gamma_1$$ and the exterior of $$\gamma_2$$, then     

$$\oint_{\gamma_1}f(z)dz=\oint_{\gamma_2}f(z)dz.$$


#### §3.3 Cauchy Integral Formula
★**Theorem** (Cauchy integral formula)**.** Let $$U\subset\mathbb{C}$$ be a simply connected region, $$f:U\to\mathbb{C}$$ be a holomorphic function, $$\gamma$$ be a counterclockwise oriented simple closed $$C^1$$ curve in $$U$$, and $$a$$ be a point in the interior of $$\gamma$$. Then

$$\frac{1}{2\pi i}\oint\frac{f(z)}{z-a}dz=f(a).$$

#### §3.4 Complex Logarithm
**Theorem.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region and $$f:U\to\mathbb{C}$$ be a holomorphic function. Then $$f$$ has an antiderivative on $$U$$.
**Corollary.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, identified as an open subset of $$\mathbb{R}^2$$. If $$u:U\to\mathbb{R}$$ is a harmonic function, then there exists a holomorphic function $$f:U\to\mathbb{C}$$ such that $$\text{Re }f=u$$.     
**Theorem.** Let $$U\subset\mathbb{C}$$ be a simply connected region such that $$0\not\in U$$. Then there exists holomorphic function $$f:U\to\mathbb{C}$$ such that $$e^{f(z)}=z$$ for every $$z\in U$$.      
**Definition** (Branch of logarithm)**.** Let $$U\subset\mathbb{C}$$ be a simply connected region such that $$0\not\in U$$. A *branch of (complex) logarithm* is a choice of a holomorphic function $$f:U\to\mathbb{C}$$ such that $$e^{f(z)}=z$$ for $$z\in U$$.       
**Corollary.** Let $$U\subset\mathbb{C}$$ be a simply connected region such that $$0\not\in U$$. For every branch of logarithm $$\log:U\to\mathbb{C}$$, we always have $$\frac{d}{dz}\log z=\frac{1}{z}.$$         
> ★ **Remark.** The *principal branch of logarithm*: $$z=re^{i\theta}, r>0, \theta\in(-\pi,\pi)$$
>
> $$Log z = \ln|r|+i\theta.$$
>


> ★**Remark.** Let $$U\subset\mathbb{C}$$ be a simply connected region such that $$0\not\in U$$. A branch of logarithm on $$U$$ can be defined as: fixing any $$a\in U$$ and choosing $$k\in\mathbb{C}$$ such that $$e^k=a$$ ($$\log a = k$$), a branch of logarithm $$\log:U\to\mathbb{C}$$ can be defined by
>
> $$\log z=k+\int \frac{1}{w}dw.$$
>
> The line integral is evaluated by a curve in $$U$$ joining $$a$$ to $$z$$ and it is path-independent. Every two different choices of $$k$$ differing by an integer multiple of $$2\pi i$$ result in 2 different branches of logarithm on $$U$$.     

**Definition** (Exponential function with base $$z$$)**.** Let $$U\in \mathbb{C}$$ be a simply connected region such that $$0\not\in U$$. For a fixed choice of branch of logarithm $$\log:U\to\mathbb{C}$$ and for each $$z\in U$$, the *exponential function with base* $$z$$ is defined by

$$z^w=e^{w\log z}.$$

> **Remark.** For a fixed branch of complex logarithm, generally $$\log(zw)\neq\log z+\log w, \log(z/w)\neq\log z-\log w, \log z^w\neq w\log z, \log e^z\neq z$$. However, $$e^{\log z}=z$$ still holds.     

**Theorem.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region and let $$g:U\to\mathbb{C}$$ be a holomorphic function such that $$g(z)\neq 0$$ for any $$z\in U$$. Then there exists a holomorphic function $$f:U\to\mathbb{C}$$ such that $$e^{f(z)}=g(z)$$ for every $$z\in U$$.     
**Theorem.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region and let $$g:U\to\mathbb{C}$$ be a holomorphic function such that $$g(z)\neq 0$$ for any $$z\in U$$. Then for each $$n\in \mathbb{N}$$, there exists a holomorphic function $$f:U\to\mathbb{C}$$ such that $$(f(z))^n=g(z)$$ for every $$z\in U$$.     


### <center>4  Consequences of the Cauchy Integral Formula</center>
#### §4.1 Taylor Series of a Function
**Theorem** (Taylor)**.** Let $$a\in\mathbb{C}$$ and $$r>0$$, and let $$f:D(a:r)\to\mathbb{C}$$ be a holomorphic function. Then there exists a sequence of complex numbers $$(a_n)$$ such that 

$$f(z)=\sum_{k=0}^\infty a_k(z-a)^k$$

for every $$z\in D(a;r)$$.       
**Corollary.** Let $$U\subseteq\mathbb{C}$$ be an open set and $$f:U\to\mathbb{C}$$ be a holomorphic function. Then its derivative $$f':U\to\mathbb{C}$$ is also holomorphic. Consequently, a holomorphic function on $$U$$ is infinitely many times differentiable at each point in $$U$$.      
★**Corollary** (Generalized Cauchy integral formula)**.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, $$f:U\to\mathbb{C}$$ be a holomorphic function, $$\gamma$$ be a counterclockwise oriented simple closed $$C^1$$ curve in $$U$$, $$a$$ be a point in the interior of $$\gamma$$, and $$n$$ be a non-negative integer. Then

$$f^{(n)}(a)=\frac{n!}{2\pi i}\oint_\gamma\frac{f(z)}{(z-a)^{n+1}}dz.$$

★**Definition** (Taylor series)**.** Let $$a\in \mathbb{C}$$ and $$r>0$$, and let $$f:D(a;r)\to\mathbb{C}$$ be a holomorphic function. The power series

$$\sum_{k=0}^\infty\frac{f^{(k)}(a)}{k!}(z-a)^k,$$

is called the *Taylor series of* $$f$$ at $$a$$. The Taylor series of $$f$$ at $$0$$ is also called the *Maclaurin series* of $$f$$.
> **Remark.** ★(1) Let $$f$$ be holomorphic at $$a$$. Let $$b$$ the point(s) nearest to $$a$$ such that $$\lim_{z\to b}f(z)\not\in\mathbb{C}$$. The radius of convergence of the Taylor series of $$f$$ at $$a$$ is $$|b-a|$$.       
> ★(2) Note that $$\displaystyle\frac{1}{1-w}=\sum_{k=0}^\infty w^k$$ for $$|w|<1.$$       
> (3) A function of one complex variable is analytice iff it is holomorphic.        
> ★(4) The following Maclaurin series are useful in finding the Taylor series:
> 
> $$e^z=\sum_{k=0}^{\infty}\frac{1}{k!}z^k,\quad\sin z=\sum_{k=0}^\infty\frac{(-1)^k}{(2k+1)!}z^{2k+1},\quad\cos z=\sum_{k=0}^\infty\frac{(-1)^k}{(2k)!}z^{2k}.$$
>

A number $$a$$ satisfying $$f(a)=0$$ is usually called a *zero* of $$f$$.      
★**Definition.** Let $$a\in\mathbb{C}$$ and let $$f$$ be a function which is holomorphic at $$a$$. We say that $$f$$ has a *zero of order* $$m$$ at $$a$$ if

$$f(a)=f'(a)=\cdots=f^{(m-1)}(a)=0$$

but $$f^{(m)}\neq 0$$.    
★**Lemma** (Factor theorem)**.** Let $$a\in\mathbb{C}$$ and let $$f$$ be a function which is holomorphic at $$a$$. Then $$f$$ has a zero of order $$m$$ at $$a$$ iff there exists $$r>0$$ and a holomoprhic function $$g:D(a;r)\to\mathbb{C}$$ such that $$g(a)\neq 0$$ and

$$f(z)=(z-a)^mg(z)$$

for every $$z\in D(a;r)$$.

#### §4.2 Morera's Theorem
★**Theorem** (Morera)**.** Let $$U\subseteq\mathbb{C}$$ be a region and $$f:U\to\mathbb{C}$$ be a continuous function. If 

$$\oint_\gamma f(z)dz=0$$

for every triangle $$\gamma$$ in $$U$$, then $$f$$ is holomorphic on $$U$$.       
**Theorem.** Let $$U\subseteq\mathbb{C}$$ be a region and let $$(f_n)$$ be a sequence of holomorphic functions $$f_n:U\to\mathbb{C}$$. If $$(f_n)$$ converges to a function $$f:U\to\mathbb{C}$$ uniformly on every compact subset of $$U$$, then $$f$$ is holomorphic. In other words, the uniform limit of a sequence of holomorphic functions is also holomorphic.       
**Theorem.** Let $$U\subseteq\mathbb{C}$$ be a region, $$a\in U$$ and $$f:U\to\mathbb{C}$$ be a continuous function which is holomorphic on $$U\backslash\{a\}$$. Then $$f$$ is holomorphic on $$U$$.      
> **Example.** $$U\subseteq\mathbb{C}$$ is a region, $$a\in U$$ and $$f:U\to\mathbb{C}$$ be a holomorphic function. Then the continuous function $$g:U\to\mathbb{C}$$ defined by $$g(z)=\frac{f(z)-f(a)}{z-a}$$ if $$z\in U\backslash\{a\}$$ and $$g(z)=f'(a)$$ if $$z=a$$ is also holomorphic on $$U$$.

**Theorem.** Let $$U\subseteq \mathbb{C}$$ be a region, $$\gamma:\mathbb{R}\to U$$ be a piecewise $$C^1$$ curve, and $$f:U\to\mathbb{C}$$ be a continuous function which is holomorphic on $$U\backslash\text{image }\gamma$$. Then $$f$$ is holomorphic on $$U$$.       
The following two reflection principles extends the domains of holomorphic functions by reflection.        
**Theorem** (Schwarz reflection)**.** Let $$H=\{z\in\mathbb{C}:\text{Im }z>0\}$$ be the open upper half-plane. Let $$U\subseteq H$$ be a region, and denote the reflection of $$U$$ across the real axis by $$U^*=\{z\in\mathbb{C}:\bar z\in U\}.$$ Let $$f:\bar U\to\mathbb{C}$$ be a continuosu function which is holomorphic on $$U$$. If $$f$$ sends real numbers to real numbers (i.e. $$f(z)\in\mathbb{R}$$ for every $$z\in \bar U\cap \mathbb{R}$$), then $$f$$ can be extended to a holomorphic functions on $$U\cup U^*$$, i.e. there exists a continuous function $$F:\overline{U\cup U^*}\to\mathbb{C}$$ which is holomorphic on the interior of its domain and $$F(z)=f(z)$$ for every $$z\in\bar U$$. In particular, if $$f:\bar H\to\mathbb{C}$$ is continuous on $$\bar H$$, holomorphic on $H$, and $$f(z)\in\mathbb{R}$$ for every $$z\in \mathbb{R}$$, then $$f$$ can be extended to an entire function $$F:\mathbb{C}\to\mathbb{C}$$.          
**Theorem** (Schwarz reflection)**.** Let $$U\subset D(0;1)$$ be a region, and denote the reflection across $$\partial D(0;1)$$ by $$U^*=\{z\in\mathbb{C}:1/\bar z\in U\}$$. Let $$f:\bar U\to\mathbb{C}$$ be a continuous function which is holomorphic on $$U$$. If $$f$$ sends $$\partial D(0;1)$$ to real numbers, then $$f$$ can be extended to a holomorphic function on $$U\cup U^*$$, i.e. there exists a continuous function $$F:\overline{U\cup U^*}\to\mathbb{C}$$ which is holomorphic on the interior of its domain and $$F(z)=f(z)$$ for every $$z\in\bar U$$. In particular, if $$f:\overline{D(0;1)}\to\mathbb{C}$$ is continuous on $$\overline{D(0;1)}$$, holomorphic on $$D(0;1)$$, and $$f(z)\in \mathbb{R}$$ for every $$z\in\partial D(0;1)$$, then $$f$$ can be extended to an entire function $$F:\mathbb{C}\to\mathbb{C}$$.        

#### §4.3 Isolated Zeros Theorem, Identity Theorem
★**Theorem** (Isolated zeros)**.** Let $$U\subset\mathbb{C}$$ be a region and $$f:U\to\mathbb{C}$$ be a holomorphic function. If there exists $$a\in U$$ and a sequence $$(z_n)$$ of points in $$U$$ converging to $$a$$ such that $$z_n\neq a$$ for all $$n\in\mathbb{N}$$ and $$f(z_n)=0$$ for all $$n\in N$$, then $$f$$ must be the constant function zero, i.e. $$f(z)=0$$ for all $$z\in U$$.        
**Definition.** A set $$S\subset \mathbb{C}$$ is *isolated* if for each $$a\in S$$, there exists $$r>0$$ such that $$(D(a;r)\backslash\{a\})\cap S=\emptyset,$$ i.e. $$D(a;r)$$ doesn't contain any other element of $$S$$ apart from $$a$$.          
**Corollary** (Isolated zeros)**.** Let $$U\subseteq\mathbb{C}$$ be a region and $$f:U\to\mathbb{C}$$ be a holomorphic function such that $$f\not\equiv0$$. Then the zeros of $$f$$ are *isolated*, i.e. $$f^{-1}(\{0\})$$ is an isolated set.    
**Corollary.** Let $$U\subseteq\mathbb{C}$$ be a region and $$f:U\to\mathbb{C}$$ be a holomorphic function such that $$f\not\equiv 0$$. Then for each compact set $$K\subset U$$, $$f$$ has only finitely many zeros in $$K$$.       
★**Corollary** (Identity theorem)**.** Let $$U\subseteq\mathbb{C}$$ be a region and $$f,g:U\to\mathbb{C}$$ be holomorphic functions. If there exists $$a\in U$$ and a sequence $$(z_n)$$ of points in $$U$$ converging to $$a$$ such that $$z_n\neq a$$ for all $$n\in \mathbb{N}$$ and $$f(z_n)=g(z_n)$$ for all $$n\in \mathbb{N}$$, then $$f$$ and $$g$$ must be the same function, i.e. $$f(z)=g(z)$$ for all $$z\in U$$.      

#### §4.4 Maximum Modulus Principle
**Theorem** (Mean value property)**.** Let $$U\subseteq\mathbb{C}$$ be an open set, let $$f:U\subseteq\mathbb{C}$$ be a holomorphic function, and let $$a\in U$$ and $$r>0$$ such that $$\overline{D(a;r)}\subset U$$. Then $$\displaystyle\frac{1}{2\pi}\int_0^{2\pi}f(a+re^{it})dt=f(a).$$          
**Theorem** (Maximum modulus principle)**.** Let $$U\subseteq\mathbb{C}$$ be a region and let $$f:U\subseteq\mathbb{C}$$ be a non-constant holomorphic function. Then $$|f|$$ doesn't attain relative maximum in $$U$$.       
**Corollary** (Minimum modulus principle)**.** Let $$U\subseteq\mathbb{C}$$ and let $$f:U\subseteq\mathbb{C}$$ be a non-constant holomorphic function such  that $$f(z)\neq 0$$ for any $$z\in U$$. Then $$|f|$$ doesn't attain relative minimum in $$U$$.          
★**Corollary** (Maximum modulus principle)**.** Let $$U\subseteq\mathbb{C}$$ be a bounded region and let $$f:\bar U\to\mathbb{C}$$ be a continuosu function which is holomorphic on $$U$$. Then the absolute maximum of $$|f|$$ in $$\bar U$$ is attained on $$\partial U$$, i.e. $$\max\{|f(z)|:z\in\bar U\}=\max\{|f(z)|:z\in\partial U\}$$.        
**Theorem** (Open mapping)**.** The direct image of an open set via a non-constant holomorphic function is open.            
**Theorem** (Biholomorphic regions)**.** Let $$U,V\subseteq\mathbb{C}$$ be regions. If $$f:U\to V$$ is a holomorphic function which has an inverse $$g:V\to U$$, then $$g$$ is also holomorphic.        
**Theorem** (Schwarz lemma)**.** Let $$f:D(0;1)\to D(0;1)$$ be a holomorphic function such that $$f(0)=0$$. Then        
&emsp;(1) $$|f(z)|\leq |z|$$ for every $$z\in D(0;1)$$, and $$|f'(0)|\leq 1$$;    
&emsp;(2) If either one of the equalities holds, i.e. $$|f(w)|=|w|$$ for some non-zero $$w$$ or $$|f'(0)|=1$$, then there exists $$\theta\in\mathbb{R}$$ such that $$f(z)=e^{i\theta}z$$ for every $$z\in D(0;1)$$.           
**Lemma.** For each $$a\in D(0;1)$$, let $$\varphi_a:D(0;1)\to D(0;1)$$ be the function 

$$\varphi_a(z)=\frac{a-z}{1-\bar a z}.$$

Then        
&emsp;(1) $$\varphi_a$$ is holomorphic and invertible (an automorphism of $$D(0;1)$$) with $$\varphi_a^{-1}=\varphi_a.$$          
&emsp;(2) $$\varphi_a$$ swaps $$0$$ and $$a$$, i.e. $$\phi_a(0)=a$$ and $$\phi_a(a)=0$$.        
&emsp;(3) $$\displaystyle\varphi_a'(z)=\frac{|a|^2-1}{(1-\bar a z)^2}$$ for every $$z\in D(0;1)$$.         
> ★**Example.** Let $$f:D(0;1)\to D(0;1)$$ be a holomorphic function. Then $$\displaystyle|f'(z)|\leq\frac{1-|f(z)|^2}{1-|z|^2}$$ for every $$z\in D(0;1)$$, and that this bound for $$|f'|$$ is sharp, i.e. for each $$z\in D(0;1)$$, there exists a holomorphic function $$f$$ such that the equality is attained at $$z$$.          
&emsp;


#### §4.5 Liouville's Theorem
**Lemma** (Cauchy estimate)**.** Let $$U\subseteq\mathbb{C}$$ be an open set, let $$f:U\to\mathbb{C}$$ be a holomorphic function, and let $$a\in U$$ and $$r>0$$ such that $$\overline{D(a;r)}\subset U$$. Then for each $$n\in\mathbb{N}\cup\{0\}$$,

$$|f^{n}(a)|\leq\frac{n!M_r}{r^n},\quad M_r=\max\{|f(z)|:z\in\partial D(a;r)\}.$$

★**Theorem** (Liouville)**.** Let $$f:\mathbb{C}\to\mathbb{C}$$ be a bounded entire function. Then $$f$$ is a constant function.         
**Theorem** (Fundamental Theorem of Algebra)**.** A non-constant polynomial with complex coeffcients must have a zero in $$\mathbb{C}$$. In other words, the field of complex numbers $$\mathbb{C}$$ is algebraically closed.         

### <center>5  Isolated Singularities</center>
#### §5.1 Classification of Singularities
**Definition.** $$a\in\mathbb{C}$$. A function $$f$$ has an *isolated singularity* at $$a$$ if $$f$$ is not holomorphic at $$a$$ but is holomorphic on some "punctured disk" centered at $$a$$, i.e. if there exists $$r>0$$ such that $$f$$ is holomorphic on $$D(a;r)\backslash\{a\}.$$          
★**Definition.** Let $$a\in\mathbb{C}$$ and let $$f$$ be a function which has an isolated singularity at $$a$$.      
(1) $$f$$ has a *removable singularity* at $$a$$ if $$\displaystyle\lim_{z\to a}f(z)$$ exists as a finite complex number.       
(2) $$f$$ has a *pole* at $$a$$ if $$\displaystyle\lim_{z\to a}f(z)=\infty$$, i.e., $$\displaystyle\lim_{z\to a}\frac{1}{f(z)}=0.$$         
(3) $$f$$ has an *essential singularity* at $$a$$ if $$f$$ has neither a removable singularity nor a pole at $$a$$, i.e. $$\displaystyle\lim_{z\to a}f(z)$$ doesn't exist.            
**Corollary.** Let $$a\in\mathbb{C}$$ and let $$f$$ be a function which has an isolated singularity at $$a$$. Then $$f$$ has a removable singularity at $$a$$ iff there exist $$r>0$$ and a holomorphic function $$F:D(a;r)\to\mathbb{C}$$ such that $$F(z)=f(z)$$ for every $$z\in D(a;r)\backslash\{a\}$$.         
**Theorem** (Riemann extension)**.** Let $$a\in\mathbb{C}$$ and let $$f$$ be a function which has an isolated singularity at $$a$$. Then $$f$$ has a *removable singularity* at $$a$$ iff there exists $$r>0$$ such that $$f$$ is bounded on $$D(a;r)\backslash\{a\}$$.        
**Theorem** (Casorati-Weierstrass)**.** Let $$a\in\mathbb{C}$$ and let $$f$$ be a function which has an isolated singularity at $$a$$. Then $$f$$ has an *essential singularity* at $$a$$ iff for every $$r>0$$. $$\overline{f(D(a;r)\backslash\{a\})}=\mathbb{C}$$, i.e. for each $$w\in\mathbb{C}$$ and each $$\varepsilon>0$$, there exists $$z\in D(a;r)\backslash\{a\}$$ such that $$|f(z)-w|<\epsilon.$$ (This means that for each $$w\in\mathbb{C}$$, there exists $$z$$ arbitary near $$a$$ such that $$f(z)$$ is near $$w$$.) 

#### §5.2 Laurent Series
★**Definition.** Let $$a\in\mathbb{C}$$ and let $$(a_n)_{n\in\mathbb{Z}}$$ be a two-sided sequence of complex numbers. A *Laurent series* is a two-sided series of functions of the form

$$f(z)=\sum_{k=-\infty}^\infty a_k(z-a)^k.$$

The number $$a$$ is called the *center* of the Laurent series $$f$$, and the $$a_n$$'s are called the *coefficients* of $$f$$.         
**Definition.** Let $$a\in\mathbb{C}$$ and let $$0\leq r\leq R\leq +\infty$$. The open annulus centered at $$a$$ with inner radius $$r$$ and outer radius $$R$$ is the set 

$$A(a;r;R)=\{z\in\mathbb{C}:r<|z-a|<R\}.$$

**Definition.** Let $$a\in\mathbb{C}$$ and let $$(a_n)_{n\in\mathbb{Z}}$$ be a two-sided sequence of complex numbers. Let $$R_0,R_1\in[0,+\infty]$$ be the extended real numbers defined by

$$R_0=\limsup_{n\in\mathbb{N}}|a_{-n}|^\frac{1}{n},\quad R_1=\frac{1}{\limsup_{n\in\mathbb{N}}|a_n|^\frac{1}{n}}.$$

Then the *annulus of convergence* of teh Laurent series $$\sum_{k=-\infty}^\infty a_k(z-a)^k$$ is $$A(a;R_0;R_1).$$        
**Lemma.** Let $$a\in\mathbb{C}$$ and let $$(a_n)_{n\in\mathbb{Z}}$$ be a two-sided sequence of complex numbers. Let $$A(a;R_0;R_1)$$ be the annulus of convergence of the Laurent series $$\sum_{k=-\infty}^\infty a_k(z-a)^k$$ is $$A(a;R_0;R_1).$$, where $$0\leq R_0\leq R_1\leq +\infty$$. Then        
(i) This Laurent series is uniformly absolutely-convergent on every compact subset of $$A(a;R_0;R_1)$$, and its uniform limit is a holomorphic function $$f:A(a;R_0;R_1)\to\mathbb{C}.$$       
(ii) This Laurent series diverges at every point in the interior of $$\mathbb{C}\backslash A(a;R_0;R_1).$$         
★**Theorem** (Laurent)**.** Let $$a\in\mathbb{C}$$ and $$0\leq r<R\leq +\infty$$, and let $$f:A(a;r;R)\to\mathbb{C}$$ be a holomorphic function. Then there exists a two-sided sequence of complex numbers $$(a_n)_{n\in\mathbb{Z}}$$ such that

$$f(z)=\sum_{k=-\infty}^\infty a_k(z-a)^k$$

for every $$z\in A(a;r;R)$$.        
**Definition.** Let $$a\in\mathbb{C}$$ and $$0\leq r<R\leq +\infty$$, and let $$f:A(a;r;R)\to\mathbb{C}$$ be a holomorphic function. The Laurent series $$\sum_{k=-\infty}^{+\infty} a_k(z-a)^k$$ centered at $$a$$ with coefficients 

$$a_n=\frac{1}{2\pi i}\oint_{\partial D(a;\rho)}\frac{f(w)}{(w-a)^{n+1}}dw$$

where $$\rho\in(r,R)$$ is called the *Laurent series* of $$f$$ in the annulus $$A(a;r;R).$$
> ★**Remark.** 
>
> $$\displaystyle\frac{1}{1-w}=\sum_{k=0}^{+\infty} w^k,\quad |w|<1.$$
>

**Definition.** Let $$a\in\mathbb{C}$$ and $$f$$ be a function which has an isolated singularity at $$a$$, i.e. there exists $$r>0$$ such that $$f:D(a;r)\backslash\{a\}\to\mathbb{C}$$ is a holomorphic function. Then the Laurent series

$$\sum_{k=-\infty}^{+\infty}a_k(z-a)^k$$

of $$f$$ in the punctured disk $$A(a;0;r)=D(a;r)\backslash\{a\}$$ is particularly important, and is called the *Laurent series* of $$f$$ at $$a$$. The part $$\sum_{k=0}^{+\infty}a_k(z-a)^k$$ is called the *analytic part* of this Laurent series, while the remaining part $$\sum_{k=-\infty}^{-1}a_k(z-a)^k$$ is called the *principal part* of the Laurent series.         
★**Theorem.** Let $$a\in\mathbb{C}$$ and $$f$$ be a function which has an isolated singularity at $$a$$. Then      
(1) $$f$$ has a removable singularity at $$a$$ iff the principal part of the Laurent series of $$f$$ at $$a$$ is zero.         
(2) $$f$$ has a pole at $$a$$ iff the principal part of the Laurent series of $$f$$ at $$a$$ is a non-zero finite sum.         
(3) $$f$$ has an essential singularity at $$a$$ iff the principal part of the Laurent series of $$f$$ at $$a$$ is an infinite sum.          
**Definition.** Let $$a\in\mathbb{C}$$ and let $$f$$ be a function which has a pole at $$a$$, so that the principal part of the Laurent series $$\sum_{k=-\infty}^{+\infty}a_k(z-a)^k$$ of $$f$$ at $$a$$ is a non-zero finite sum. We say that $$f$$ has a *pole of order* $$n$$ at $$a$$ if $$a_{-n}\neq 0$$ but $$a_k=0$$ for all $$k<-n$$, i.e. if $$n$$ is the greatest natural number such that $$a_{-n}\neq 0$$. We also say that $$f$$ has a simple (double) pole at $$a$$ if $$f$$ has a pole of order 1 (2) at $$a$$.           
★**Corollary** (Factor theorem)**.** Let $$a\in\mathbb{C}$$ and let $$f$$ be a function which has an isolated singularity at $$a$$. Then $$f$$ has a pole of order $$n$$ at $$a$$ iff there exists $$r>0$$ and a holomorphic function $$g:D(a;r)\to\mathbb{C}$$ such that $$g(a)\neq 0$$ and 

$$f(z)=\frac{g(z)}{(z-a)^n}$$

for every $$z\in D(a;r)\backslash\{a\}$$.

#### §5.3 Residue
★**Definition.** Let $$a\in\mathbb{C}$$ and let $$f$$ be a function which has an isolated singularity at $$a$$. The *residue* of $$f$$ at $$a$$ is the coefficient of $$(z-a)^{-1}$$ in the Laurent series of $$f$$ at $$a$$, i.e.

$$\text{Res}(f;a)=a_{-1}$$

if $$f(z)=\sum_{k=-\infty}^{+\infty}a_k(z-a)^k$$ for every $$z\in D(a;r)\backslash\{a\}.$$         
★**Lemma.** Let $$a\in\mathbb{C}$$ and let $$f$$ be a function which has an isolated singularity at $$a$$.        
(1) If $$f$$ has a removable singularity at $$a$$, then

$$\text{Res}(f;a)=0.$$

(2) If $$f$$ has a simple pole at $$a$$, then

$$\text{Res}(f;a)=\lim_{z\to a}(z-a)f(z).$$

(3) In general, if $$f$$ has a pole of order at most $$n$$ at $$a$$, then

$$\text{Res}(f;a)=\frac{1}{(n-1)!}\lim_{z\to a}\frac{d^{n-1}}{dz^{n-1}}[(z-a)^nf(z)].$$

**Theorem.** Let $$\gamma:[0;1]\to\mathbb{C}$$ be a closed $$C^1$$ curve and let $$a\in\mathbb{C}\backslash\text{image }\gamma$$, i.e. $$\gamma$$ doesn't pass through $$a$$. Then

$$\frac{1}{2\pi i}\oint_\gamma\frac{1}{z-a}dz$$

is an integer.           
**Definition.** Let $$\gamma:[0;1]\to\mathbb{C}$$ be a closed $$C^1$$ curve and let $$a\in\mathbb{C}\backslash\text{image }\gamma$$, i.e. $$\gamma$$ doesn't pass through $$a$$. The *winding number* of $$\gamma$$ around $$a$$ is the integer defined by

$$n(\gamma;a)=\frac{1}{2\pi i}\oint_\gamma\frac{1}{z-a}dz.$$

**Corollary.** Let $$\gamma;[0,1]\to\mathbb{C}$$ be a counterclockwise oriented simple closed $$C^1$$ curve, and let $$a\in\mathbb{C}\backslash(\text{image }\gamma)$$. Then $$n(\gamma;a)=0$$ if $$a$$ is in the exterior of $$\gamma$$, and $$n(\gamma;a)$$ is in the interior of $$\gamma$$.           
★**Theorem** (Cauchy's residue theorem)**.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, let $$\gamma$$ be a closed piecewise $$C^1$$ curve in $$U$$, and let $$f$$ be a function holomorphic on $$U$$ except at some isolated singularities $$z_1,z_2,\cdots\in U\backslash(\text{image }\gamma)$$. Then

$$\oint_\gamma f(z)dz=2\pi i\sum_j n(\gamma;z_j)\text{Res}(f;z_j).$$

**Corollary** (Cauchy's residue theorem)**.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, let $$\gamma$$ be a counterclockwise oriented simple closed piecewise $$C^1$$ curve in $$U$$, and let $$f$$ be a function holomorphic on $$U$$ except at some isolated singularities $$z_1,z_2,\cdots\in U\backslash(\text{image }\gamma)$$. Then

$$\oint_\gamma f(z)dz=2\pi i\sum_{j=1}^n \text{Res}(f;z_j).$$

#### §5.4 Evaluation of Real Integrals
★**Remark** (Rational functions of $$\cos$$ and $$\sin$$)**.** Evaluate the integrals of the type

$$\int_0^{2\pi}R(\cos t,\sin t)dt,$$

where $$R$$ is a rational function: evaluate

$$\oint_{\partial D(0;1)}\frac{1}{z}R\left(\frac{z+z^{-1}}{2},{z-z^{-1}}{2i}\right)dz$$

along the counterclockwise oriented unit circle centered at the origin.       
★**Remark** (Rational functions)**.** To evaluate integrals of the type

$$\int_{-\infty}^{+\infty}\frac{p(t)}{q(t)}dt,$$

where $$p$$ and $$q$$ are polynomials with $$\text{deg }q\geq\text{deg }p+2$$, consider the line integral

$$\oint_\gamma\frac{p(z)}{q(z)}dz,$$

where $$\gamma$$ is the counterclockwise oriented boundary of a large semicircular disk centered at the origin, whose diameter coincides with the real axis.

<center><img src="http://sxubi.github.io/photos/semicircle.png" width = "150"/></center>

★**Remark** (Rational function times $$\cos$$ or $$\sin$$)**.** Evaluate integrals of the type 

$$\int_{-\infty}^{+\infty}\frac{p(t)}{q(t)}\cos t\,dt,\quad \int_{-\infty}^{+\infty}\frac{p(t)}{q(t)}\sin t\,dt,$$

where $$p$$ and $$q$$ are polynomials with $$\text{deg }q>\text{deg }p$$, consider the line integral 

$$\oint_\gamma \frac{p(z)}{q(z)}e^{iz}dz,$$

where $$\gamma$$ is the boundary of a large semicircular disk in the upper half-plane centered at the oigin whose diameter coincides with the real axis. When estimating the integral along the large semicircle, simply usen ML-estimate if $$\text{deg }q\geq \text{deg }p+2$$. In case $$\text{deg }q= \text{deg }p+1$$, use the Jordan's inequality: $$\sin t\geq \frac{2}{\pi}t$$ for every $$t\in[0,\pi/2]$$.         
★**Remark** (Logarithms)**.** Evaluate the integrals of the type

$$\int_0^{+\infty}R(t)\ln t\,dt,\quad \int_0^{+\infty}R(t)t^a\,dt,$$

where $$R$$ is a rational function and $$a$$ is not an integer, it's useful to consider the line integrals

$$\oint_\gamma R(z)\log z\,dz,\quad \oint_\gamma R(z)e^{a\log z}dz.$$

The branch of complex logarithm has to be defined on a simply connected region not containing 0, so the simple closed curve $$\gamma$$ has to be chosen in a way that avoids the point 0. The following indented path or key-hole path are natural choices of $$\gamma$$.

<center><img src="http://sxubi.github.io/photos/semicircle2.png" width = "370"/></center>

#### §5.5 Argument Principle
**Definition** (Meromorphic functions)**.** Let $$U\subseteq\mathbb{C}$$ be a region and $$f$$ be a function which is holomorphic on $$U$$ except at isolated singularities. We say that $$f$$ is a meromorphic function on $$U$$ if it has non essential singularities, i.e. the isolated singularities of $$f$$ are either removable singularities or poles. In this case we may extend the domain of $$f$$ to include its poles, and define $$F:U\to\mathbb{C}\cup\{\infty\}$$ by

$$F(z)=\lim_{w\to z}f(w).$$

★**Theorem** (Argument principle)**.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, let $$\gamma$$ be a counterclockwise oriented simple closed peicewise $$C^1$$ curve in $$U$$, and let $$f$$ be a meromorphic function on $$U$$, whose zeros and poles are in $$U\backslash(\text{image }\gamma)$$. Then the line integral

$$\frac{1}{2\pi i}\oint_\gamma\frac{f'(z)}{f(z)}dz$$

equals to the number of zeros of $$f$$ in the interior of $$\gamma$$ minus the number of poles of $$F$$ in the interior of $$\gamma$$, both counting multiplicities (each zero/pole of order $$n$$ is counted $$n$$ times).       
**Corollary** (Argument principle)**.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, let $$\gamma$$ be a counterclockwise oriented simple closed peicewise $$C^1$$ curve in $$U$$, and let $$f$$ be a meromorphic function on $$U$$, whose zeros and poles are in $$U\backslash(\text{image }\gamma)$$. Then the winding number of $$f\circ\gamma$$ around 0, $$n(f\circ\gamma;0)$$, equals to the number of zeros of $$f$$ in the interior of $$\gamma$$ minus the number of poles of $$F$$ in the interior of $$\gamma$$, both counting multiplicities (each zero/pole of order $$n$$ is counted $$n$$ times).       
★**Theorem** (Generalized argument principle)**.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, let $$\gamma$$ be a counterclockwise oriented simple closed peicewise $$C^1$$ curve in $$U$$, and let $$f$$ be a meromorphic function on $$U$$, whose zeros and poles are in $$U\backslash(\text{image }\gamma)$$, and let $$g:U\to\mathbb{C}$$ be a holomorphic function. If in the interior of $$\gamma$$, $$f$$ has a zero of order $$m_j$$ at $$a_j$$ for $$j\in\{1,2,\cdots,m\}$$ and has a pole of order $$n_k$$ at $$b_k$$ for $$k\in\{1,2,\cdots,n\}$$, then

$$\frac{1}{2\pi i}\oint_\gamma g(z)\frac{f'(z)}{f(z)}dz=\sum_{j=1}^m m_jg(a_j)-\sum_{k=1}^n n_kg(b_k).$$         


**Corollary.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, let $$\gamma$$ be a counterclockwise oriented simple closed peicewise $$C^1$$ curve in $$U$$, and let $$f:U\to V$$ be a holomorphic function which has an inverse $$f^{-1}:V\to U$$. Then for each $$w\in V$$ suchh that $$f^{-1}(w)$$ is in the interior of $$\gamma$$, we have

$$f^{-1}(w)=\frac{1}{2\pi i}\oint_\gamma\frac{zf'(z)}{f(z)-w}dz.$$

★**Theorem** (Rouché)**.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, let $$f,g:U\to\mathbb{C}$$ be holomorphic functions and let $$\gamma$$ be a simple closed curve in $$U$$. If 

$$|f(z)-g(z)|<|f(z)|+|g(z)|$$

for every $$z\in\text{image }\gamma$$, then $$f$$ and $$g$$ have the same number of zeros in the interior of $$\gamma$$, counting multiplicities.          
★**Corollary** (Rouché)**.** Let $$U\subseteq\mathbb{C}$$ be a simply connected region, let $$f,g:U\to\mathbb{C}$$ be holomorphic functions and let $$\gamma$$ be a simple closed curve in $$U$$. If 

$$|f(z)-g(z)|<|f(z)|.$$

for every $$z\in\text{image }\gamma$$, then $$f$$ and $$g$$ have the same number of zeros in the interior of $$\gamma$$, counting multiplicities.    

<center><b>THE END</b></center>
