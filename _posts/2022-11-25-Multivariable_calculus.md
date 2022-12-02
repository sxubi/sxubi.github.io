---
layout: post
mathjax: true
categories: media
title: "Multivariable Calculus Notes"
---

The purpose of this post is to help me memorize some equations for my Multivariable Calculus final exam. XD

#### Global Maximum and Minimum Values
Suppose $$f$$ is a continuous function on a closed and bounded region $$R$$ on the $$xy$$-plane.

(1) List the interior points of $$R$$ where $$f$$ may have local maxima and mimima;

(2) List the boundary points of $$R$$ where $$f$$ may have local maxima and mimima;

(3) Look through the lists for the maximum and minimum values of $$f$$.


#### Lagrange Multiplier
Suppose there's a point $$P(a,b,c)$$ such that $$w=f(x,y,z)$$ has a maximum or minimum value at $$P(a,b,c)$$ subject to the constraint $$g(x,y,z)=k$$. Then the point is given by

$$ \nabla f(a,b,c)=\lambda\nabla g(a,b,c)\quad\text{and}\quad g(a,b,c)=k.$$

#### Double Integral on Rectangular Region
Suppose $$z=f(x,y)$$ is a continuous function on region $$R:a\leq x\leq b, c\leq y\leq d.$$ Then 

$$\iint_R f(x,y)dA=\int_a^b \int_c^d f(x,y)dydx=\int_c^d \int_a^b f(x,y)dxdy.$$

#### Double Integral on General Region
Suppose $$z=f(x,y)$$ is a continuous function on region $$R:a\leq x\leq b, g_1(x)\leq y\leq g_2(x)$$, then

$$\iint_R f(x,y)dA=\int_a^b \int_{g_1(x)}^{g_2(x)} f(x,y)dydx.$$

Suppose $$z=f(x,y)$$ is a continuous function on region $$R:c\leq x\leq d, h_1(y)\leq x\leq h_2(y)$$, then

$$\iint_R f(x,y)dA=\int_c^d \int_{h_1(y)}^{h_2(y)} f(x,y)dxdy.$$

#### Double Integrals in Polar coordinates
Suppose $$z=f(x,y)$$ is continuous over region $$R$$, then we have

$$\iint_R f(x,y)dA=\iint_G f(r\cos\theta,r\sin\theta)rdrd\theta.$$

Note that $$x=r\cos\theta$$, $$y=r\sin\theta$$ and $$dA=rdrd\theta$$.

#### Surface Area
Suppose surface $$S$$ is traced out by a vector function $$\vec{r}(u,v)=<x(u,v),y(u,v),z(u,v)>$$ where $$a\leq u\leq b$$ and $$c\leq v\leq d$$. Then the surface area of $$S$$ is

$$\iint_R\left|\left(\frac{\partial\vec{r}}{\partial u}\right)\times\left(\frac{\partial\vec{r}}{\partial v}\right)\right|dvdu=\int_a^b \int_c^d\left|\left(\frac{\partial\vec{r}}{\partial u}\right)\times\left(\frac{\partial\vec{r}}{\partial v}\right)\right|dvdu.$$

Or suppose that $$S$$ is given by $$z=f(x,y)$$ then the surface area of $$S$$ can be written as

$$\iint_R\sqrt{\left(\frac{\partial f}{\partial x}\right)^2+\left(\frac{\partial f}{\partial y}\right)^2+1}dA.$$

#### Surface Integral
Suppose surface $$S$$ is traced out by a vector function $$\vec{r}(u,v)=<x(u,v),y(u,v),z(u,v)>. $$w=G(x,y,z)$$ is continuous. Then

$$\iint_S G(x,y,z)dS=\iint_{R_{uv}}G(x(u,v),y(u,v),z(u,v))\left|\left(\frac{\partial\vec{r}}{\partial u}\right)\times\left(\frac{\partial\vec{r}}{\partial v}\right)\right|dvdu.$$

This can also be written as

$$\iint_S G(x,y,z)dS=\iint_{R_{xy}}G(x,y,f(x,y))\sqrt{\left(\frac{\partial f}{\partial x}\right)^2+\left(\frac{\partial f}{\partial y}\right)^2+1}dA.$$

#### Triple Integrals in Rectangular Coordinates
Suppose $$F(x,y,z)$$ is continuous on a closed and bounded region $$D$$ in 3-space. The triple integral is given by

$$\iiint_D F(x,y,z)dV=\int_a^b \int_{g_1(x)}^{g_2(x)} \int_{f_1(x,y)}^{f_2(x,y)} F(x,y,z)dzdydx.$$

#### Triple Integrals in Cylinder Coordinates
Suppose $$F(x,y,z)$$ is continuous on a closed and bounded region $$D$$ in 3-space. The triple integral is given by

$$\iiint_D F(x,y,z)dV = \iiint_D F(r\cos\theta,r\sin\theta,z)dzrdrd\theta.$$

#### Triple Integrals in Spherical Coordinates
Suppose $$F(x,y,z)$$ is continuous on a closed and bounded region $$D$$ in 3-space. The triple integral is given by

$$\iiint_D F(x,y,z)dV=\iiint_D F(\rho\sin\phi\cos\theta,\rho\sin\phi\sin\theta,\rho\cos\phi)\rho^2\sin\phi d\rho d\phi d\theta.$$

#### Line Integrals
Suppose $$z=f(x,y)$$ is countinous in a region containing a smooth curve $$C$$. $$C$$ is traced out by th vector function $$\vec{r}(t)=<x(t),y(t),z(t)>,$$ where $$a\leq t\leq b$$, then 

$$\int_C f(x,y)ds=\int_a^b f(x(t),y(t),z(t)) \left|\frac{d\vec{r}}{dt}\right|dt.$$

#### Vector Field
The function $$\vec{F}$$ is called a **vector field** over the solid region $$R$$

$$\vec{F}(x,y,z)=M(x,y,z)\vec{i}+N(x,y,z)\vec{j}+P(x,y,z)\vec{k}.$$

The **gradient field** of a differentiable function $$w=f(x,y,z)$$ is 

$$\nabla f(x,y,z)=<\frac{\partial f}{\partial x},\frac{\partial f}{\partial y},\frac{\partial f}{\partial z}>.$$

#### Work Done (Fluid's flow)
The **work done** by a vector field $$\vec{F}(x,y,z)=M(x,y,z)\vec{i}+N(x,y,z)\vec{j}+P(x,y,z)\vec{k}$$ in moving an object over a smooth curve $$C$$ given by $$\vec{r}(t)=<x(t),y(t),z(t)>$$ is

$$\int_C \vec{F}dr=\int_C \vec{F}(x,y,z)\frac{dr}{dt}dt.$$

This could be also written as

$$\int_C \vec{F}(x,y,z)dr = \int_C Mdx+Ndy+Pdz.$$

#### Flux across a Curve
Suppose curve $$C$$ is a smooth closed curve of $$\vec{F}(x,y)$$ in the $$xy$$-plane, and $$\vec{n}$$ is the *outward-pointing unit vector on the curve* $$C$$, then the flux of $$\vec{F}$$ across the curve $$C$$ is defined as 

$$\int_C \vec{F}\cdot\vec{n}ds=\int_a^b \vec{F}(x(t),y(t))\cdot<\frac{dy}{dt},-\frac{dx}{dt}>dt.$$

#### Conservative Vector Field
Suppose $$C$$ is a smooth curve joining points $$A$$ and $$B$$ and given by $$\vec{r}(t)$$. $$f$$ is a differentiable function with a continuous gradient vector $$\nabla f(x,y,z) = \vec{F}(x,y,z)$$. Then we have

$$\int_C \vec{F}\cdot d\vec{r}=\int_C \nabla f\cdot d\vec{r}=f(B)-f(A).$$

Suppose $$\vec{F}(x,y,z)=M(x,y,z)\vec{i}+N(x,y,z)\vec{j}+P(x,y,z)\vec{k}$$, then $$\vec{F}(x,y,z)$$ is **conservative** if and only if 

$$
\text{curl}\vec{F}=\nabla\times\vec{F}=
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k} \\
\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
M & N & P 
\end{vmatrix}
=\vec{0},
$$

where 

$$\nabla = <\frac{\partial}{\partial x} , \frac{\partial}{\partial y} , \frac{\partial}{\partial z} >.$$

#### Green's Theorem
Suppose $$C$$ is a smooth, simple and **closed** curve enclosing a region $$R$$. Then

$$\oint_C \vec{F}\cdot d\vec{r}=\iint_R \text{curl}\vec{F}\cdot\vec{k}dA.$$

The closed curve $$C$$ is required to be in the **counterclockwise direction** (positive orientation).

Let $$C$$ be a simple closed curve with **positive orientation**, let $$C_1, C_2, ... ,C_n$$ be simple closed curves with **negative orientation**. Let $$\omega$$ be the region interior to the curve $$C$$ and exterior to $$C_1, C_2, ... ,C_n$$. The total boundary curve of $$\omega$$ is denoted by $$\Gamma$$.

$$\ing_Gamma pdx+qdy=\iint_\omega \left(\frac{\partial q}{\partial x}-\partial p}{\partial y}\right)dA.$$

#### Flux of Vector Fields
The **flux** of vector field $$\vec{F}(x,y,z)$$ across an oriented surface $$S$$ in the direction of $$\vec{n}$$ is defined as

$$\iint_S \vec{F}\cdot\vec{n}dS.$$

#### Divergence
The **divergence** of a vector field $$\vec{F}(x,y,z)=M(x,y,z)\vec{i}+N(x,y,z)\vec{j}+P(x,y,z)\vec{k}$$ is defined as 

$$\text{div}\vec{F}=\nabla\cdot\vec{F}=\frac{\partial M}{\partial x}+\frac{\partial N}{\partial y}+\frac{\partial P}{\partial z}.$$

If $$S$$ is a closed surface enclosing solid $$D$$ and $$\vec{n}$$ is the **outward unit normal vector**, then

$$\iint_S \vec{F}\cdot\vec{n}dS=\iiint_D \text{div}\vec{F}dV.$$
