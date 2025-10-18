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
a(c - e) &= b(d - f) && \text{ distributive property of } \mathbb{R}
\end{align}
$$
<br><br>
$$
\begin{align}
(ad + bc) &= (af + be) \\
ad - af &= be - bc && \text{ additive inverse on } \mathbb{R} \\
a(d - f) &= b(e - c) && \text { distributive property of } \mathbb{R} \\
a(d - f) &= -b(c - e) && \text{ multiplicative inverse on } \mathbb{R} \text { and } (-1)(-1) = 1
\end{align}
$$

Multiplying \\(a\\) and \\(b\\) to both equations,
<br><br>
$$
\begin{align}
a^2(c - e) &= ab(d - f) \\
ab(d - f) &= -b^2(c - e) 
\end{align}
$$

Combining the equations,
<br><br>
$$
\begin{align}
a^2(c - e) &= -b^2(c - e) \\
a^2(c - e) + b^2(c - e) &= 0 && \text{ additive inverse on } \mathbb{R} \\
(a^2 + b^2)(c - e) &= 0 && \text{ distributive property on } \mathbb{R}
\end{align}
$$

Since we know that \\(\alpha \neq 0\\), we know that at least \\(a\\) or \\(b\\) will be non-zero, and \\(a^2 + b^2 \neq 0\\). This would mean that \\(c - e = 0\\).

Multiplying \\(a\\) and \\(b\\) to both equations again,
<br><br>
$$
\begin{align}
ab(c - e) &= b^2(d - f) \\
a^2(d - f) &= -ab(c - e) 
\end{align}
$$

Combining the equations,
<br><br>
$$
\begin{align}
a^2(d - f) + b^2(d - f) &= 0 \\
(a^2 + b^2)(d - f) &= 0 && \text{ distributive property on } \mathbb{R}
\end{align}
$$

Since we know that \\(\alpha \neq 0\\), we know that at least \\(a\\) or \\(b\\) will be non-zero, and \\(a^2 + b^2 \neq 0\\). This would mean that \\(d - f = 0\\).

This would mean that \\(c = e\\) and \\(d = f\\), which implies that \\(\alpha = \lambda\\), which contradicts the original assumption that for some \\(\alpha \in \mathbb{C}\\), where \\(\alpha \neq 0\\), there exists \\(\beta, \lambda \in \mathbb{C}\\) such that \\(\alpha\beta = 1\\) and \\(\alpha\lambda = 1\\).

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

Knowing that \\(b \neq 0\\),
<br><br>
$$
\begin{align}
ab + ba &= 1 \\
2ab &= 1 \\
a &= \frac{1}{2b} 
\end{align}
$$

Substituting into the other equation,
<br><br>
$$
\begin{align}
a^2 - b^2 &= 0 \\
\frac{1}{(2b)^2} - b^2 &= 0 \\
\frac{1}{4} - b^4 &= 0 \\
b &= \pm\frac{1}{\sqrt{2}}
\end{align}
$$

Solving for \\(a\\),
<br><br>
$$
\begin{align}
a &= \pm\frac{1}{2(\frac{1}{\sqrt{2}})} \\
a &= \pm\frac{\sqrt{2}}{2}
\end{align}
$$

Hence,
<br><br>
$$
\begin{align}
i &= \frac{\sqrt{2}}{2} + \frac{1}{\sqrt{2}}i \\
    &= -\frac{\sqrt{2}}{2} - \frac{1}{\sqrt{2}}i
\end{align}
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

### Exercise 1.A.10
Explain why there does not exist \\(\lambda \in \mathbb{C}\\) such that
<br><br>
$$
\lambda(2 - 3i, 5 + 4i, -6 + 7i) = (12 - 5i, 7 + 22i, -32 - 9i)
$$.

### Solution
Assume that there exists some \\(\lambda \in \mathbb{C}\\) such that \\(\lambda(2 - 3i, 5 + 4i, -6 + 7i) = (12 - 5i, 7 + 22i, -32 - 9i)\\).
<br><br>
$$
\begin{align}
\lambda(2 - 3i) &= 12 - 51\\
(a + bi)(2 - 3) &= 12 - 5i \\
(2a + 3b) + (-3a + 2b)i &= 12 - 5i 
\end{align}
$$

Resulting in,
<br><br>
$$
\begin{align}
2a + 3b &= 12 \\
-3a + 2b &= -5
\end{align}
$$

Solving the equations,
<br><br>
$$
\begin{align}
a &= 6 - \frac{3b}{2} \\
-3(\frac{3b}{2}) + 2b &= -5 \\
-9b + 4b &= -10 \\
b &= 2 \\
a &= 6 - \frac{(3)(2)}{2} \\
    &= 3
\end{align}
$$

Checking the values for the third dimension,
<br><br>
$$
\begin{align}
\lambda(-6 + 7i) &= (a + bi)(-6 + 7i) \\
                    &= (3 + 2i)(-6 + 7i) \\
                    &= (-18 - 14) + (21 - 12)i \\
                    &= -32 + 9i \\
                    &\neq -32 - 9i
\end{align}
$$

Hence, this contradicts the original assumption that there exists some \\(\lambda \in \mathbb{C}\\) such that \\(\lambda(2 - 3i, 5 + 4i, -6 + 7i) = (12 - 5i, 7 + 22i, -32 - 9i)\\).

### Exercise 1.A.11
Show that \\((x + y) + z = x + (y + z)\\) for all \\(x, y, z \in \mathbb{F}^n\\).

### Solution
$$
\begin{align}
(x + y) + z &= ((x_1, \ldots, x_n) + (y_1, \ldots, y_n)) + (z_1, \ldots, z_n) && \\
            &= (x_1 + y_1, \ldots, x_n + y_n) + (z_1, \ldots, z_n) && \\
            &= ((x_1 + y_1) + z_1, \ldots, (x_n + y_n) + z_n) && \\
            &= (x_1 + (y_1 + z_1), \ldots, x_n + (y_n + z_n)) && \text{ associativity of addition on } \mathbb{F} \\
            &= (x_1, \ldots, x_n) + (y_1 + z_1, \ldots, y_n + z_n) && \\
            &= (x_1, \ldots, x_n) + ((y_1, \ldots, y_n) + (z_1, \ldots, z_n)) && \\
            &= x + (y + z)
\end{align}
$$

### Exercise 1.A.12
Show that \\((ab)x = a(bx)\\) for all \\(x \in \mathbb{F}^n\\) and all \\(a, b \in \mathbb{F}\\).

### Solution
$$
\begin{align}
(ab)x &= (ab)(x_1, \ldots, x_n) && \\
        &= ((ab)x_1, \ldots, (ab)x_n) && \\
        &= (a(bx_1), \ldots, a(bx_n)) && \text{ associativity of multiplication on } \mathbb{F} \\
        &= a(bx_1, \ldots, bx_n) && \\
        &= a(b(x_1, \ldots, x_n)) && \\
        &= a(bx)
\end{align}
$$

## Chapter 2: Finite-Dimensional Vector Spaces

### Exercise 2.A.1
Find a list of four distinct vectors in \\(\mathbb{F}^3\\) whose span equals
$$
\{(x, y, z) \in \mathbb{F}^3 : x + y + z = 0\}
$$.

### Solution: