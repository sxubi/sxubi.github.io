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


