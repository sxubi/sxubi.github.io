---
layout: post
mathjax: true
categories: media
title: "Multivariable Calculus"
---

The purpose of this post is to help me memorize some equations for my Multivariable Calculus final exam. XD

#### Global Maximum and Minimum Values
Suppose $$f$$ is a continous function on a closed and bounded region $$R$$ on the $$xy$$-plane.

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
Suppose surface $$S$$ is traced out by a vector function $$\vec{A}(u,v)=<x(u,v),y(u,v),z(u,v)>$$ where $$a\leq u\leq b$$ and $$c\leq v\leq d$$. Then the surface area of $$S$$ is

$$\iint_R\left|\left(\frac{\partial\vec{r}}{\partial u}\right)\times\left(\frac{\partial\vec{r}}{\partial v}\right)\right|dvdu=\int_a^b \int_c^d\left|\left(\frac{\partial\vec{r}}{\partial u}\right)\times\left(\frac{\partial\vec{r}}{\partial v}\right)\right|dvdu.$$

Or suppose that $$S$$ is given by $$z=f(x,y)$$ then the surface arear of $$S$$ can be written as

$$\iint_R\sqrt{\left(\frac{\partial f}{\partial x}\right)^2+\left(\frac{\partial f}{\partial y}\right)^2+1}dA.$$

### Triple Integrals in Rectangular Coordinates
Suppose $$F(x,y,z)$$ is continuous on a closed and bounded region $$D$$ in 3-space. The triple integral is given by

$$\iiint_D F(x,y,z)dV=\int_a^b \int_{g_1(x)}^{g_2(x)} \int_{f_1(x,y)}^{f_2(x,y)} F(x,y,z)dzdydx.$$

### Triple Integrals in Cylinder Coordinates
Suppose $$F(x,y,z)$$ is continuous on a closed and bounded region $$D$$ in 3-space. The triple integral is given by

$$\iiint_D F(x,y,z)dV = \iiint_D F(r\cos\theta,r\sin\theta,z)dzrdrd\theta.$$

### Triple Integrals in Spherical Coordinates
Suppose $$F(x,y,z)$$ is continuous on a closed and bounded region $$D$$ in 3-space. The triple integral is given by

$$\iiint_D F(x,y,z)dV=\iiint_D F(\rho\sin\phi\cos\theta,\rho\sin\phi\sin\theta,\rho\cos\phi)\rho^2\sin\phi d\rho d\phi d\theta.$$
