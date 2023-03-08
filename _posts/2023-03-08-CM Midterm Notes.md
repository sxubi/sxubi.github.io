---
layout: post
mathjax: true
categories: media
title: "CM Midterm Summary"
---

## I. Oscillations
### Undamped Oscillation
Consider $$m\ddot{x}+kx=0$$. The general solution is given by 


### Nondriven Damped Oscillation
Now we have $$m\ddot{x}+b\dot{x}+kx=0.$$ The characteristic equation is $$mr^2+br+k=0$$ with solution $$r_1,r_2$$

(1) **Underdamped**: $$b<\sqrt{2mk}$$. Suppose $$r=\lambda\pm\mu$$. The general solution is

$$x(t)=e^{\lambda t}(c_1\cos\mu t+c_2\sin\mu t).$$

(2) **Critical damped**: $$b=\sqrt{2mk}$$. The general solution is

$$x(t)=(c_1+c_2t)e^{rt}.$$

(3) **Overdamped**: $$b>\sqrt{2mk}$$. The general solution is

$$x(t)=c_1e^{r_1t}+c_2e^{r_2t}.$$

### Driven Oscillation
Now consider $$m\ddot{x}+b\dot{x}+kx=F_0\cos(\omega t).$$ The homogeneous part of solutions are the same as nondriven ones. The particular solution is given by

$$x_P(t)=A(\omega)\cos(\omega t-\phi),$$

where
$$A(\omega)=\frac{F_0/m}{\sqrt{(\omega_0-\omega)^2+b^2\omega^2/m^2}},$$

$$\tan\phi=\frac{b\omega/m}{\omega_0-\omega},\quad \omega_0=\sqrt{\frac{k}{m}}.$$

## II. Projectile of Motion


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

## IV. Conservative Force


