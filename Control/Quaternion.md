# Quaternion

## Complex Analysis

### Matrix Representation of Complex number $\C$

* $z = a + bi \iff $ $z = \begin{bmatrix}\ a\\b \end{bmatrix}$  **vector representation** ---> Complex Plane etc.

  * $z_1+z_2 = (a_1+a_2) + (b_1+b_2)i \implies z=\begin{bmatrix}a_1+a_2\\b_1+b_2\end{bmatrix}$	

* $z=a+bi \iff \begin{bmatrix}a & -b \\ b & a \end{bmatrix}$ **Matrix Representation**

  * $z_1+z_2 = \begin{bmatrix}a_1 & -b_1 \\ b_1 & a_1 \end{bmatrix} + \begin{bmatrix}a_2 & -b_2 \\ b_2 & a_2 \end{bmatrix} = \begin{bmatrix}a_1+a_2 & -(b_1+b_2) \\ b_1+b_2 & a_1+a_2 \end{bmatrix} = (a_1+a_2)+(b_1+b_2)i$

  * $z_1\cdot z_2 = \begin{bmatrix}a_1 & -b_1 \\ b_1 & a_1 \end{bmatrix} \begin{bmatrix}a_2 & -b_2 \\ b_2 & a_2 \end{bmatrix}$ = 

    $\begin{bmatrix}a_1a_2-b_1b_2 & -(a_1b_2+b_1a_2) \\ a_1b_2+b_1a_2 & a_1a_2-b_1b_2 \end{bmatrix} \iff (a_1a_2-b_1b_2) + (a_1b_2+b_1a_2)i$

* $i = \begin{bmatrix}0 & -1 \\ 1 & 0 \end{bmatrix}$ obviously~~  $i^2 = \begin{bmatrix}-1 & 0 \\ 0 & -1 \end{bmatrix} = -I$

### $L_2$ Norm and Conjugate

*  $z=a+bi \implies \bar{z} = a+(-b)i$
* $z\cdot \bar{z} = (\|z\|_2)^2 \iff \|z\|_2 = \sqrt{z\cdot \bar{z}}$

### Complex Multiplication and 2-Dimensional Rotation

* $z=a+bi = \begin{bmatrix} a & -b \\ b & a\end{bmatrix} = \sqrt{a^2+b^2} \begin{bmatrix} \frac{a}{ \sqrt{a^2+b^2}} & \frac{-b}{ \sqrt{a^2+b^2}} \\ \frac{b}{ \sqrt{a^2+b^2}} & \frac{a}{ \sqrt{a^2+b^2}}\end{bmatrix} =  \sqrt{a^2+b^2} \begin{bmatrix}cos(\theta) & -sin(\theta) \\ sin(\theta) & cos(\theta)\end{bmatrix}$

  * ![](C:\Users\zhang\Documents\GitHub\QuadCopter-Math\Control\Markdown Imgs\Quaternion_complex_trig.PNG)

* $\sqrt{a^2+b^2} \begin{bmatrix}cos(\theta) & -sin(\theta) \\ sin(\theta) & cos(\theta)\end{bmatrix} = \|z\|\cdot I \begin{bmatrix}cos(\theta) & -sin(\theta) \\ sin(\theta) & cos(\theta)\end{bmatrix} = \begin{bmatrix}\|z\| & 0 \\ 0&\|z\| \end{bmatrix}\begin{bmatrix}cos(\theta) & -sin(\theta) \\ sin(\theta) & cos(\theta)\end{bmatrix}$

* $ \begin{bmatrix}\|z\| & 0 \\ 0&\|z\| \end{bmatrix}$  is **scaling matrix**

* $\begin{bmatrix}cos(\theta) & -sin(\theta) \\ sin(\theta) & cos(\theta)\end{bmatrix}$ is **rotation matrix**

* Revisit the matrix representation of complex number, $z = \begin{bmatrix}a & -b \\ b & a \end{bmatrix}$ is an **orthogonal matrix(orthonormal set of columns)** iff $\|z\|=1$. In general the column vectors of $\begin{bmatrix}a & -b \\ b & a \end{bmatrix}$ form a **orthogonal basis**, i.e. an orthogonal coordinate axes.

* And a complex matrix multiply by another complex matrix is simply the [**Rotation & Scaling**] of a coordinate axes in complex plane.

*  $\begin{bmatrix}cos(\theta) & -sin(\theta) \\ sin(\theta) & cos(\theta)\end{bmatrix} = cos(\theta) +i\ sin(\theta)$

* define $z$ as a rotational matrix, $z =cos(\theta) +i\ sin(\theta)$,

   $v' = zv = (cos(\theta) +i\ sin(\theta))v$ where we get $v'$ by rotate $v$ **counterclockwise** $\theta$ degrees.

### Complex Number in Polar Coordinates

