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

    *Lemma: For any natural numbers \\(n\\) and \\(m\\), \\(n + m\\) is a natural number.*

    Using induction on n, for the base case, \\(0 + m = m\\) (by definition of addition) and since \\(m\\) is a natural number, \\(0 + m\\) is a natural number. We assume inductively that \\(n + m\\) is a natural number. We now look at \\(n\text{++} + m\\), which is \\((n + m)\text{++}\\) (by definition of addition). By the inductive step and Axiom 2.2, we know that \\((n + m)\text{++}\\) is a natural number.

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

    We will prove the forward direction first. \\(a \geq b\\) implies \\(a = b + d\\) for some natural number \\(d\\) (by definition of ordering of natural numbers). We then get \\(a + c = (b + d) + c\\), which then implies \\(a + c = (b + c) + d\\) (by commutativity of addition and associativity of addition), which finally shows \\(a + c \geq b + c\\).

    We will now prove the other direction. \\(a + c \geq b + c\\) implies \\(a + c = (b + c) + d\\) for some natural number \\(d\\) (by definition of ordering of natural numbers). We can show that \\(a + c = (b + d) + c\\) (by commutativity of addition and associativity of addition), and then \\(a = b + d\\) (by cancellation law), which finally shows \\(a \geq b\\).

-   \\(a < b\\) if and only if \\(a\text{++} \leq b\\).

    We will prove the forward direction first. \\(a < b\\) implies \\(b = a + d\\) for some natural number \\(d\\) (by definition of ordering of natural numbers) and \\(a \neq b\\). Since \\(a \neq b\\), it implies that \\(d \neq 0\\), else it will contradict Lemma 2.2.2. Hence, we know that \\(d\\) is a postive number (by definition of positive natural numbers) and it implies that there exists some natural number \\(e\\) such that \\(e\text{++} = d\\) (by Lemma 2.2.10). Hence, \\(b = a + e\text{++}\\), which implies \\(b = (a + e)\text{++}\\) (by Lemma 2.2.3), and \\(b = a\text{++} + e\\) (by definition of addition), which finally shows \\(a\text{++} \leq b\\).

    We will now prove the other direction. \\(a\text{++} \leq b\\) implies \\(b = a\text{++} + d\\) for some natural number \\(d\\) (by definition of ordering of natural numbers), which implies \\(b = (a + d)\text{++}\\) (by definition of addition), and \\(b = a + d\text{++}\\) (by Lemma 2.2.3), which finally shows \\(a \leq b\\). By Axiom 2.3, we know that \\(d\text{++} \neq 0\\) and hence \\(a \neq b\\). We prove it by contradictation, assume that \\(a = b\\), hence \\(b = b + d\text{++}\\), and \\(0 = d\text{++}\\) (by cancellation law) which leads to a contradiction and showing that \\(a \neq b\\). Finally, we show that \\(a < b\\).

-   \\(a < b\\) if and only if \\(b = a + d\\) for some positive number \\(d\\).

    We will prove the forward direction first. \\(a < b\\) implies \\(b = a + d\\) for some natural number \\(d\\) (by definition of ordering of natural numbers) and \\(a \neq b\\). Since \\(a \neq b\\), we know that \\(d \neq 0\\) (by above), hence \\(d\\) is a positive number (by definition of positive natural numbers).

    We will now prove the other direction. We assume that \\(b = a\\), hence by cancellation law, \\(0 = d\\), but since we know that \\(d\\) is a positive number, \\(d \neq 0\\) and which leads to a contradiction, showing that \\(b \neq a\\). Since \\(b = a + d\\) for some natural number \\(d\\) and \\(b \neq a\\), we can show that \\(a < b\\) (by definition of ordering of natural numbers).

## Exercise 2.2.4
Justify the three statements marked (why?) in the proof of Proposition 2.2.13.

## Solution:
-   When \\(a = 0\\) we have \\(0 \leq b\\) for all \\(b\\)

    Since \\(b = 0 + b\\) (by definition of addition) and \\(b\\) is a natural number, it implies that \\(0 \leq b\\) (by definition of ordering of natural numbers).

-   If \\(a > b\\), then \\(a\text{++} > b\\)

    If \\(a > b\\), then \\(a = b + d\\) for some natural number \\(d\\) and \\(a \neq b\\) (by definition of ordering of natural numbers). Hence \\(a\text{++} = (b + d)\text{++}\\), which implies \\(a\text{++} = b + d\text{++}\\) (by Lemma 2.2.3). Let's assume that \\(a\text{++} = b\\), it then implies \\(0 = d\text{++}\\) (by cancellation law), which leads to a contradiction (by Axiom 2.3), showing that \\(a\text{++} \neq b\\). Hence, \\(a\text{++} > b\\).

-   If \\(a = b\\), then \\(a\text{++} > b\\)

    Since \\(a = b\\), then \\(a\text{++} = b\text{++}\\) and \\(a\{++} = b + 1\\) (by Lemma 2.2.2 and Lemma 2.2.3). Assume that \\(a\text{++} = b\\), it implies \\(b\text{++} = b\\), then \\(b + 1 = b\\) (by Lemma 2.2.2 and Lemma 2.2.3), which implies \\(1 = 0\\) (by Lemma 2.2.2 and cancellation law), which implies \\(0\text{++} = 0\\), which leads to a contradiction (by Axiom 2.3), showing that \\(a\text{++} \neq b\\). Hence, \\(a\text{++} > b\\).

## Exercise 2.2.5
Prove Proposition 2.2.14.

## Solution:
Let \\(m_0\\) be a natural number, and let \\(P(m)\\) be a property pertraining to an arbitrary natural number \\(m\\). We then define \\(Q(n)\\) to be the property that \\(P(m)\\) is true for all \\(m_0 \leq m < n\\).

We look at the base case \\(Q(0)\\). Since \\(m_0 = 0 + m_0\\) (by definition of addition), we know that \\(0 \leq m_0\\) (by ordering of the natural numbers), hence \\(Q(0)\\) is vacuously true (by trichotomy of ordering for natural numbers). We now assume inductively that \\(Q(n)\\) is true, and look at \\(Q(n\text{++})\\). Since \\(Q(n\text{++}) = P(m)\\) for all \\(m_0 \leq m < n\text{++}\\), we know that \\(P(m)\\) is true for all \\(m_0 \leq m < n\\) (by inductive step), and \\(P(n)\\) is also true (by assumption in Proposition 2.2.14), hence we can see that \\(Q(n\text{++})\\) is true.

This closes the induction, showing that \\(P(m)\\) is true for all natural numbers \\(m \geq m_0\\).

## Exercise 2.2.6
Let \\(n\\) be a natural number, and let \\(P(m)\\) be a property pertaining to the natural numbers such that whenever \\(P(m\text{++})\\) is true, then \\(P(m)\\) is true. Suppose that \\(P(n)\\) is also true. Prove that \\(P(m)\\) is true for all natural numbers \\(m \leq n\\); this is known as the *principle of backwards induction*.

## Solution:

## Exercise 2.2.7
Let \\(n\\) be a natural number, and let \\(P(m)\\) be a property pertaining to the natural numbers such that whenever \\(P(m)\\) is true, \\(P(m\text{++})\\) is true. Show that if \\(P(n)\\) is true, then \\(P(m)\\) is true for all \\(m \leq n\\).

## Solution:

# Chapter 3: Set Theory