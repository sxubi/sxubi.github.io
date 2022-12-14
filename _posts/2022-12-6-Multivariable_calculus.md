---
layout: post
mathjax: true
categories: media
title: "Multivariable Calculus Notes"
---

The purpose of this post is to help me memorize some equations for my Multivariable Calculus final exam. XD

#### Quadirc Surfaces
* Ellipsoid: $$\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=1.$$
* Elliptic Paraboloid: $$z=\frac{x^2}{a^2}+\frac{y^2}{b^2}.$$
* Hyperboloid of one sheet: $$\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}=1.$$
* Hyperboloid of two sheets: $$-\frac{x^2}{a^2}-\frac{y^2}{b^2}+\frac{z^2}{c^2}=1.$$
* Elliptic cone: $$\frac{x^2}{a^2}+\frac{y^2}{b^2}=\frac{z^2}{c^2}.$$
* Hyperbolic Paraboloid: $$z=\frac{x^2}{a^2}-\frac{y^2}{b^2}.$$

#### Arc length
Suppose a curve is described by $$\vec{r}(t)=<x(t),y(t),z(t)>, a\leq t\leq b$$.Then the arc length of this curve is

$$l=\int ds=\int_a^b |\vec{r}'(t)|dt.$$

#### Limits
Let $$z=f(x,y)$$. If $$|f(x,y)-L|$$ approaches 0 as $$f(x,y)$$ is getting closer and closer to $$(x_0,y_0$$, then

$$\lim_{(x,y)\to(x_0,y_0)}f(x,y)=L.$$

**Two-path test** for non-existence of limits: If $$f$$ has different limits along two different paths in the natural domain of $$f$$ as $$(x,y)$$ approaches $$(x_0,y_0)$$, then the limit $$\lim_{(x,y)\to(x_0,y_0)}f(x,y)=L$$ does not exist.

**Continuity**: $$z=f(x,y)$$ is continous at point $$(x_0,y_0)$$ if 

$$\lim_{(x,y)\to(x_0,y_0)}f(x,y)=f(x_0,y_0).$$

#### Partial Derivative
$$z=f(x,y)$$ is a continuous function of two variables. Then the partial derivative is defined as

$$f_x(x,y)=\frac{\round f}{\round x}=\lim_{h\to 0}\frac{f(x+h,y)-f(x,y)}{h},$$


$$f_y(x,y)=\frac{\round f}{\round y}=\lim_{h\to 0}\frac{f(x,y+h)-f(x,y)}{h},$$

**Mixed derivative theorem**: If $$z=f(x,y)$$ and $$f_x\, ,f_y\, ,f_{xy}\, ,f_{yx}$$ are all continuous, then

$$f_{xy}(a,b)=f_{yx}(a,b).$$

#### Chain Rule
Draw the dependence chart to determine the chain rule.

#### Gradient Vector
The gradient vector is defined as 

$$\nabla f(x,y,z)=<f_x,f_y,f_z>.$$

The gradient vector must be perpendicular to the level curve (surface) tha passing through the point.

#### Directional Derivative
The directional derivative of $$z=f(x,y)$$ at point $$(a,b)$$ in the direction of $$\vec{u}$$ (a unit vector) is 

$$D_{\vec{u}}f(a,b)=\vec{u}\cdot\nabla f(a,b).$$

At point $$(a,b)$$, the function increases most rapidly in the direction of the gradient vector.

#### Tangent Planes and Normal Lines
The **tangent plane** to the level surface $$g(x,y,z)=k$$ at point $$(a,b,c)$$ can be described as

$$\langle x-a,y-b,z-c\rangle \cdot \nabla g(a,b,c)=0.$$

The **normal line** to the level surface $$g(x,y,z)=k$$ at point $$(a,b,c)$$ can be described as

$$x=a+g_x t,\quad y=b+g_y t,\quad z=c+g_z t.$$

If two surfaces $$f$$ and $$g$$ intersect, and one wants to find the tangent line of the intersection curve, then compute $$\nabla f\times \nabla g$$ at the intersection point $$P_0$$.


#### Linear Approximation
Linear Approximation to $$z=f(x,y)$$ at point $$(x_0,y_0,f(x_0,y_0))$$ is

$$L(x,y)=f(x_0,y_0)+f_x(x-x_0)+f_y(y-y_0).$$

**Total differential** of $$f$$ is defined as

$$df=f_x dx+f_y dy.$$

#### Local Maximum and Minimum Values
**First derivative test**: If $$z=f(x,y)$$ has a local maximum or minimum at $$(a,b)$$, then

$$f_x(a,b)=f_y(a,b)=0.$$

**Second derivative test**: If we already had $$f_x(a,b)=f_y(a,b)=0,$$ then
* $$f$$ has a local maximum at $$(a,b)$$ if $$f_{xx}<0$$ and $$f_{xx}f_{yy}-f_{xy}^2>0$$.
* $$f$$ has a local minimum at $$(a,b)$$ if $$f_{xx}>0$$ and $$f_{xx}f_{yy}-f_{xy}^2>0$$.
* $$f$$ has a saddle point at $$(a,b)$$ if $$f_{xx}f_{yy}-f_{xy}^2<0$$.

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

$$\iint_R f(x,y)dA=\int_a^b \int_c^d f(x,y)dy\,dx=\int_c^d \int_a^b f(x,y)dx\,dy.$$

#### Double Integral on General Region
Suppose $$z=f(x,y)$$ is a continuous function on region $$R:a\leq x\leq b, g_1(x)\leq y\leq g_2(x)$$, then

$$\iint_R f(x,y)dA=\int_a^b \int_{g_1(x)}^{g_2(x)} f(x,y)dy\,dx.$$

Suppose $$z=f(x,y)$$ is a continuous function on region $$R:c\leq x\leq d, h_1(y)\leq x\leq h_2(y)$$, then

$$\iint_R f(x,y)dA=\int_c^d \int_{h_1(y)}^{h_2(y)} f(x,y)dx\,dy.$$

#### Double Integrals in Polar coordinates
Suppose $$z=f(x,y)$$ is continuous over region $$R$$, then we have

$$\iint_R f(x,y)dA=\iint_G f(r\cos\theta,r\sin\theta)r\,dr\,d\theta.$$

Note that $$x=r\cos\theta$$, $$y=r\sin\theta$$ and $$dA=r\,dr\,d\theta$$.

#### Surface Area
Suppose surface $$S$$ is traced out by a vector function $$\vec{r}(u,v)=<x(u,v),y(u,v),z(u,v)>$$ where $$a\leq u\leq b$$ and $$c\leq v\leq d$$. Then the surface area of $$S$$ is

$$\iint_R\left|\left(\frac{\partial\vec{r}}{\partial u}\right)\times\left(\frac{\partial\vec{r}}{\partial v}\right)\right|dvdu=\int_a^b \int_c^d\left|\left(\frac{\partial\vec{r}}{\partial u}\right)\times\left(\frac{\partial\vec{r}}{\partial v}\right)\right|dv\,du.$$

Or suppose that $$S$$ is given by $$z=f(x,y)$$ then the surface area of $$S$$ can be written as

$$\iint_R\sqrt{\left(\frac{\partial f}{\partial x}\right)^2+\left(\frac{\partial f}{\partial y}\right)^2+1}dA.$$

#### Surface Integral
Suppose surface $$S$$ is traced out by a vector function $$\vec{r}(u,v)=<x(u,v),y(u,v),z(u,v)>.$$ $$w=G(x,y,z)$$ is continuous. Then

$$\iint_S G(x,y,z)dS=\iint_{R_{uv}}G(x(u,v),y(u,v),z(u,v))\left|\left(\frac{\partial\vec{r}}{\partial u}\right)\times\left(\frac{\partial\vec{r}}{\partial v}\right)\right|dv\,du.$$

This can also be written as

$$\iint_S G(x,y,z)dS=\iint_{R_{xy}}G(x,y,f(x,y))\sqrt{\left(\frac{\partial f}{\partial x}\right)^2+\left(\frac{\partial f}{\partial y}\right)^2+1}dA.$$

#### Triple Integrals in Rectangular Coordinates
Suppose $$F(x,y,z)$$ is continuous on a closed and bounded region $$D$$ in 3-space. The triple integral is given by

$$\iiint_D F(x,y,z)dV=\int_a^b \int_{g_1(x)}^{g_2(x)} \int_{f_1(x,y)}^{f_2(x,y)} F(x,y,z)dz\,dy\,dx.$$

#### Triple Integrals in Cylinder Coordinates
Suppose $$F(x,y,z)$$ is continuous on a closed and bounded region $$D$$ in 3-space. The triple integral is given by

$$\iiint_D F(x,y,z)dV = \iiint_D F(r\cos\theta,r\sin\theta,z)dz\,r\,dr\,d\theta.$$

#### Triple Integrals in Spherical Coordinates
Suppose $$F(x,y,z)$$ is continuous on a closed and bounded region $$D$$ in 3-space. The triple integral is given by

$$\iiint_D F(x,y,z)dV=\iiint_D F(\rho\sin\phi\cos\theta,\rho\sin\phi\sin\theta,\rho\cos\phi)\rho^2\,\sin\phi\,d\rho \,d\phi\, d\theta.$$

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

$$\int_C \vec{F}\cdot d\vec{r}=\int_C \vec{F}(x,y,z)\cdot \frac{dr}{dt}dt.$$

This could be also written as

$$\int_C \vec{F}(x,y,z)\cdot d\vec{r} = \int_C Mdx+Ndy+Pdz.$$

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

Let $$C$$ be a simple closed curve with **positive orientation**, let $$C_1, C_2, ... ,C_n$$ be simple closed curves with **negative orientation**. Let $$\Omega$$ be the region interior to the curve $$C$$ and exterior to $$C_1, C_2, ... ,C_n$$. The total boundary curve of $$\Omega$$ is denoted by $$\Gamma$$.

$$\int_\Gamma pdx+qdy=\iint_\Omega \left(\frac{\partial q}{\partial x}-\frac{\partial p}{\partial y}\right)dA.$$

#### Flux of Vector Fields
The **flux** of vector field $$\vec{F}(x,y,z)$$ across an oriented surface $$S$$ in the direction of $$\vec{n}$$ is defined as

$$\iint_S \vec{F}\cdot\vec{n}dS.$$

If the surface is traced out by $$\vec{r}(u,v)=<x(u,v),y(u,v),z(u,v)>.,$$ this could be simplified as

$$\iint_S \vec{F}\cdot\vec{n}dS=\iint_{R_{uv}}\vec{F}\cdot\left|\left(\frac{\partial\vec{r}}{\partial u}\right)\times\left(\frac{\partial\vec{r}}{\partial v}\right)\right|dv\,du.$$

#### Divergence
The **divergence** of a vector field $$\vec{F}(x,y,z)=M(x,y,z)\vec{i}+N(x,y,z)\vec{j}+P(x,y,z)\vec{k}$$ is defined as 

$$\text{div}\vec{F}=\nabla\cdot\vec{F}=\frac{\partial M}{\partial x}+\frac{\partial N}{\partial y}+\frac{\partial P}{\partial z}.$$

If $$S$$ is a closed surface enclosing solid $$D$$ and $$\vec{n}$$ is the **outward unit normal vector**, then

$$\iint_S \vec{F}\cdot\vec{n}dS=\iiint_D \text{div}\vec{F}dV.$$
