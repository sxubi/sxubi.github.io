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

$$|f(z)-L<\varepsilon|,\quad \text{whenever }z\in U\text{ and }0<|z-a|<\delta,$$

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