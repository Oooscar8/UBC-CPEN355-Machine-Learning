[toc]



# Lecture Notes

This file mainly consists of my Lecture Notes of UBC CPEN355 Machine Learning with Engineering Applications.



# Lecture1

---

## Course Outline

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409080941585.png" alt="image-20240908094102405" style="zoom: 67%;" />

## Grade Structure

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409091414291.png" style="zoom:50%;" />



# Tutorial1

---

> Refer to [this](https://colab.research.google.com/drive/15Nfsx3JgpSYfIiBZnpREahHTFUZhYTBY?usp=sharing#scrollTo=tdvs4_zzcWrI)

The `colab` link above explains **what** is `colab`, **why** we use `colab`, how to read/process **text data, image data and tabular data** and how to **run on local machines**



# Lecture2

---

## Basics of Linear Algebra

### Vector Product

$ y = Ax $ can be written as **a linear combination** of the columns of A scaled by x

x is the scalar, and each column of A is a vector

Important to understand **attention** used in transformers!

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101555440.png" alt="image-20240910155503320" style="zoom: 67%;" />

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101556125.png" alt="image-20240910155602060" style="zoom: 67%;" />

### Linear Equations

General equations to solve x, as A may not be reversible

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101603709.png" alt="image-20240910160305630" style="zoom: 67%;" />

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101604452.jpg" alt="b83a4264e9d0535431115872046fc68" style="zoom: 33%;" />

### Vector Spaces

The addition of two vectors in a vector space result in a vector in the same vector space.

A vector in a vector space scaled by a scalar needs to be in the same vector space.

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101610189.png" alt="image-20240910161048127" style="zoom: 67%;" />

### Linear Independence and Rank

* Linear Independence

A set of vectors $ \{x_1, x_2, \dots, x_n\} \subset \mathbb{R}^m $

Linear Independent: no vector can be represented as a linear combination of the remaining vectors.

* Rank

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101619516.png" alt="image-20240910161910442" style="zoom: 67%;" />

The last line is the **Rank Theorem**

* Basic properties of the rank

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101625110.png" alt="image-20240910162522055" style="zoom: 67%;" />

### Span, Range and `Nullspace` of a Matrix

* Span

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101634852.png" alt="image-20240910163446783" style="zoom:67%;" />

* range and `nullspace`

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101641912.png" alt="image-20240910164121849" style="zoom:67%;" />

### Orthogonal and orthonormal

* orthogonal

Two vectors x, y are orthogonal if $x^Ty = 0$​

**orthonormal matrix = orthogonal matrix**

![image-20240910165125708](https://gitee.com/OooAlex/study_note/raw/master/img/202409101651761.png)

* Property of orthonormal matrix

![image-20240910165337613](https://gitee.com/OooAlex/study_note/raw/master/img/202409101653664.png)

### Determinant

Geometric meaning of determinant:

![image-20240910170612347](https://gitee.com/OooAlex/study_note/raw/master/img/202409101706423.png)

### Norms

A **norm** is a function that maps a vector into the a non-negative real number

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101722487.png" alt="image-20240910172219425" style="zoom:67%;" />

* L1 and L2 Norms

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101723364.png" alt="image-20240910172335291" style="zoom: 80%;" />

### Eigen values and eigen vectors

$Ax = {\lambda}x$​

$\lambda$ is the eigen value, x is the corresponding eigen vector

* Solve for eigen values

$ singular \ matrix \Leftrightarrow non-reversible \ matrix \Leftrightarrow det(matrix) = 0 $

![179a0d538ff5e46a4a467fdcb7f9407](https://gitee.com/OooAlex/study_note/raw/master/img/202409101750719.jpg)

* Eigen-Decomposition (ED)

Only apply to square matrix

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409101810098.jpg" alt="92b55b5573b38f17d21dcd973c46208" style="zoom: 50%;" />

* Singular Value Decomposition (SVD)

General form of ED



## Basics of Probability

### Random Variable

* Discrete Random Variable

e.g. dice number

* Continuous Random Variable

e.g. a person's height

### PMF and PDF

* PMF

For Discrete RVs

* PDF

For Continuous RVs

The value of PDF(f(x)) at a specific point represents the density of the probability around that point

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409111745453.jpg" alt="48c07a70bed73d6ff7297a5488b443d" style="zoom: 33%;" />

### Mean and Variance

* Mean

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409111755154.jpg" alt="09f2a126abfd561d4fc9ddebc615211" style="zoom: 33%;" />

* Variance

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409111756456.jpg" alt="d29d7c37a0c597fa273c75aa26631da" style="zoom:33%;" />

### Normal Distribution

PDF: f(x) = …:

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409111742849.png" alt="image-20240911174216708" style="zoom: 50%;" />

### Joint Probability Distribution

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409111806472.jpg" alt="a5edb7bbc4d994431873f1daad719da" style="zoom: 50%;" />

### Covariance

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409161759329.png" alt="image-20240916175926042" style="zoom: 50%;" />



# Lecture3

## Linear Regression

**Supervised** vs **Unsupervised** Learning

**Regression** vs **Classification**

**Gradient Descent**

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202409161834349.jpg" alt="de9556f66e4aec6aba178199d9280cf" style="zoom: 67%;" />

**Linear Regression**

**Minimizing Loss Function**

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202410081914345.jpg" alt="fade74f11354dbfc9b9d72b6b229698" style="zoom: 67%;" />

<img src="https://gitee.com/OooAlex/study_note/raw/master/img/202410081914785.png" alt="image-20241008191441718"  />

