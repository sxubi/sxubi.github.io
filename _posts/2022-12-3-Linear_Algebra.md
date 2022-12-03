---
layout: post
mathjax: true
categories: media
title: "Linear Algebra Notes"
---

This post aims to conclude some common algorithm in Linear Algebra, since I guess there would be many calculations in our final exam. LOL

#### Row reduced echelon form (RREF)
Just perform the **elementary row operations**: replacement, scaling and interchange.

#### Solutions of linear system
For a matrix $$A$$, do row operations to $$RREF(A)$$.
* The system has 0 solutions if the last column is a pivot column.
* The system has 1 solutions if the last column is not a pivot column and there are no free variables.
* Otherwise the system has infinitely many solutions.

#### Linear independence
The columns of matrix $$A$$ are linearly independent if and only if $$A$$ has a pivot postion in every column.

#### Span
Suppose $$A$$ is an $$m\times n$$ matrix. The span of columns of $$A$$ is $$\mathbb{R}^m$$ if and only if $$A$$ has a pivot position in every row.

#### Invertible matrix
A matrix $$A$$ is invertible if and only if $$\det(A)\neq0.$$ To compute $$A^{-1}$$, we have

$$RREF([A\quad I_n])=[I_n\quad A^{-1}].$$

#### Basis of $$\text{Col}A$$ and $$\text{Nul}A$$
For a matrix $$A$$, the pivot columns of $$A$$ forms a basis for $$\text{Col}A$$. The basis of linear system $$Ax=0$$ forms a basis for $$\text{Nul}A$$.

#### Determinant
Suppose $$A$$ is a $$n\times n$$ matrix. Then

$$\det A=\sum_{X\in S_n}\text{prod}(X,A)(-1)^{\text{inv}(X)}.$$

One can also expand one row or one column to compute $$\det A$$. For a $$2\times 2$$ matrix $$A$$, we have

$$A^{-1}=\frac{1}{ad-bc}\begin{bmatrix}
d & -b\\
-c & a
\end{bmatrix}.$$

#### Diagonalization
First we compute the equation $$\det(A-\lambda I)=0$$ and obtain the **eigenvalues** of matrix $$A$$. The eigenvalues form the diagonal entries of diagonal matrix $$D$$. Then for each eigenvalue $$\lambda$$, compute the basis for $$\text{Nul}(A-\lambda I).$$ Those basis forms the column of matrix $$P$$. And hence we have

$$A=PDP^{-1}.$$

#### Orthogonal complement
Suppose $$A$$ is an $$m\times n$$ matrix. Then

$$(\text{Col}A)^\perp=\text{Nul}(A^T).$$

#### Orthogonal projection
Let $$W\subseteq\mathbb{R}$$ be a subspace. Suppose $$u_1,u_2,...,u_p$$ is an orthogonal basis for $$W$$. The orthogonal projection of vector $y$ onto $$W$$ is

$$proj_W(y)=\hat{y}=\frac{y\cdot u_1}{u_1 \cdot u_1}u_1+\frac{y\cdot u_2}{u_2 \cdot u_2}u_2+\cdots \frac{y\cdot u_p}{u_p \cdot u_p}u_p.$$

#### Gram-Schmidt process
Suppose $$x_1,x_2,...,x_p$$ is any basis for $$W$$. Then an orthogonal basis is given by $$v_1,v_2,...,v_p$$

$$\begin{align*}
& v_1=x_1,\\
& v_2=x_2-\frac{x_2\cdot v_1}{v_1 \cdot v_1}v_1,\\
& v_3=x_3-\frac{x_3\cdot v_1}{v_1 \cdot v_1}v_1-\frac{x_3\cdot v_2}{v_2 \cdot v_2}v_2,\\
& ......\\
& v_p=x_p-\frac{x_p\cdot v_1}{v_1 \cdot v_1}v_1-\cdots-\frac{x_p\cdot v_{p-1}}{v_{p-1} \cdot v_{p-1}}v_{p-1}.
\end{align*}$$

#### Least-squares solution
The set of least-squares solutions to $$Ax=b$$ is the set of exact solutions to the linear system

$$A^TAx=A^Tb.$$

#### Symmtric matrix
A symmetric matrix $$A$$ is orthogonally diagonalizable:

$$A=UDU^T,$$

where $$U$$ is an orthogonal matrix.

#### Sigular value decomposition (SVD)
1. Find an orthogonal diagonalization of $$A^T A.$$ Let the eigenvalues be in the decreasing order. Then $$v_1,v_2,...,v_n$$ is a list of orthonormal eigenvectors. 
2. For the eigenvalues we have $$\lambda_{r+1}=\lambda_{r+2}=\cdots=\lambda{n}=0.$$ Let $$\sigma_1=\sqrt{\lambda_1},\sigma_2=\sqrt{\lambda_2},...,\sigma_r=\sqrt{\lambda_r}.$$ They form the entries of the diagonal matrix $$D$$.
3. For each $$i=1,2,...,r$$, let $$u_i=\frac{1}{\sigma_i}Av_i.$$ Choose $$u_{r+1},u_{r+2},...,u_{m}$$ to form an orthonormal basis for $$\mathbb{R}^m$$.
4. Let $$U=[u_1\quad u_2\quad u_m], V=[v_1\quad v_2\quad v_n]$$ and 

$$\Sigma=\begin{bmatrix} D & 0 \\ 0 & 0
\end{bmatrix}.$$ 

Then we have the SVD of $$A$$:

$$A=U\Sigma V^T.$$


#### Persudo-inverse
If $$A=U\Sigma V^T$$, then $$A^+=V\Sigma^+ U^T.$$
