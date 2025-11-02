---
layout: post
title: "Exercises: Analysis I"
subject: "Mathematics"
---

# Chapter 2: Starting at the Beginning: The Natural Numbers

## Exercise 2.2.1
Prove Proposition 2.2.5.

## Solution:
Using induction on \\(a\\) and keeping \\(b\\) and \\(c\\) fixed, we look at the base case of \\(a = 0\\).
<br><br>
$$
\begin{align}
(0 + b) + c &= b + c && \text{ definition of addition } \\
            &= 0 + (b + c) && \text{ definition of addition }
\end{align}
$$

Now we assume inductively that \\((a + b) + c = a + (b + c)\\),
<br><br>
$$
\begin{align}
((a\text{++}) + b) + c &= ((a + b)\text{++} + c) && \text{ definition of addition } \\
                &= ((a + b) + c)\text{++} && \text{ definition of addition } \\
                &= (a + (b + c))\text{++} && \text{ inductive step } \\
                &= (a\text{++}) + (b + c) && \text{ definition of addition }
\end{align}
$$

This closes the induction.

## Exercise 2.2.2
Prove Lemma 2.2.10.

## Solution:
Using induction on \\(a\\), the base case of \\(a = 0\\) is vacuously true since \\(a\\) is not a positive number (by definition).

Now, we assume inductively that there exists exactly one natural number \\(b\\) such that \\(b\text{++} = a\\). We now need to prove that there exists exactly one natural number \\(c\\) such that \\(c\text{++} = a\text{++}\\). We can show the existence of \\(c\\) since \\(a\text{++} = a\text{++}\\), hence \\(c = a\\), and \\(a\\) is a natural number (inductive step). We can show the uniqueness of \\(c\\) by Axiom 2.4, where \\(c = a\\).

This closes the induction.

## Exercise 2.2.3
Prove Proposition 2.2.12.

## Solution:
Let \\(a, b, c\\) be natural numbers, we want to prove that:

-   (Order is reflexive) \\(a \geq a\\).

    Since we know that \\(a = a + 0\\) (by Lemma 2.2.2) and that 0 is a natural number (by Axiom 2.1), it implies that \\(a \geq a\\) (by definition of ordering of the natural numbers).

-   (Order is transitive) If \\(a \geq b\\) and \\(b \geq c\\), then \\(a \geq c\\).

    Using induction on \\(c\\), for the base case of \\(c = 0\\), we have \\(a = 0 + a\\) (by definition of addition), implying that \\(a \geq 0\\) (by definition of ordering of the natural numbers). We assume inductively that if \\(a \geq b\\) and \\(b \geq c\\), then \\(a \geq c\\). We now need to prove that if \\(a \geq b\\) and \\(b \geq c\text{++}\\), then \\(a \geq c\text{++}\\).

    Since \\(b \geq c\text{++}\\) implies \\(b = c\text{++} + d\\) for some natural number \\(d\\) (by definition of ordering of natural numbers), it also implies \\(b = c + 1 + d\\) (by Lemma 2.2.2 and Lemma 2.2.3) and since \\(1 + d\\) is a natural number (by commutativity of addition, Lemma 2.2.2 and Lemma 2.2.3), we know that \\(b \geq c\\). Since we also know that \\(a = b + e\\) for some natural number \\(e\\) (by definition of ordering of natural numbers), it implies that \\(a = (c\text{++} + d) + e = c\text{++} + (d + e)\\) (by associativity of addition), and that \\(d + e\\) is a natural number (sum of two natural number is a natural number), hence \\(a \geq c\text{++}\\).

    This closes the induction.

-   (Order is antisymmetric) If \\(a \geq b\\) and \\(b \geq a\\), then \\(a = b\\).

    If \\(a \geq b\\), then it implies \\(a = b + d\\) for some natural number \\(d\\), and if \\(b \geq a\\), then it implies \\(b = a + e\\) for some natural number \\(e\\). This also implies that:
    <br><br>
    $$
    \begin{align}
    a = b + d &= (a + e) + d && \\
                &= a + (e + d) && \text{ by commutativity of addition } \\
    a + 0       &= a + (e + d) && \text{ by Lemma 2.2.2 } \\
    0           &= e + d && \text{ by cancellation law } \\
    \end{align}
    $$
    
    and this implies that \\(e = 0\\) and \\(d = 0\\) (by Corollary 2.2.9), and that \\(a = b + 0\\), and \\(a = b\\) (by Lemma 2.2.2).

-   (Addition preserves order) \\(a \geq b\\) if and only if \\(a + c \geq b + c\\).