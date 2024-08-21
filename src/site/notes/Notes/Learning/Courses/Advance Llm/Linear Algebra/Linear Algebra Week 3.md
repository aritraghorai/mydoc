---
{"dg-publish":true,"permalink":"/notes/learning/courses/advance-llm/linear-algebra/linear-algebra-week-3/","title":"Linear Algebra - Vector & Linear transformations"}
---

# Vectors
**1. Vector**

A vector is an ordered list of numbers that represent a point in space. In machine learning and data science, vectors are often used to represent data points, features, or parameters. Vectors can be in various dimensions, depending on the number of elements they contain.

**Example of a 3D vector:**
```python
v = [1, 2, 3]
```

**Uses of Vectors:**
- **Feature Representation**: Vectors can represent features of a dataset.
- **Model Parameters**: In machine learning models, vectors can store the weights or coefficients.
- **Embeddings**: Vectors are used to represent words or other entities in a continuous vector space.

---

**2. Properties of Vectors**

Vectors have several key properties that are essential in machine learning and data science:

- **Magnitude**: The length or size of the vector, calculated using the Euclidean norm.
  $$
  \text{Magnitude} = \sqrt{x_1^2 + x_2^2 + \ldots + x_n^2}
  $$
  
- **Direction**: The orientation of the vector in space, relative to the origin.

- **Dot Product**: A scalar product of two vectors, representing their cosine similarity.
  $$
  \text{Dot Product} = \sum_{i=1}^n x_i \cdot y_i
  $$
  
- **Cross Product**: A vector that is perpendicular to two other vectors (only in 3D space).

- **Addition and Subtraction**: Vectors can be added or subtracted to form new vectors.
  
  $$
  v_3 = v_1 + v_2 = [x_1 + x_2, y_1 + y_2, z_1 + z_2]
  $$
  
- **Scalar Multiplication**: Multiplying a vector by a scalar changes its magnitude but not its direction.

## Vector Operations

**1. Vector Addition**

Vector addition involves adding corresponding elements of two vectors to produce a new vector. 

**Example:**
Given two vectors:
$$
\mathbf{v_1} = [x_1, y_1, z_1]
$$
$$
\mathbf{v_2} = [x_2, y_2, z_2]
$$
The sum is:
$$
\mathbf{v_3} = \mathbf{v_1} + \mathbf{v_2} = [x_1 + x_2, y_1 + y_2, z_1 + z_2]
$$

---

**2. Vector Subtraction**

Similar to addition, vector subtraction involves subtracting corresponding elements of one vector from another.

**Example:**
Given two vectors:
$$
\mathbf{v_1} = [x_1, y_1, z_1]
$$
$$
\mathbf{v_2} = [x_2, y_2, z_2]
$$
The difference is:
$$
\mathbf{v_3} = \mathbf{v_1} - \mathbf{v_2} = [x_1 - x_2, y_1 - y_2, z_1 - z_2]
$$

---

**3. Scalar Multiplication**

Scalar multiplication involves multiplying each element of a vector by a scalar (a single number). This operation changes the magnitude of the vector but not its direction (unless the scalar is negative, which reverses the direction).

**Example:**
Given a vector:
$$
\mathbf{v} = [x, y, z]
$$
And a scalar \( c \):
$$
c \cdot \mathbf{v} = [c \cdot x, c \cdot y, c \cdot z]
$$

---

**4. Dot Product (Scalar Product)**

The dot product is an operation that takes two vectors and returns a scalar. It's a measure of how similar the two vectors are, with applications in calculating projections, angles, and more.

**Example:**
Given two vectors:
$$
\mathbf{v_1} = [x_1, y_1, z_1]
$$
$$
\mathbf{v_2} = [x_2, y_2, z_2]
$$
The dot product is:
$$
\mathbf{v_1} \cdot \mathbf{v_2} = x_1 \cdot x_2 + y_1 \cdot y_2 + z_1 \cdot z_2
$$

**Interpretation:**
- If the dot product is positive, the vectors point in roughly the same direction.
- If it's negative, they point in opposite directions.
- If it's zero, the vectors are orthogonal (perpendicular).

---

**5. Cross Product**

The cross product is an operation defined only in three-dimensional space that takes two vectors and returns a third vector that is perpendicular to both. It’s widely used in physics and engineering.

**Example:**
Given two vectors:
$$
\mathbf{v_1} = [x_1, y_1, z_1]
$$
$$
\mathbf{v_2} = [x_2, y_2, z_2]
$$
The cross product is:
$$
\mathbf{v_1} \times \mathbf{v_2} = [y_1 \cdot z_2 - z_1 \cdot y_2, z_1 \cdot x_2 - x_1 \cdot z_2, x_1 \cdot y_2 - y_1 \cdot x_2]
$$

The resulting vector is perpendicular to both \( \mathbf{v_1} \) and \( \mathbf{v_2} \).

---

**6. Vector Norm (Magnitude)**

The norm or magnitude of a vector is a measure of its length. For an n-dimensional vector, the magnitude is calculated as follows:

$$
||\mathbf{v}|| = \sqrt{x_1^2 + x_2^2 + \ldots + x_n^2}
$$

**Example:**
For a vector \( \mathbf{v} = [3, 4] \):
$$
||\mathbf{v}|| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5
$$

---

**7. Unit Vector**

A unit vector has a magnitude of 1 and points in the same direction as the original vector. It is obtained by dividing the vector by its magnitude.

**Example:**
For a vector  *v* :
$$
\mathbf{\hat{v}} = \frac{\mathbf{v}}{||\mathbf{v}||} \
$$


# Linear transformations

## Matrix to linear transformation
![Linear Algebra Week 3 Linear Transformation.png](/img/user/assets/Linear%20Algebra%20Week%203%20Linear%20Transformation.png)
## Linear transformation to matrix
![Linear Algebra Week 3 Linear Transformation to matrix.png](/img/user/assets/Linear%20Algebra%20Week%203%20Linear%20Transformation%20to%20matrix.png)
## Matrix Multiplication
![Linear Algebra Week 3 Matrix Multipication.png](/img/user/assets/Linear%20Algebra%20Week%203%20Matrix%20Multipication.png)

![Linear Algebra Week 3 Dimention After multipication.png](/img/user/assets/Linear%20Algebra%20Week%203%20Dimention%20After%20multipication.png)


## Identity matrix

An identity matrix is a square matrix where all the elements on the main diagonal (from the top left to the bottom right) are equal to 1, and all off-diagonal elements are 0. In other words, it's a matrix that doesn't change a vector when you multiply the vector by the matrix.

For example, a 3x3 identity matrix looks like this:

$$
I_3 = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$


