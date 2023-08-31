---
layout: page
mathjax: true
title: "Abstract Algebra"
date: 08/30/2023
---
Reference: *A first course in abstract algebra*, 3rd Edtion, by J. Rotman. Please note that this post is only for personal learning purposes and has no commercial use. The copyright belongs to the author of the textbook.

#### <center>Lecture 1</center>
**Definition** (Set). A *set* is a collection of objects.       
**Definition.** A statement is a sentence that can have a true value.        
**Definition.** The symbol $$\forall$$ means *for all*. The symbol $$\exists$$ means *there exists*. And $$\exists!$$ means "there exists a unique".    
**Defition** (Equality of sets). $$X$$ is equal to $$Y$$, written as $$X=Y$$ if $$\forall x, x\in X\Leftrightarrow x\in Y.$$     
**Definition** (Subset). $$X$$ is a *subset* of $$Y$$, written as $$X\subseteq Y$$ or $$X\subset Y$$, if all elements in $$X$$ are in $$Y$$, i.e. $$\forall x, x\in X\Rightarrow x\in Y$$.     
**Definition** (Intersection, union, set difference and power set). Given two sets $$X,Y$$,
* Intersection: $$X\cap Y=\{x:x\in X\text{ and }x\in Y\}$$
* Union: $$X\cup Y=\{x:x\in X\text{ or }x\in Y\}$$
* Set difference: $$X\backslash Y=\{x\in X:X\notin Y\}$$
* Power set: $$\mathscr{P}(x)=\{S:S\subseteq X\}$$

**Definition** (Ordered pair). An *order pair* $$(x,y)$$ is a pair of two items in which order matters. We have $$(x,y)=(x',y')$$ iff $$x=x',y=y'$$.       
**Definition** (Cartesian product). Given two sets $$X,Y$$, the *Cartesian product* of $$X$$ and $$Y$$ is $$X\times Y=\{(x,y):x\in X,y\in Y\}$$.      
**Definition** (Function). A *function* $$f:X\to Y$$ is a subset: $$\Gamma_f\subset X\times Y$$, called the *graph* of $$f$$, such that

$$\forall x\in X,\exists!y\in Y: (x,y)\in\Gamma_f.$$

This unique $$y$$ is denoted $$y=f(x)$$ and called the *value* of $$f$$ at $$x$$.     
**Terminology.** $$X$$ is the *domain* of $$f$$. $$Y$$ is the *codomain* of $$f$$. The *image* of $$X$$ under $$f$$ is the set

$$f(X)=\{y\in Y|\exists x\in X,f(x)=y\}.$$

#### <center>Lecture 2</center>
**Definition** (Injective function). A function $$f:X\to Y$$ is *injective* if $$\forall x,y\in X, f(x)=f(y)\Rightarrow x=y.$$     
**Definition** (Surjective function). A function $$f:X\to Y$$ is *surjective* if $$\forall y\in Y, \exists x\in X,f(x)=y.$$     
**Definition** (Bijective function).
