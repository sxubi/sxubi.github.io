---
layout: post
mathjax: true
categories: media
title: "Classical Mechanics 1"
---
*Based on HKUST PHYS3032 Classical Mechanics.*
## I. Oscillations
### Undamped Oscillation
Consider $$m\ddot{x}+kx=0$$. The general solution is given by 
$$x(t)=A\cos\omega t+B\sin\omega t.$$

### Nondriven Damped Oscillation
Now we have $$m\ddot{x}+b\dot{x}+kx=0.$$ The characteristic equation is $$mr^2+br+k=0$$ with solution $$r_1,r_2$$

(1) **Underdamped**: $$b<\sqrt{2mk}$$. Suppose $$r=\lambda\pm\mu i$$. The general solution is

$$x(t)=e^{\lambda t}(c_1\cos\mu t+c_2\sin\mu t).$$

(2) **Critical damped**: $$b=\sqrt{2mk}$$. The general solution is

$$x(t)=(c_1+c_2t)e^{rt}.$$

(3) **Overdamped**: $$b>\sqrt{2mk}$$. The general solution is

$$x(t)=c_1e^{r_1t}+c_2e^{r_2t}.$$

### Driven Oscillation
Now consider $$m\ddot{x}+b\dot{x}+kx=F_0\cos(\omega t).$$ The homogeneous part of solutions are the same as nondriven ones. The particular solution is given by

$$x_P(t)=A(\omega)\cos(\omega t-\phi),$$

where

$$\begin{align*}A(\omega)&=\frac{F_0/m}{\sqrt{(\omega_0^2-\omega^2)^2+b^2\omega^2/m^2}},\\
\tan\phi&=\frac{b\omega/m}{\omega_0^2-\omega^2},\quad \omega_0=\sqrt{\frac{k}{m}}.
\end{align*}$$

Two special cases:
**Forced oscillations without damping**: $$m\ddot{x}+kx=F_0\cos(\omega t).$$    
(1) If $$\omega\neq\omega_0$$, the general solution is given by

$$x=c_1\sin\omega_0 t+c_2\cos\omega_0 t+\frac{F_0}{m(\omega_0^2-\omega^2)}\cos\omega t.$$

If $$x(0)=0,x'(0)=0$$, then we have

$$\begin{align*}x(t) &= \frac{F_0}{m(\omega_0^2-\omega^2)}(\cos\omega t-\cos\omega_0 t)\\
&= \frac{2F_0}{m(\omega_0^2-\omega^2)}\sin\frac{(\omega_0-\omega)t}{2}\sin\frac{(\omega_0+\omega)t}{2}.
\end{align*}$$

If $$\omega_0-\omega$$ is small, then it's called a **beat**.

(2) If $$\omega=\omega_0$$, the general solution is

$$x=c_1\sin\omega_0 t+c_2\cos\omega_0 t+\frac{F_0}{2m\omega_0}t\sin\omega_0 t.$$

## II. Projectile of Motion
Stoke's drag: $$\vec f_D=-m\kappa\vec v $$. The solution is given by

$$\begin{align*}
x(t)&=\frac{u_x}{\kappa}(1-e^{-\kappa t}),\\
y(t)&=-\frac{g}{\kappa}t+\frac{1}{\kappa}\left(u_y+\frac{g}{\kappa}\right)(1-e^{-\kappa t}).
\end{align*}$$

## III. Non-Inertial Frame of Reference
Consider a fixed inertial frame $$S$$ and a rotating coordinate system $$S'$$ rotating with angular velocity $$\vec\omega$$. For a moving object, we have

$$\begin{align*}\vec v &=\vec v'+\vec\omega\times\vec r'+\vec V_0\\
\vec a &=\vec a'+\dot{\vec\omega}\times \vec r'+2\vec\omega\times \vec v'+\vec\omega\times(\vec\omega\times \vec r')+\vec A_0.
\end{align*}$$

The equation of motion for an object in the noninertial frame is

$$\vec F-m\vec A_0-2m\vec\omega\times\vec v'-m\dot{\vec\omega}\times \vec r'-m\vec\omega\times(\vec\omega\times\vec r')=m\vec a'.$$

where

$$\begin{align*}
&\vec F'_{Cor} =-2m\vec\omega\times\vec v',\\
&\vec F'_{trans} =-m\dot{\vec\omega}\times \vec r',\\
&\vec F'_{centrif} =-m\vec\omega\times(\vec\omega\times\vec r').
\end{align*}$$

To conclude,

$$\vec F'=\vec F_{physical}+\vec F'_{Cor}+\vec F'_{trans}+\vec F'_{centrif}-m\vec A_0.$$

**Remark**:For any quantity in a fixed and rotating coordinate with the same origin, we have
$$\left(\frac{d\vec Q}{dt}\right)_\text{fixed}=\left(\frac{d\vec Q}{dt}\right)_\text{rot}+\vec \omega\times\vec Q.$$
## IV. Conservative Force
Some properties for conservative force $$F$$:

(1) Work done for any closed loop is 0:

$$\forall C,\quad \oint_C \vec F\cdot d\vec r=0.$$

(2) The circulation of $$F$$ is zero:

$$\text{curl}\vec F=\nabla\times\vec F=0.$$

(3) There exists a potential function $$U$$ such that

$$\vec F=-\nabla U.$$

The potential difference between two point $$A$$ and $$B$$ is given by

$$U(B)-U(A)=\int_C \vec F\cdot d\vec r.$$

(4) The total energy satisfies

$$T_i+U_i=T_f+U_f.$$
