---
layout: post
title: "Exercises: Linear Algebra Done Right"
subject: "Mathematics"
---

## Chapter 1: Vector Spaces

### Exercise 1.A.1
The question asks to prove that the additive inverse in a vector space is unique.

**Solution:**
Suppose an element $v \in V$ has two additive inverses, $w_1$ and $w_2$.
By definition of an additive inverse, we have $v + w_1 = 0$ and $v + w_2 = 0$.

We can write:
$$
w_1 = w_1 + 0 = w_1 + (v + w_2) = (w_1 + v) + w_2 = 0 + w_2 = w_2
$$
This shows that $w_1 = w_2$. Therefore, the additive inverse is unique. ✨