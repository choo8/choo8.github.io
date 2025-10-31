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

Now, we assume inductively that there exists exactly one natural number \\(b\\) such that \\(b\text{++} = a\\). We now need to prove that there exists exactly one natural number \\(c\\) such that \\(c\text{++} = a\text{++}\\). We can show the existence of \\(c\\) since \\(a\text{++} = a\text{++}\\), hence \\(c = a\\), and \\(a\\) is a natural number (inductive step). We can show the uniqueness of \\(c\\) by Axiom 2.4.

This closes the induction.

## Exercise 2.2.3
Prove Proposition 2.2.12.

## Solution: