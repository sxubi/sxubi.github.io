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
Suppose $$A$$ is an $$m\times n$$ matrix. The span of columns of $$A$$ is $$\mathrm{R}^m$$ if and only if $$A$$ has a pivot position in every row.

#### Invertible matrix
A matrix $$A$$ is invertible if and only if $$\det(A)=0.$$ To compute $$A^{-1}$$, we have

$$RREF(\[A\quad I_n\])=\[I_n\quad A^{-1}\].$$

#### Basis of $$Col A$$ and $$Nul A$$


