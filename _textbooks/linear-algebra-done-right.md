---
layout: post
title: "Exercises: Linear Algebra Done Right"
subject: "Mathematics"
---

## Chapter 1: Vector Spaces

### Exercise 1.A.1
Show that \\(\alpha + \beta = \beta + \alpha\\) for all \\(\alpha, \beta \in \mathbb{C}\\).

### Solution:
$$
\begin{align}
\alpha + \beta &= (a + bi) + (c + di) && \text{ where } a, b, c, d \in \mathbb{R} \\
                &= (a + c) + (b + d)i && \text{ by definition of addition on } \mathbb{C} \\
                &= (c + a) + (d + b)i && \text{ commutativity of addition on } \mathbb{R} \\
                &= (c + di) + (a + bi) && \text{ by definiton of addition on } \mathbb{C} \\
                &= \beta + \alpha
\end{align}
$$

### Exercise 1.A.2
Show that \\((\alpha + \beta) + \lambda = \alpha + (\beta + \lambda)\\) for all \\(\alpha, \beta, \lambda \in \mathbb{C}\\).

### Solution:
$$
\begin{align}
(\alpha + \beta) + \lambda &= ((a + bi) + (c + di)) + e + fi && \text{ where } a, b, c, d, e, f \in \mathbb{R} \\
                            &= ((a + c) + (b + d)i) + e + fi && \text{ by definition of addition on } \mathbb{C} \\
                            &= ((a + c) + e) + ((b + d) + f)i && \text{ by definition of addition on } \mathbb{C} \\
                            &= (a + (c + e)) + (b + (d + f))i && \text{ associativity of addition on } \mathbb{R} \\
                            &= a + bi + ((c + e) + (d + f)i) && \text{ by definition of addition on } \mathbb{C} \\
                            &= a + bi + (c + di + e + fi) && \text{ by definition of addition on } \mathbb{C} \\
                            &= \alpha + (\beta + \lambda)
\end{align}
$$

### Exercise 1.A.3
Show that \\((\alpha\beta)\lambda = \alpha(\beta\lambda)\\) for all \\(\alpha, \beta, \lambda \in \mathbb{C}\\).

### Solution:
$$
\begin{align}
(\alpha\beta)\lambda &= ((a + bi)(c + di))(e + fi) \\
                        &= ((ac - bd) + (ad + bc)i)(e + fi) && \text{ by definition of multiplication on } \mathbb{C} \\
                        &= ((ac - bd)e - (ad + bc)f) + ((ac - bd)f + (ad + bc)e)i && \text{ by definition of multiplication on } \mathbb{C} \\
                        &= (ace - bde - adf - bcf) + (acf - bdf + ade + bce)i && \text{ distributive property of } \mathbb{R} \\
                        &= (a(ce - df) - b(cf + de)) + (a(cf + de) + b(ce - df))i && \text{ distributive property of } \mathbb{R} \\
                        &= (a + bi)((ce - df) + (cf + de)i) && \text{ by definition of multiplication on } \mathbb{C} \\
                        &= (a + bi)((c + di)(e + fi)) && \text{ by definition of multiplication on } \mathbb{C} \\
                        &= \alpha(\beta\lambda)
\end{align}
$$

### Exercise 1.A.4
Show that \\(\lambda(\alpha + \beta) = \lambda\alpha + \lambda\beta\\) for all \\(\lambda, \alpha, \beta \in \mathbb{C}\\).

### Solution:
$$
\begin{align}
\lambda(\alpha + \beta) &= (e + fi)((a + bi) + (c + di)) \\
                        &= (e + fi)((a + c) + (b + d)i) && \text{ by definition of addition on } \mathbb{C} \\
                        &= (e(a + c) - f(b + d)) + (e(b + d) + f(a + c))i && \text{ by definition of multiplication on } \mathbb{C} \\
                        &= (ea + ec - fb - fd) + (eb + ed + fa + fc)i && \text{ distributive property of } \mathbb{R} \\
                        &= (ea - fb) + (eb + fa)i + (ec - fd) + (ed + fc)i && \text{ commutativity of addition on } \mathbb{C} \\
                        &= (e + fi)(a + bi) + (e + fi)(c + di) && \text{ by definition of multiplication on } \mathbb{C} \\
                        &= \lambda\alpha + \lambda\beta
\end{align}
$$

### Exercise 1.A.5
Show that for every \\(\alpha \in \mathbb{C}\\), there exists a unique \\(\beta \in \mathbb{C}\\) such that \\(\alpha + \beta = 0\\).

### Solution:
Assume that for some \\(\alpha \in \mathbb{C}\\), there exists \\(\beta, \lambda \in \mathbb{C}\\) such that \\(\alpha + \beta = 0\\) and \\(\alpha + \lambda = 0\\).
<br><br>
$$
\begin{align}
\alpha + \beta &= \alpha + \lambda \\
(a + bi) + (c + di) &= (a + bi) + (e + fi) \\
(a + c) + (b + d)i &= (a + e) + (b + f)i && \text{ by definition of addition on } \mathbb{C} \\
\end{align}
$$

We end up with the following equalities:
<br><br>
$$
\begin{align}
a + c &= a + e \\
a + c + -a &= a + e + -a \\
c &= e && \text{ additive inverse on } \mathbb{R}
\end{align}
$$
<br><br>
$$
\begin{align}
b + d &= b + f \\
b + d + -b &= b + f + -b \\
d &= f && \text{ additive inverse on } \mathbb{R}
\end{align}
$$

Hence,
<br><br>
$$
\begin{align}
\beta &= c + di \\
        &= e + fi \\
        &= \lambda
\end{align}
$$

and this contradicts the original assumption that for some \\(\alpha \in \mathbb{C}\\), there exists \\(\beta, \lambda \in \mathbb{C}\\) such that \\(\alpha + \beta = 0\\) and \\(\alpha + \lambda = 0\\).

### Exercise 1.A.6
Show that for every \\(\alpha \in \mathbb{C}\\) with \\(\alpha \neq 0\\), there exists a unique \\(\beta \in \mathbb{C}\\) such that \\(\alpha\beta = 1\\).

### Solution:
Assume that for some \\(\alpha \in \mathbb{C}\\), where \\(\alpha \neq 0\\), there exists \\(\beta, \lambda \in \mathbb{C}\\) such that \\(\alpha\beta = 1\\) and \\(\alpha\lambda = 1\\).
<br><br>
$$
\begin{align}
\alpha\beta &= \alpha\lambda \\
(a + bi)(c + di) &= (a + bi)(e + fi) \\
(ac - bd) + (ad + bc)i &= (ae - bf) + (af + be)i && \text{ by definition of multiplication on } \mathbb{C}
\end{align}
$$

We end up with the following equalities:
<br><br>
$$
\begin{align}
(ac - bd) &= (ae - bf) \\
ac - ae &= bd - bf && \text{ additive inverse on } \mathbb{R} \\
a(c - e) &= b(d - f) && \text{ distributive property of } \mathbb{R} \\
\frac{a}{b} &= \frac{d - f}{c - e} 
\end{align}
$$
<br><br>
$$
\begin{align}
(ad + bc) &= (af + be) \\
ad - af &= be - bc && \text{ additive inverse on } \mathbb{R} \\
a(d - f) &= b(e - c) && \text { distributive property of } \mathbb{R} \\
\frac{a}{b} &= \frac{e - c}{d - f}
\end{align}
$$

Hence,
<br><br>
$$
\begin{align}
\frac{d - f}{c - e} &= \frac{e - c}{d - f} \\
(d - f)(d - f)
\end{align}
$$

### Exercise 1.A.7
Show that \\(\frac{-1 + \sqrt{3}i}{2}\\) is a cube root of 1 (meaning that its cube equals 1).

### Solution:
$$
\begin{align}
(\frac{-1 + \sqrt{3}i}{2})^3 &= (\frac{-1 + \sqrt{3}i}{2})(\frac{-1 + \sqrt{3}i}{2})(\frac{-1 + \sqrt{3}i}{2}) \\
                                &= \frac{(-1 + \sqrt{3}i)(-1 + \sqrt{3}i)(-1 + \sqrt{3}i)}{8} \\
                                &= \frac{(1 - 2\sqrt{3}i - 3)(-1 + \sqrt{3}i)}{8} \\
                                &= \frac{(-2 - 2\sqrt{3}i)(-1 + \sqrt{3}i)}{8} \\
                                &= \frac{2 + 6}{8} \\
                                &= 1
\end{align}
$$

### Exercise 1.A.8
Find two distinct square roots of \\(i\\).

### Solution:
$$
\begin{align}
i &= (a + bi)^2 \\
    &= (a + bi)(a + bi) \\
    &= (a^2 - b^2) + (ab + ba)i && \text{ by definition of multiplication on } \mathbb{C}
\end{align}
$$

Hence,
<br><br>
$$
\begin{align}
a^2 - b^2 &= 0 \\
ab + ba &= 1
\end{align}
$$
<br><br>
$$
$$

### Exercise 1.A.9
Find \\(x \in \mathbb{R}^4\\) such that
<br><br>
$$(4,-3,1,7) + 2x = (5,9,-6,8)$$.

### Solution:
$$
\begin{align}
(4,-3,1,7) + 2x &= (5,9,-6,8) \\
2x &= (5,9,-6,8) + (-4,3,-1,-7) && \text{ additive inverse in } \mathbb{R}^n \\
2x &= (1,12,-7,1) \\
x &= \frac{1}{2}(1,12,-7,1) && \text{ multiplicative inverse in } \mathbb{R} \\
    &= (\frac{1}{2},6,\frac{-7}{2},\frac{1}{2})
\end{align}
$$

## Chapter 2: Finite-Dimensional Vector Spaces

### Exercise 2.A.1
Find a list of four distinct vectors in \\(\mathbb{F}^3\\) whose span equals
$$
\{(x, y, z) \in \mathbb{F}^3 : x + y + z = 0\}
$$.

### Solution: