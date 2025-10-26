# Chapter 2 – Solving Linear Equations

This chapter focuses on systematic methods for solving **linear systems**, **matrix operations**, **inverses**, and **factorization techniques**. The main theme: how **elimination** and **matrix structure** make **solving equations** efficient.

---

### 2.1 Vectors and Linear Equations

- A system of linear equations can be written compactly using vectors and matrices.  
- Example:
  
  $$\begin{cases}
  2x + y = 5 \\
  x - y = 1
  \end{cases}$$
  
  becomes
  
  $$A \mathbf{x} = \mathbf{b}, \quad 
  A = \begin{bmatrix} 2 & 1 \\ 1 & -1 \end{bmatrix}, \quad 
  \mathbf{x} = \begin{bmatrix} x \\ y \end{bmatrix}, \quad
  \mathbf{b} = \begin{bmatrix} 5 \\ 1 \end{bmatrix}$$
- Key insight: Solving equations = finding a vector $\mathbf{x}$ in $\mathbb{R}^n$ such that $A\mathbf{x} = \mathbf{b}$.  
- Multiple perspectives:  
	- **Row picture**: Intersections of lines/planes.  
	- **Column picture**: Linear combination of columns of $A$ equals $\mathbf{b}$.

---

### 2.2 The Idea of Elimination

- **Elimination** systematically removes variables from equations to simplify the system.  
- Example (2 equations, 2 unknowns):  
	- Subtract multiples of one equation from another to eliminate a variable.  
- Leads to a **triangular system** that can be solved by back substitution.  
- Problems may arise:  
	- **No solution** (inconsistent system).  
	- **Many solutions** (underdetermined system).  
- This motivates using **matrices and elimination matrices** to formalize the process.

---

### 2.3 Elimination Using Matrices

- **Gaussian elimination** can be expressed with **elimination matrices**.  
- An elimination matrix $E$ applies a row operation:$$
  E A = A'
  $$
  where $A'$ is the matrix after one elimination step.  

- Successive elimination:
  
  $$E_k \cdots E_2 E_1 A = U$$
  
  where $U$ is upper triangular.  

- Connects elimination directly with matrix multiplication.

---

### 2.4 Rules for Matrix Operation

- **Matrix Addition & Scalar Multiplication**: Entry-wise operations.  
- **Matrix Multiplication**: Row-by-column combination.  
	- Associative: $(AB)C = A(BC)$  
	- Distributive: $A(B+C) = AB + AC$  
	- Not commutative: $AB \neq BA$ in general.  

- **Identity Matrix ($I$)**: $IA = AI = A$  
- **Zero Matrix ($0$)**: $A + 0 = A$  

---

### 2.5 Inverse Matrices

- A matrix $A$ is invertible if there exists $A^{-1}$ such that:
  
  $$AA^{-1} = A^{-1}A = I$$

- Conditions:  
	- Square matrix.  
	- Nonzero determinant.  
- Computing inverses: Solve $AX = I$ by elimination → $X = A^{-1}$.  
- **Singular matrices** (no inverse) occur when equations are dependent.

---

### 2.6 Factorization $A = LU$

- Any invertible matrix $A$ can be factored as:

$$A = LU$$

	- $L$: lower triangular (multipliers from elimination).  
	- $U$: upper triangular (result of elimination).  

- Solving $A\mathbf{x} = \mathbf{b}$ becomes efficient:  
	1. $L\mathbf{y} = \mathbf{b}$ (forward substitution).  
	2. $U\mathbf{x} = \mathbf{y}$ (back substitution).

---

### 2.7 Transposes and Permutation

- **Transpose ($A^T$)**: Rows become columns.  
	- $(A^T)_{ij} = A_{ji}$  
	- $(AB)^T = B^T A^T$  
	- $(A^T)^T = A$  

- **Symmetric Matrix**: $A = A^T$  
- **Permutation Matrices**:  
	- Swap rows or reorder equations.  
	- Derived from the identity by row exchanges.  
	- Used for pivoting in elimination (avoiding division by zero).
