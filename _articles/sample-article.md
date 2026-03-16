---
layout: post
title: "Sample Article"
topic: Machine Learning
date: 2026-03-15
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit. In supervised learning, we seek a function \\(f: \mathcal{X} \to \mathcal{Y}\\) that minimizes the expected risk over some data distribution \\(\mathcal{D}\\).

## Loss Functions

Given a dataset \\(\{(x_i, y_i)\}_{i=1}^{n}\\), the empirical risk is defined as:

$$\hat{R}(f) = \frac{1}{n} \sum_{i=1}^{n} \mathcal{L}(f(x_i), y_i)$$

where \\(\mathcal{L}\\) is a suitable loss function. For regression tasks, the mean squared error is commonly used:

$$\mathcal{L}(f(x), y) = (f(x) - y)^2$$

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium. The bias-variance decomposition tells us that for any estimator \\(\hat{f}\\):

$$\mathbb{E}\left[(y - \hat{f}(x))^2\right] = \text{Bias}(\hat{f})^2 + \text{Var}(\hat{f}) + \sigma^2$$

## Gradient Descent

To minimize the empirical risk, we often use gradient descent with update rule:

$$\theta_{t+1} = \theta_t - \eta \nabla_\theta \hat{R}(f_\theta)$$

where \\(\eta > 0\\) is the learning rate. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt.

Under suitable convexity assumptions, gradient descent converges at a rate of \\(O(1/t)\\), and with strong convexity, the convergence improves to \\(O(e^{-ct})\\) for some constant \\(c > 0\\).
