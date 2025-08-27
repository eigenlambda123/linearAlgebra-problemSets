# Chapter 3 – Vector Spaces and Subspaces

This chapter develops the idea of **vector spaces** and their **subspaces**, introducing the **nullspace**, **basis**, and **dimension**. These concepts unify the structure of solutions to linear equations.

---

### 3.1 Space of Vectors

- A **vector space** is a set of vectors closed under **addition** and **scalar multiplication**.  
- Examples:  
	- $\mathbb{R}^n$ = all $n$-dimensional vectors.  
	- Subspaces: lines/planes through the origin.  

- **Subspace criteria**:  
	1. Contains the zero vector.  
	2. Closed under addition.  
	3. Closed under scalar multiplication.  

---

### 3.2 The Nullspace of $A$

- **Nullspace ($N(A)$)**: The set of all solutions to $A\mathbf{x} = 0$.  
  $$
  N(A) = \{ \mathbf{x} \in \mathbb{R}^n : A\mathbf{x} = 0 \}
  $$
- Always a subspace of $\mathbb{R}^n$.  
- Finding $N(A)$: Solve the homogeneous system $Ax=0$ using elimination.  
- Dimension of $N(A)$ = **number of free variables**.  

---

### 3.3 The Complete Solution to $A\mathbf{x} = \mathbf{b}$

- General solution = **particular solution** + **nullspace solution**.  
  $$
  \mathbf{x} = \mathbf{x}_p + \mathbf{x}_n
  $$
	- $\mathbf{x}_p$: a particular solution of $A\mathbf{x} = \mathbf{b}$.  
	- $\mathbf{x}_n$: any solution in the nullspace of $A$.  

- Key idea: The nullspace describes the **freedom in solutions**.  

---

### 3.4 Independence, Basis, and Dimension

- **Linear Independence**: Vectors $\mathbf{v}_1, \dots, \mathbf{v}_k$ are independent if:
  $$
  c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \cdots + c_k \mathbf{v}_k = 0
  $$
  implies all $c_i = 0$.  

- **Basis**: A set of independent vectors that span the space.  
- **Dimension**: The number of vectors in any basis for the space.  
	- Dimension is well-defined (all bases have the same size).  

---

### 3.5 Dimensions of Four Subspaces

Every matrix $A$ defines **four fundamental subspaces**:

1. **Column space ($C(A)$)**: Span of columns, subspace of $\mathbb{R}^m$.  
2. **Nullspace ($N(A)$)**: Solutions to $A\mathbf{x} = 0$, subspace of $\mathbb{R}^n$.  
3. **Row space ($C(A^T)$)**: Span of rows, subspace of $\mathbb{R}^n$.  
4. **Left nullspace ($N(A^T)$)**: Solutions to $A^T\mathbf{y} = 0$, subspace of $\mathbb{R}^m$.

- **Rank-Nullity Theorem**  $$
  \text{rank}(A) + \text{nullity}(A) = n
  $$
  where $n$ = number of columns of $A$.  
