# Linear Algebra and Optimization: An Introduction

## Key Concepts

### 1. Linear Transformations and Systems

**Linear Transformation:**
\( f(ax + by) = af(x) + bf(y) \)

**Affine Transformation:**
\( f(ax + by) = af(x) + bf(y) + c \)

### 2. Geometry of Matrix Multiplication

**Matrix Multiplication:**
- Linear transformation: \( Ax \)

**Orthogonal Transformations:**
\( R = \begin{bmatrix} \cos(\theta) & -\sin(\theta) \\ \sin(\theta) & \cos(\theta) \end{bmatrix} \)

**Combining Orthogonal and Scaling Transformations:**
- Rotate \( D \) using \( V \).
- Scale \( DV \) using \( \Delta \).
- Rotate back using \( V^{-1} \).

### 3. Vector Spaces and Their Geometry

**Vector Space:**
- Closed under addition and scalar multiplication.

**Linear Independence:**
- No vector in the set can be written as a linear combination of the others.

**Basis:**
\( v = c_1 v_1 + c_2 v_2 + \dots + c_n v_n \)

**Span:**
- Set of all possible linear combinations of a set of vectors.

**Orthogonal Vector Spaces:**
\( u \cdot v = 0 \)

### 4. The Linear Algebra of Matrix Rows and Columns

**Four Fundamental Subspaces:**
1. **Column Space (Range):** Spanned by columns.
2. **Row Space:** Spanned by rows.
3. **Null Space:** \( Ax = 0 \).
4. **Left Null Space:** \( A^\top x = 0 \).

**Matrix Rank:**
\( \text{rank}(A) = \text{rank}(A^\top) \)

**Row Echelon Form:**
- Leading entry in each row is 1.
- Leading 1 in each row to the right of the one in the previous row.
- Zero rows at the bottom.

**LU Decomposition:**
\( A = LU \)

### 5. Matrix Rank and Its Properties

**Matrix Rank:**
- Maximum number of linearly independent column vectors.

**Effect of Matrix Operations on Rank:**
\( \text{rank}(A + B) \leq \text{rank}(A) + \text{rank}(B) \)
\( \text{rank}(A + B) \geq |\text{rank}(A) - \text{rank}(B)| \)
\( \text{rank}(AB) \leq \min(\text{rank}(A), \text{rank}(B)) \)
\( \text{rank}(AB) \geq \text{rank}(A) + \text{rank}(B) - d \)

### 6. Projections and Least Squares

**Orthogonal Projection:**
\( \text{proj}_u(y) = \frac{y \cdot u}{u \cdot u} u \)

**Least Squares Method:**
\( \sum_{i=1}^n (y_i - (mx_i + b))^2 \)

### 7. Gram-Schmidt and QR Decomposition

**Gram-Schmidt Orthogonalization:**
\( v_i' = v_i - \sum_{j=1}^{i-1} \text{proj}_{v_j}(v_i) \)

**QR Decomposition:**
\( A = QR \)

**Least Squares Solution using QR Decomposition:**
1. Compute \( A = QR \).
2. Solve \( R \hat{x} = Q^\top b \).
