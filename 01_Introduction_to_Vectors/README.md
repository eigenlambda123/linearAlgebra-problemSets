# Chapter 1 – Introduction to Vectors

This chapter introduces the fundamental building blocks of linear algebra: **vectors**, **dot products**, and **matrices**. These ideas form the foundation for everything else in the subject.

---

### 1.1 Vectors and Linear Combination

- A **vector** is an ordered list of numbers (components) that can represent direction, magnitude, or abstract quantities.  
  - Example:  
    - In 2D: $\mathbf{v} = (v_1, v_2)$  
    - In 3D: $\mathbf{v} = (v_1, v_2, v_3)$
- **Linear Combination**: A weighted sum of vectors using scalar coefficients.  

- **Span**: The set of all possible linear combinations of given vectors.  
- Key Idea: Linear algebra studies what vectors can be built from combinations of other vectors.

---

### 1.2 Lengths and Dot Product

- **Length (Norm)** of a vector $\mathbf{v} = (v_1, v_2, \dots, v_n)$:
  $$\|\mathbf{v}\| = \sqrt{v_1^2 + v_2^2 + \cdots + v_n^2}$$
  
- **Dot Product**: For vectors $\mathbf{u}, \mathbf{v} \in \mathbb{R}^n$,
  $$\mathbf{u} \cdot \mathbf{v} = u_1v_1 + u_2v_2 + \cdots + u_nv_n$$
  
- Connection:  
  $$\mathbf{u} \cdot \mathbf{v} = \|\mathbf{u}\| \|\mathbf{v}\| \cos \theta$$
  
  where $\theta$ is the angle between them.

- Applications:  
	- Checking **orthogonality** ($\mathbf{u} \cdot \mathbf{v} = 0$).  
	- Measuring projection of one vector onto another.

---

### 1.3 Matrices

- A **matrix** is a rectangular array of numbers, written in rows and columns.  
- A matrix represents a **linear transformation** from vectors to vectors.  
- **Columns of $A$** show how basis vectors are transformed.

