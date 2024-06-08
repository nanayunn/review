# Linear Algebra and Optimization: An Introduction

## Key Concepts

### 1. Linear Transformations and Systems

**Linear Transformation:**
A function \( f(x) \) is a linear transformation if it satisfies the following properties for any vectors \( x, y \) and scalars \( a, b \):
\( f(ax + by) = af(x) + bf(y) \)

**Affine Transformation:**
A function \( f(x) \) is an affine transformation if it satisfies:
\( f(ax + by) = af(x) + bf(y) + c \)
where \( c \) is a constant vector.

### 2. Geometry of Matrix Multiplication

**Matrix Multiplication:**
Matrix multiplication can be seen as a series of linear transformations. If \( A \) is an \( n \times d \) matrix and \( x \) is a \( d \)-dimensional vector, the product \( Ax \) is a linear transformation.

**Orthogonal Transformations:**
An orthogonal transformation rotates vectors without changing their length. For a 2D rotation by angle \( \theta \):
\[
R = \begin{bmatrix} \cos(\theta) & -\sin(\theta) \\ \sin(\theta) & \cos(\theta) \end{bmatrix}
\]

**Combining Orthogonal and Scaling Transformations:**
To scale and rotate a data matrix \( D \):
1. Rotate \( D \) using an orthogonal matrix \( V \).
2. Scale the matrix \( DV \) using a diagonal matrix \( \Delta \).
3. Rotate back using \( V^{-1} \).

Example:
To scale each 2D row of \( D \) in the direction \( [\cos(-30^\circ), \sin(-30^\circ)] \) by a factor of 2, and in the direction \( [\cos(60^\circ), \sin(60^\circ)] \) by a factor of 0.5:
\( D' = (DV)\Delta V^{-1} \)

### 3. Vector Spaces and Their Geometry

**Vector Space:**
A vector space is a collection of vectors that is closed under addition and scalar multiplication.

**Linear Independence:**
A set of vectors \( \{v_1, v_2, \ldots, v_n\} \) is linearly independent if no vector in the set can be written as a linear combination of the others:
\( c_1 v_1 + c_2 v_2 + \ldots + c_n v_n = 0 \implies c_1 = c_2 = \ldots = c_n = 0 \)

**Basis:**
A basis of a vector space \( V \) is a set of linearly independent vectors that span the entire space. Any vector \( v \) in \( V \) can be expressed as a linear combination of the basis vectors:
\( v = c_1 v_1 + c_2 v_2 + \ldots + c_n v_n \)

**Span:**
The span of a set of vectors is the set of all possible linear combinations of those vectors.

**Orthogonal Vector Spaces:**
Two vector spaces \( U \) and \( W \) are orthogonal if the dot product of any vector from \( U \) with any vector from \( W \) is zero:
\( u \cdot w = 0 \quad \forall u \in U, w \in W \)

### 4. The Linear Algebra of Matrix Rows and Columns

**Four Fundamental Subspaces:**
1. **Column Space (Range):** The span of the columns of \( A \).
2. **Row Space:** The span of the rows of \( A \).
3. **Null Space:** The set of all solutions to \( Ax = 0 \).
4. **Left Null Space:** The set of all solutions to \( A^\top x = 0 \).

**Matrix Rank:**
The rank of a matrix is the dimension of its column space (or row space). It represents the maximum number of linearly independent columns (or rows) in the matrix:
\( \text{rank}(A) = \text{rank}(A^\top) \)

**Row Echelon Form:**
A matrix is in row echelon form if:
- The leftmost non-zero entry in each row is 1.
- The leading 1 in each row is to the right of the leading 1 in the previous row.
- All zero rows are at the bottom.

**LU Decomposition:**
LU decomposition factors a matrix \( A \) into a lower triangular matrix \( L \) and an upper triangular matrix \( U \):
\( A = LU \)

### 5. Matrix Rank and Its Properties

**Matrix Rank:**
The rank of a matrix \( A \) is the maximum number of linearly independent column vectors in \( A \).

**Effect of Matrix Operations on Rank:**
- Addition Upper Bound: 
\( \text{rank}(A + B) \leq \text{rank}(A) + \text{rank}(B) \)
- Addition Lower Bound: 
\( \text{rank}(A + B) \geq |\text{rank}(A) - \text{rank}(B)| \)
- Multiplication Upper Bound: 
\( \text{rank}(AB) \leq \min(\text{rank}(A), \text{rank}(B)) \)
- Multiplication Lower Bound: 
\( \text{rank}(AB) \geq \text{rank}(A) + \text{rank}(B) - d \)

### 6. Projections and Least Squares

**Orthogonal Projection:**
The orthogonal projection of a vector \( y \) onto a vector \( u \) is given by:
\( \text{proj}_u(y) = \frac{y \cdot u}{u \cdot u} u \)

**Least Squares Method:**
The least squares method finds the best fit line \( y = mx + b \) for data points \( (x_i, y_i) \) by minimizing the sum of the squares of the residuals:
\( \sum_{i=1}^n (y_i - (mx_i + b))^2 \)

### 7. Gram-Schmidt and QR Decomposition

**Gram-Schmidt Orthogonalization:**
The Gram-Schmidt process converts a set of vectors into an orthogonal set:
\( v_i' = v_i - \sum_{j=1}^{i-1} \text{proj}_{v_j}(v_i) \)

**QR Decomposition:**
QR decomposition factors a matrix \( A \) into an orthogonal matrix \( Q \) and an upper triangular matrix \( R \):
\( A = QR \)

**Least Squares Solution using QR Decomposition:**
1. Compute \( A = QR \).
2. Solve \( R \hat{x} = Q^\top b \).
