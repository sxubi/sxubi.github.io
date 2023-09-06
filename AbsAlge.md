---
layout: page
mathjax: true
title: "Abstract Algebra"
date: 08/30/2023
---

### <center>Lecture 1</center>
**Definition** (Set)**.**  A *set* is a collection of objects.       
**Definition.** A statement is a sentence that can have a true value.        
**Definition.** The symbol $$\forall$$ means *for all*. The symbol $$\exists$$ means *there exists*. And $$\exists!$$ means "there exists a unique".    
**Defition** (Equality of sets)**.**  $$X$$ is equal to $$Y$$, written as $$X=Y$$ if $$\forall x, x\in X\Leftrightarrow x\in Y.$$     
**Definition** (Subset)**.**  $$X$$ is a *subset* of $$Y$$, written as $$X\subseteq Y$$ or $$X\subset Y$$, if all elements in $$X$$ are in $$Y$$, i.e. $$\forall x, x\in X\Rightarrow x\in Y$$.     
**Definition** (Intersection, union, set difference and power set). Given two sets $$X,Y$$,
* Intersection: $$X\cap Y=\{x:x\in X\text{ and }x\in Y\}$$
* Union: $$X\cup Y=\{x:x\in X\text{ or }x\in Y\}$$
* Set difference: $$X\backslash Y=\{x\in X:X\notin Y\}$$
* Power set: $$\mathscr{P}(x)=\{S:S\subseteq X\}$$

**Definition** (Ordered pair)**.**  An *order pair* $$(x,y)$$ is a pair of two items in which order matters. We have $$(x,y)=(x',y')$$ iff $$x=x',y=y'$$.       
**Definition** (Cartesian product)**.**  Given two sets $$X,Y$$, the *Cartesian product* of $$X$$ and $$Y$$ is $$X\times Y=\{(x,y):x\in X,y\in Y\}$$.      
**Definition** (Function)**.**  A *function* $$f:X\to Y$$ is a subset: $$\Gamma_f\subset X\times Y$$, called the *graph* of $$f$$, such that

$$\forall x\in X,\exists!y\in Y: (x,y)\in\Gamma_f.$$

This unique $$y$$ is denoted $$y=f(x)$$ and called the *value* of $$f$$ at $$x$$.     
**Terminology.** $$X$$ is the *domain* of $$f$$. $$Y$$ is the *codomain* of $$f$$. The *image* of $$X$$ under $$f$$ is the set

$$f(X)=\{y\in Y|\exists x\in X,f(x)=y\}.$$

### <center>Lecture 2</center>
**Definition** (Injective function)**.**  A function $$f:X\to Y$$ is *injective* if $$\forall x,y\in X, f(x)=f(y)\Rightarrow x=y.$$     
**Definition** (Surjective function)**.**  A function $$f:X\to Y$$ is *surjective* if $$\forall y\in Y, \exists x\in X,f(x)=y.$$     
**Definition** (Bijective function)**.**  A function is *bijective* if it is both injective and surjective.    
**Definition.** Let $$X,Y,Z$$ be sets and $$f:X\to Y, g:Y\to Z$$ be functions. Then the composition $$g\circ f$$ is the function $$g\circ f:X\to Z$$ such that $$\forall x\in X, (g\circ f)(x)=g(f(x))$$.    
**Definition.** Let $$X$$ be a set. The *identity function* is the function

$$\text{id}_X:X\to X\text{ such that }\forall x\in X, \text{id}_X(x)=x.$$

**Axiom** (Axiom of choice)**.**  Given a family of non-empty sets $$X_i,i\in I$$, there exists a choice function $$f:I\to U_{i\in I}X_i$$ such that $$f(i)\in X_i$$.     
**Definition.** A *relation* $$\mathcal{R}$$ on a set is a subset $$R\subseteq X\times X.$$ We write $$x\sim_\mathcal{R}y\Leftrightarrow (x,y)\in\mathcal{R}.$$    
**Definition** (Properties of relations)**.**  Let $$\mathcal{R}$$ be a relation on $$X$$.    
&emsp;1. It is *reflexive* if $$\forall x\in X,x\sim_\mathcal{R}x$$.     
&emsp;2. It is *symmetric* if $$\forall x,y\in X, x\sim_\mathcal{R}y\Rightarrow y\sim_\mathcal{R}x$$.     
&emsp;3. It is *transitive* if $$\forall x,y,z\in X,x\sim_\mathcal{R} y,y\sim_\mathcal{R}z\Rightarrow x\sim_\mathcal{R}z$$.     
**Definition** (Equivalence relation)**.**  A relation is an *equivalence relation* if it is reflexive, symmetric and transitive.    
**Definition** (Equivalence class)**.**  If $$\mathcal{R}$$ is an equivalence relation, then the *equivalence class* $$[x]$$ is the set of all elements that are related via $$\sim_\mathcal{R}$$ to $$x$$:

$$[x]=\{y\in X|(x,y)\in\mathcal{R}\}.$$

**Definition** (Quotient set)**.**  If $$\mathcal{R}$$ is an equivalence relation on $$X$$, then we denote the *quotient set*:

$$X/\mathcal{R}=\{[x]|x\in X\}.$$

Quotient set is the set of equivalence classes.    
**Definition** (Partition of a set)**.**  A *partition* of a set $$X$$ is a collection of subsets $$X_i$$ of $$X$$ such that each element of $$X$$ is in exactly one of $$X_i$$.    
**Theorem.** To give an equivalence relation on $$X$$ is the same as to give a partition of $$X$$.

### <center>Lecture 3</center>
**Definition** (Factor of integers)**.**  Given $$a,b\in\mathbb{Z}$$, we say $$a$$ *divides* $$b$$, $$a$$ is a *factor* of $$b$$, or $$a|b$$ if $$\exists c\in\mathbb{Z}, b=ac$$. For any $$b$$, $$\pm 1$$ and $$\pm b$$ are always factors of $$b$$. The other factors are called *proper factors*.       
**Theorem** (Division Algorithm). Given $$a,b\in\mathbb{N}, b\neq 0$$, there are unique $$q,r\in\mathbb{Z}$$ with 

$$a=qb+r,\quad 0\leq r<b.$$

**Definition** (Common factor of integers)**.**  A *common factor* of $$a$$ and $$b$$ is a number $$c\in\mathbb{Z}$$ such that $$c|a$$ and $$c|b$$.    
**Definition** (Greatest common divisor)**.**  The *greatest common divisor* $$\gcd(a,b)$$ of two numbers $$a,b\in\mathbb{N}$$ is a number $$d\in\mathbb{N}$$ such that     
&emsp;(1) $$d$$ is a common factor of $$a$$ and $$b$$, and    
&emsp;(2) if $$c$$ is also a common factor, $$c|d$$.    
**Proposition.** If $$c|a$$ and $$c|b$$, then $$c|(ua+vb)$$ for all $$u,v\in\mathbb{Z}$$.    
**Theorem.** Let $$a,b\in\mathbb{N}$$, then $$\gcd(a,b)$$ exists.    
**Corollary.** Let $$d=\gcd(a,b),$$ then $$d$$ is the smallest positive linear combination of $$a$$ and $$b$$.    
**Corollary.** (Bézout's identity)**.**  Let $$a,b\in\mathbb{N}$$ and $$c\in\mathbb{Z}$$. Then there exists $$u,v\in\mathbb{Z}$$ with $$c=ua+vb$$ iff $$\gcd(a,b)|c$$.     
**Proposition** (Euclid's Algorithm)**.**  If we continuously break down $$a$$ and $$b$$ by the following procedure:

$$\begin{align*}
a&=q_1b+r_1,\\
b&=q_2r_1+r_2,\\
r_1&=q_3r_2+r_3,\\
&\vdots\\
r_{n-2}&=q_nr_{n-1}.
\end{align*}$$

Then we have $$\gcd(a,b)=r_{n-1}$$.    
**Definition** (Modulo). If $$a,b\in\mathbb{Z}$$ have the same remainder after division by $$m$$, i.e. $$m|(a-b)$$, we say $$a$$ and $$b$$ are *congruent modulo* $$m$$, and write

$$a\equiv b\pmod m.$$

**Proposition.** If $$a\equiv b\pmod m$$, and $$d|m$$, then $$a\equiv b\pmod d$$.    
With $$m$$ fixed, $$a\equiv b\pmod m$$ is an equivalence class. The set of equivalence classes is written as $$\mathbb{Z}/(m\mathbb{Z})$$.    
**Proposition.** If $$a\equiv b\pmod m$$ and $$u\equiv v\pmod m$$, then $$a+u\equiv b+v\pmod m$$ and $$au\equiv bv\pmod m.$$

### <center>Lecture 4</center>
**Definition** (Binary operation)**.** A *binary operation* on a set $$S$$ is a way of combining two elements to get a new element, which is a map $$*:S\times S\to S.$$    
**Definition** (Group)**.** A *group* is a set $$G$$ with a binary operation $$*$$ satisfying the following axioms:    
&emsp;1. (Identity) There is some $$e\in G$$ such that for all $$a$$, $$a*e=e*a=a.$$     
&emsp;2. (Inverse) For all $$a\in G$$, there is some $$a^{-1}\in G$$ such that $$a*a^{-1}=a^{-1}*a=e$$.    
&emsp;3. (Associativity) For all $$a,b,c,\in G$$, we have $$(a*b)*c=a*(b*c)$$.    
