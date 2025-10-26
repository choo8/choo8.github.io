---
layout: post
title: "Exercises: Linear Algebra Done Right"
subject: "Mathematics"
---

# Chapter 1: Vector Spaces

## Chapter 1A: \\(\mathbb{R}^n\\) and \\(\mathbb{C}^n\\) 

### Exercise 1A.1
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

### Exercise 1A.2
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

### Exercise 1A.3
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

### Exercise 1A.4
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

### Exercise 1A.5
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

### Exercise 1A.6
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

### Exercise 1A.7
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

### Exercise 1A.8
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

### Exercise 1A.9
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

### Exercise 1A.10
Explain why there does not exist \\(\lambda \in \mathbb{C}\\) such that
<br><br>
$$
\lambda(2 - 3i, 5 + 4i, -6 + 7i) = (12 - 5i, 7 + 22i, -32 - 9i)
$$.

### Solution:
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

### Exercise 1A.11
Show that \\((x + y) + z = x + (y + z)\\) for all \\(x, y, z \in \mathbb{F}^n\\).

### Solution:
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

### Exercise 1A.12
Show that \\((ab)x = a(bx)\\) for all \\(x \in \mathbb{F}^n\\) and all \\(a, b \in \mathbb{F}\\).

### Solution:
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

### Exercise 1A.13
Show that \\(1x = x\\) for all \\(x \in \mathbb{F}^n\\).

### Solution:
$$
\begin{align}
1x &= 1(x_1, \ldots, x_n) && \\
    &= (1x_1, \ldots, 1x_n) && \\
    &= (x_1, \ldots, x_n) && \text{ multiplicative identity on } \mathbb{F} \\
    &= x
\end{align}
$$

### Exercise 1A.14
Show that \\(\lambda(x + y) = \lambda x + \lambda y\\) for all \\(\lambda \in \mathbb{F}\\) and all \\(x, y \in \mathbb{F}^n\\).

### Solution:
$$
\begin{align}
\lambda(x + y) &= \lambda((x_1, \ldots, x_n) + (y_1, \ldots, y_n)) && \\
                &= \lambda(x_1 + y_1, \ldots, x_n + y_n) && \\
                &= (\lambda(x_1 + y_n), \ldots, \lambda(x_n + y_n)) && \\
                &= (\lambda x_1 + \lambda y_1, \ldots, \lambda x_n + \lambda y_n) && \text{ distributive property on } \mathbb{F} \\
                &= (\lambda x_1, \ldots, \lambda x_n) + (\lambda y_1, \ldots, \lambda y_n) && \\
                &= \lambda(x_1, \ldots, x_n) + \lambda(y_1, \ldots, y_n) && \\
                &= \lambda x + \lambda y
\end{align}
$$

### Exercise 1A.15
Show that \\((a + b)x = ax + bx\\) for all \\(a, b \in \mathbb{F}\\) and all \\(x \in \mathbb{F}^n\\).

### Solution:
$$
\begin{align}
(a + b)x &= (a + b)(x_1, \ldots, x_n) && \\
            &= ((a + b)x_1, \ldots, (a + b)x_n) && \\
            &= (ax_1 + bx_1, \ldots, ax_n + bx_n) && \text{ distributive property on } \mathbb{F} \\
            &= (ax_1, \ldots, ax_n) + (bx_1, \ldots, bx_n) && \\
            &= a(x_1, \ldots, x_n) + b(x_1, \ldots, x_n) && \\
            &= ax + bx
\end{align}
$$

## Chapter 1B: Definition of Vector Space

### Exercise 1B.1
Prove that \\(-(-v) = v\\) for every \\(v \in V\\).

### Solution:
$$
\begin{align}
-(-v) &= -(-v) + 0 && \text{ additive identity on } V \\
        &= -(-v) + (v + -v) && \text{ unique additive inverse on } V \\
        &= -(-v) + (-v + v) && \text{ commutativity of addition on } V \\
        &= (-(-v) + -v) + v && \text{ distributive property of } V \\
        &= v
\end{align}
$$

### Exercise 1B.2
Suppose \\(a \in \mathbb{F}, v \in V\\), and \\(av = 0\\). Prove that \\(a = 0\\) or \\(v = 0\\).

### Solution:
Assume that both \\(a \neq 0\\) and \\(v \neq 0\\),
<br><br>
$$
\begin{align}
av &= 0 && \\
a(\frac{1}{a})v &= (\frac{1}{a})0 && \\
v &= 0 && \text{ multiplicative inverse on } \mathbb{F}
\end{align}
$$

Hence, this contradicts the original assumption that both \\(a \neq 0\\) and \\(v \neq 0\\).

### Exercise 1B.3
Suppose \\(v, w \in V\\). Explain why there exists a unique \\(x \in V\\) such that \\(v + 3x = w\\). 

### Solution:
Suppose there exist \\(x, x' \in V\\) such that \\(v + 3x = w\\) and \\(v + 3x' = w\\).
<br><br>
$$
\begin{align}
v + 3x &= w && \\
        &= v + 3x' && \\
v + 3x + (-v) &= v + 3x' + (-v) && \\
3x &= 3x' && \text{ additive inverse on } V \\
(\frac{1}{3})(3x) &= (\frac{1}{3})(3x') && \\
x &= x' && \text{ multiplicative inverse on } \mathbb{F}
\end{align}
$$

Hence, \\(x = x'\\), proving that there exists a unique \\(x \in V\\) such that \\(v + 3x = w\\).

### Exercise 1B.4
The empty set is not a vector space. The empty set fails to satisfy only one of the requirements listed in the defintion of a vector space (1.20). Which one?

### Solution:
The empty set not satisfy the "additive identity" requirement, since \\(0 \notin \emptyset\\).

### Exercise 1B.5
Show that in the definition of a vector space (1.20), the additive inverse condition can be replace with the condition that
<br><br>
\\(0v = 0\\) for all \\(v \in V\\).

Here the 0 on the left side is the number 0, and the 0 on the right side is the additive identity of \\(V\\).

### Solution:
Replacing "additive inverse" condition,
<br><br>
$$
\begin{align}
0v &= 0 && \\
(1 + -1)v &= 0 && \text{ additive inverse on } \mathbb{F} \\
1v + (-1)(v) &= 0 && \text{ distributive property of } V \\
v + -v &= 0 && \text{ multiplicative inverse on } \mathbb{F}
\end{align}
$$

Since \\(-1 \in \mathbb{F}\\), hence we have \\(-v \in V\\), which satisfies the original condition.

### Exercise 1B.6
Let \\(\infty\\) and \\(-\infty\\) denote two distinct objects, neither of whcih is in \\(\mathbb{R}\\). Define an addition and scalar multiplication on \\(\mathbb{R} \cup \\{ \infty, -\infty \\}\\) as you could guess from the notation. Specifically, the sum and product of two real numbers is as usual, and for \\(t \in \mathbb{R}\\) define
<br><br>
$$
\begin{equation*}
t\infty = \begin{cases}
                -\infty & \text{ if } t < 0, \\
                0 & \text{ if } t = 0, \\
                \infty & \text{ if } t > 0, 
            \end{cases} \quad
t(-\infty) = \begin{cases}
                -\infty & \text{ if } t < 0, \\
                0 & \text{ if } t = 0, \\
                \infty & \text{ if } t > 0,
            \end{cases}
\end{equation*}
$$

and
<br><br>
$$
\begin{align}
t + \infty &= \infty + t = \infty + \infty = \infty \\
t + (-\infty) &= (-\infty) + t = (-\infty) + (-\infty) = -\infty\\
\infty + (-\infty) &= (-\infty) + \infty = 0.
\end{align}
$$

With these operations of addition and scalar multiplication, is \\(\mathbb{R} \cup \\{ \infty, -\infty \\}\\) a vector space over \\(\mathbb{R}\\)? Explain.

### Solution:
\\(\mathbb{R} \cup \\{ \infty, -\infty\\}\\) is not a vector space over \\(\mathbb{R}\\).
<br><br>
$$
\begin{align}
\infty &= \infty + 0 \\
        &= \infty + (\infty + (-\infty)) \\
        &= (\infty + \infty) + (-\infty) \\
        &= \infty + (-\infty) \\
        &= 0
\end{align}
$$

Hence, we can see that the associativity property of addition is not held in \\(\mathbb{R} \cup \\{ \infty, -\infty\\}\\).

### Exercise 1B.7
Suppose \\(S\\) is a nonempty set. Let \\(V^S\\) denote the set of functions from \\(S\\) to \\(V\\). Define a natural addition and scalar multiplication on \\(V^S\\), and show that \\(V^S\\) is a vector space with these definitions.

### Solution:
For \\(f, g \in V^S\\), let addition be defined as:
<br><br>
$$
(f + g)(x) = f(x) + g(x)
$$

for all \\(x \in S\\).

For \\(f \in V^S\\) and \\(\lambda \in \mathbb{F}\\), let scalar multiplication be defined as:
<br><br>
$$
(\lambda f)(x) = \lambda f(x)
$$

for all \\(x \in S\\).

Commutativity:

For any \\(f, g \in V^S\\),
<br><br>
$$
\begin{align}
(f + g)(x) &= f(x) + g(x) && \\
            &= g(x) + f(x) && \text{ commutativity of addition on } V \\
            &= (g + f)(x)
\end{align}
$$

for all \\(x \in S\\).

Associativity:

For any \\(f, g, h \in V^S\\) and \\(a, b \in F\\),
<br><br>
$$
\begin{align}
((f + g) + h)(x) &= (f + g)(x) + h(x) \\
                    &= f(x) + g(x) + h(x) \\
                    &= f(x) + (g + h)(x) \\
                    &= (f + (g + h))(x)
\end{align}
$$

for all \\(x \in S\\).
<br><br>
$$
\begin{align}
((ab)f)(x) &= (ab)f(x) \\
            &= a(bf(x)) && \text{ associativity of multiplication on } V \\
            &= a((bf)(x))
\end{align}
$$

for all \\(x \in S\\).

Additive identity:

Let the additive identity be \\(j\\) such that \\(j(x) = 0\\) for all \\(x \in S\\).
<br><br>
$$
\begin{align}
(f + j)(x) &= f(x) + j(x) && \\
            &= f(x) + 0 && \\
            &= f(x) && \text{ additive identity on } V
\end{align}
$$

for all \\(x \in S\\).

Additive inverse:

For every \\(f \in V^S\\), there exists \\(-f \in V^S\\) such that \\((-f)(x) = -(f(x))\\) for all \\(x \in S\\).
<br><br>
$$
\begin{align}
f(x) + (-f)(x) &= f(x) + -(f(x)) && \\
                &= 0 && \text{ additive inverse on } V
\end{align}
$$

for all \\(x \in S\\).

Multiplicative identity:

Let the multiplicative identity be \\(1 \in S\\).
<br><br>
$$
\begin{align}
(1f)(x) &= 1(f(x)) && \\
        &= f(x) && \text{ multiplicative identity of } V
\end{align}
$$

for all \\(x \in S\\).

Distributive properties:

For any \\(f, g \in V^S\\) and \\(a, b \in S\\),
<br><br>
$$
\begin{align}
a((f + g)(x)) &= a(f(x) + g(x)) && \\
                &= a(f(x)) + a(g(x)) && \text{ distributive property on } V \\
                &= (af)(x) + (ag)(x)
\end{align}
$$

for all \\(x \in S\\).
<br><br>
$$
\begin{align}
((a + b)f)(x) &= (a + b)(f(x)) && \\
                &= a(f(x)) + b(f(x)) && \text{ distributive property on } V \\
                &= (af)(x) + (bf)(x) 
\end{align}
$$

for all \\(x \in S\\).

Hence \\(V^S\\) is a vector space with those definitions of natural addition and scalar multiplication.

### Exercise 1B.8
Suppose \\(V\\) is a real vector space.
* The *complexification* of \\(V\\), denoted by \\(V_\mathbb{C}\\), equals \\(V \times V\\). An element of \\(V_\mathbb{C}\\) is an ordered pair \\((u, v)\\), where \\(u, v \in V\\), but we write this as \\(u + iv\\).
* Addition on \\(V_\mathbb{C}\\) is defined by
<br><br>
$$
(u_1 + iv_1) + (u_2 + iv_2) = (u_1 + u_2) + i(v_1 + v_2)
$$

for all \\(u_1, v_1, u_2, v_2 \in V\\).
* Complex scalar multiplication on \\(V_\mathbb{C}\\) is defined by
<br><br>
$$
(a + bi)(u + iv) = (au - bv) + i(av + bu)
$$

for all \\(a, b \in \mathbb{R}\\) and all \\(u, v \in V\\).

Prove that with the definitions of addition and scalar multiplication as above, \\(V_\mathbb{C}\\) is a complex vector space.

### Solution:
Commutativity:

For any \\((a, b), (u, v) \in V_\mathbb{C}\\),
<br><br>
$$
\begin{align}
(a + bi) + (u + vi) &= (a + u) + (b + v)i && \\
                    &= (u + a) + (v + b)i && \text{ commutativity of addition on } V \\
                    &= (u + vi) + (a + bi)
\end{align}
$$

Associativity:

For any \\((a, b), (c, d), (u, v) \in V_\mathbb{C}\\) and \\((e + fi), (m + ni) \in \mathbb{C}\\),
<br><br>
$$
\begin{align}
((a + bi) + (c + di)) + (u + vi) &= ((a + c) + (b + d)i) + (u + vi) && \\
                                    &= ((a + c) + u) + ((b + d) + v)i && \\
                                    &= (a + (c + u)) + (b + (d + v))i && \text{ associativity of addition on } \mathbb{R} \\
                                    &= (a + bi) + ((c + u) + (d + v)i) && \\
                                    &= (a + bi) + ((c + di) + (u + vi))
\end{align}
$$
<br><br>
$$
\begin{align}
((e + fi)(m + ni))(u + vi) &= ((em - fn) + (en + fm)i)(u + vi) && \\
                            &= ((em - fn)u - (en + fm)v) + ((em - fn)v + (en + fm)u)i && \\
                            &= ((em)u - (fn)u - (en)v - (fm)v) + ((em)v - (fn)v + (en)u + (fm)u)i && \\
                            &= (e(mu) - f(nu) - e(nv) - f(mv)) + (e(mv) - f(nv) + e(nu) + f(mu))i && \text{ associativity of multiplication on } V \\
                            &= (e(mu - nv) - f(mv + nu)) + (e(mv + nu) + f(mu - nv))i && \text{ distributive property of } V \\
                            &= (e + fi)((mu - nv) + (mv + nu)i) && \\
                            &= (e + fi)((m + ni)(u + vi))
\end{align}
$$

Additive identity:

Let the additive identity be \\((0, 0) \in V_\mathbb{C}\\),
<br><br>
$$
\begin{align}
(u + vi) + (0 + 0i) &= (u + 0) + (v + 0)i \\
                    &= u + vi && \text{ additive identity on } V
\end{align}
$$

Additive inverse:

Let the additive inverse of some \\((u, v) \in V\\) be \\((-u, -v) \in V_\mathbb{C}\\),
<br><br>
$$
\begin{align}
(u + vi) + (-u + (-v)i) &= (u + -u) + (v + -v)i && \\
                        &= 0 + 0i && \text{ additive inverse on } V \\
                        &= 0
\end{align}
$$

Multiplicative identity:

Let the multiplicative identity be \\((1, 0) \in V_\mathbb{C}\\),
<br><br>
$$
\begin{align}
(1 + 0i)(u + vi) &= (1u - 0v) + (1v + 0u)i && \\
                &= (u - 0) + (v + 0)i && \text{ multiplicative identity on } V \\
                &= u + vi
\end{align}
$$

Distributive properties:

For any \\((a, b), (c, d) \in V_\mathbb{C}\\) and \\((e + fi), (m + ni) \in \mathbb{C}\\),
<br><br>
$$
\begin{align}
(e + fi)((a + bi) + (c + di)) &= (e + fi)((a + c) + (b + d)i) && \\
                                &= (e(a + c) - f(b + d)) + (e(b + d) + f(a + c))i && \\
                                &= (ea + ec - fb - fd) + (eb + ed + fa + fc)i && \text{ distributive property on } V \\
                                &= (ea - fb) + (eb + fa)i + (ec - fd) + (ed + fc)i && \\
                                &= (e + fi)(a + bi) + (e + fi)(c + di)
\end{align}
$$
<br><br>
$$
\begin{align}
((e + fi) + (m + ni))(a + bi) &= ((e + m) + (f + n)i)(a + bi) && \\
                                &= ((e + m)a - (f + n)b) + ((e + m)b + (f + n)a)i && \\
                                &= (ea + ma - fb - nb) + (eb + mb + fa + na)i && \text{ distributive property on } V \\
                                &= ((ea - fb) + (eb + fa)i) + ((ma - nb) + (mb + na)i) && \\
                                &= (e + fi)(a + bi) + (m + ni)(a + bi)
\end{align}
$$

Hence \\(V^\mathbb{C}\\) is a vector space with those definitions of addition and scalar multiplication.

## Chapter 1C: Subspaces

### Exercise 1C.1
For each of the following subsets of \\(\mathbb{F}^3\\), determine whether it is a subspace of \\(\mathbb{F}^3\\).
* \\(\\{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1 + 2x_2 + 3x_3 = 0\\}\\)
* \\(\\{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1 + 2x_2 + 3x_3 = 4\\}\\)
* \\(\\{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1x_2x_3 = 0\\}\\)
* \\(\\{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1 = 5x_3\\}\\)

### Solution:
* \\((0, 0, 0) \in U\\) since \\(0 + 2(0) + 3(0) = 0\\).

    For some \\((x, y, z), (a, b, c) \in U\\), \\((x, y, z) + (a, b, c) = (x + a, y + b, z + c)\\), and \\((x + a) + 2(y + b) + 3(z + c) = (x + 2y + 3z) + (a + 2b + 3c) = 0\\).

    For some \\(a \in \mathbb{F}\\) and \\((x, y ,z) \in U\\), \\(a(x, y, z) = (ax, ay, az)\\), and \\((ax) + 2(ay) + 3(az) = a(x + 2y + 3z) = a0 = 0\\).

    Hence, \\(\\{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1 + 2x_2 + 3x_3 = 0\\}\\) is a subspace of \\(\mathbb{F}^3\\).

* \\((0, 0, 0) \notin U\\) because \\(0 + 2(0) + 3(0) \neq 4\\), hence \\(\\{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1 + 2x_2 + 3x_3 = 4\\}\\) is not a subspace of \\(\mathbb{F}^3\\).

* \\((1, 0, 1) + (0, 1, 0) \notin U\\) because \\((1, 0, 1) + (0, 1, 0) = (1, 1, 1)\\), and \\((1)(1)(1) \neq 0\\), hence \\(\\{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1x_2x_3 = 0\\}\\) is not a subspace of \\(\mathbb{F}^3\\).

* \\((0, 0, 0) \in U\\) since \\(0 = 5(0)\\).

    For some \\((x, y, z), (a, b, c) \in U\\), \\((x, y, z) + (a, b, c) = (x + a, y + b, z + c)\\), and \\(x + a = 5z + 5c = 5(z + c)\\), hence \\((x + a, y + b, z + c) \in U\\).

    For some \\(a \in \mathbb{F}\\) and \\((x, y ,z) \in U\\), \\(a(x, y, z) = (ax, ay, az)\\) and \\(ax = a(5z) = 5(az)\\), hence \\((ax, ay, az) \in U\\).

    Hence, \\(\\{(x_1, x_2, x_3) \in \mathbb{F}^3 : x_1 = 5x_3\\}\\) is a subspace of \\(\mathbb{F}^3\\).

### Exercise 1C.2
Verify all assertions about subspaces in Example 1.35.

### Solution:
* Since \\(\\{(x_1, x_2, x_3, x_4) \in \mathbb{F}^4 : x_3 = 5x^4 + b\\}\\) is a subspace of \\(\mathbb{F}^4\\),

    \\((0, 0, 0, 0) \in U\\), hence \\(0 = 5(0) + b\\), implying that \\(b = 0\\).

    Since \\(b = 0\\),
    
    \\(x_3 = 0 = 5(0) = 5(0) + 0 = 5x_4 + b\\), hence \\((0, 0, 0, 0) \in U\\).

    For some \\((w, x, y, z), (a, b, c, d) \in U\\), \\((w, x, y, z) + (a, b, c, d) = (w + a, x + b, y + c, z + d)\\), and \\((y + c) = (5z + 5d) = 5(z = d) \\).

    For some \\(a \in \mathbb{F}\\) and \\((x, y ,z) \in U\\), \\(a(x, y, z) = (ax, ay, az)\\) and

    Hence, \\(\\{(x_1, x_2, x_3, x_4) \in \mathbb{F}^4 : x_3 = 5x^4 + b\\}\\) is a subspace of \\(\mathbb{F}^4\\).

    Hence, \\(\\{(x_1, x_2, x_3, x_4) \in \mathbb{F}^4 : x_3 = 5x^4 + b\\}\\) is a subspace of \\(\mathbb{F}^4\\) if and only if \\(b = 0\\).

* Let \\(\\{f(x) = 0 : x \in [0, 1]\\}\\) be the additive identity, and \\(f \in U\\).

    For some \\(f, g \in U\\), \\((f + g)(x) = f(x) + g(x)\\).

### Exercise 1C.3
Show that the set of differentiable real-valued functions \\(f\\) on the interval \\((-4, 4)\\) such that \\(f'(-1) = 3f(2)\\) is a subspace of \\(\mathbb{R}^{(-4, 4)}\\).

### Solution:

### Exercise 1C.4
Suppose \\(b \in \mathbb{R}\\). Show that the set of continuous real-valued functions \\(f\\) on the interval \\([0, 1]\\) such that \\(\int_{0}^{1} f = b\\) is a subspace of \\(\mathbb{R}^{[0, 1]}\\) if and only if \\(b = 0\\).

### Solution:

### Exercise 1C.5
Is \\(\mathbb{R}^2\\) a subspace of the complex vector space \\(\mathbb{C}\\)?

### Solution:

# Chapter 2: Finite-Dimensional Vector Spaces

## Chapter 2A: Span and Linear Independence

### Exercise 2A.1
Find a list of four distinct vectors in \\(\mathbb{F}^3\\) whose span equals
$$
\{(x, y, z) \in \mathbb{F}^3 : x + y + z = 0\}
$$.

### Solution:
\\((1, -0.5, -0.5), (-0.5, 1, -0.5), (-0.5, -0.5, 1), (0, 0, 0)\\).

For any vector in the span:
<br><br>
$$
\begin{align}
x + y + z &= (a + b(-0.5) + c(-0.5) + d(0)) + (a(-0.5) + b + c(-0.5) + d(0)) + (a(-0.5) + b(-0.5) + c + d(0)) \\
            &= a - 0.5a - 0.5a + b - 0.5b - 0.5b + c - 0.5c - 0.5c \\
            &= 0
\end{align}
$$

### Exercise 2A.2
Prove or give a counterexample: If \\(v_1, v_2, v_3, v_4\\) spans \\(V\\), then the list
<br><br>
$$
v_1 - v_2, v_2 - v_3, v_3 - v_4, v_4
$$

also spans \\(V\\).

### Solution