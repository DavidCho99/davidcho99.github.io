---
layout: page
title: Math for ML
permalink: /math-for-ml/
---

This page distills the math that shows up repeatedly in practical ML (aligned with topics from *Neural Networks with PyTorch*).

## Table of Contents
* TOC
{:toc}

## Book Map (What Becomes "Math")

- Ch. 1-4 (Python): tools, not math (but numerical precision matters: floats, rounding).
- Ch. 5-8 (numpy/matplotlib/OpenCV/pandas): vectors/matrices, plotting, convolution as an operation, data handling.
- Ch. 9 (Linear regression): linear algebra + optimization.
- Ch. 10-11 (Feedforward nets): matrix calculus + chain rule (backprop).
- Ch. 12 (Validation): statistics mindset (generalization, leakage, metrics).
- Ch. 13 (CNN): convolution math (stride/padding/pooling).
- Ch. 14 (Cross entropy): probability + information theory.
- Ch. 15 (Autoencoder, transposed conv): representation learning + convolution transpose geometry.

## Chapter Highlights (1-15)

- Ch. 1 (Python I): binary/float representation -> rounding error, numerical stability.
- Ch. 2 (Python II): loops/conditionals -> training loops and data iteration patterns.
- Ch. 3 (Python III): functions/modules/exceptions -> reusable model/loss/training code.
- Ch. 4 (Python IV): OOP -> model classes and clean interfaces.
- Ch. 5 (numpy): array shapes, broadcasting -> linear algebra with `n x d` data matrices.
- Ch. 6 (matplotlib): plots -> loss curves, accuracy curves, diagnostics.
- Ch. 7 (OpenCV): kernel convolution -> same math as CNN conv layers.
- Ch. 8 (pandas): data frames -> preprocessing, feature selection, splits.
- Ch. 9 (Linear regression): least squares, normal equation, gradient descent, under/overfitting.
- Ch. 10 (FFNN): matrix notation, activations, first PyTorch model, backprop basics.
- Ch. 11 (FFNN II): batching/mini-batches, dropout regularization.
- Ch. 12 (Validation): train/val/test, MNIST + regression case studies, model selection.
- Ch. 13 (CNN): convolution + pooling geometry, parameter sharing, translation tolerance.
- Ch. 14 (Cross entropy): softmax probabilities, log-loss, info theory intuition.
- Ch. 15 (Topics): autoencoders, transposed conv, generation (sampling + decoding).

## 1) Linear Algebra You Use Every Day

### Vectors, matrices, and shapes

- Treat a dataset as a matrix: `X` is `n x d` (n samples, d features).
- A linear model is `y_hat = X w + b` (or `y_hat = X w` if you absorb `b` into `w`).

### Dot products and norms

- Dot product: `x^T w` measures alignment.
- L2 norm: `||w||_2^2 = w^T w` shows up in weight decay / ridge regression.

### Normal equation (least squares)

For linear regression with squared loss, the closed-form solution (when invertible) is:

$$
\hat{w} = (X^T X)^{-1} X^T y
$$

In practice, you often solve it via numerics (e.g. QR / SVD) or just do gradient descent.

## 2) Calculus + Optimization (Gradient Descent)

### Loss functions

- Regression: MSE
  $$
  L(w) = \frac{1}{n}\sum_{i=1}^n (y_i - \hat{y}_i)^2
  $$
- Binary classification: logistic loss (cross entropy with sigmoid).
- Multiclass classification: cross entropy with softmax.

### Gradient descent

The update rule:

$$
w \leftarrow w - \eta \nabla_w L(w)
$$

- `eta` (learning rate) too big: diverges; too small: slow.
- Batch vs mini-batch vs SGD is about how you approximate the gradient with subsets.

## 3) Probability + Statistics for ML

If you want a compact version: see the post [ML Statistics]({% post_url math/2026-04-15-ml-statistics %}).

### Conditional probability and Bayes

- Conditional: $$P(A|B)=\\frac{P(A\\cap B)}{P(B)}$$
- Bayes: posterior ∝ likelihood × prior

### Generalization mindset

- Train vs validation vs test: measure how well you generalize.
- Avoid leakage: any feature derived using test/validation information invalidates results.

## 4) Neural Networks: Forward Pass as Matrix Ops

For a fully-connected layer:

$$
z = W x + b,\quad a = \\phi(z)
$$

- `W` is weights, `b` is bias, `phi` is an activation function.
- For a batch, stack inputs into a matrix and use matrix multiplication.

### Common activations (and why they matter)

- ReLU: $$\\phi(z)=\\max(0,z)$$ (cheap, works well, but can "die" for negative region)
- Sigmoid: outputs in (0,1) (good for probabilities; can saturate)
- Tanh: outputs in (-1,1) (also saturates)

## 5) Backprop: Chain Rule (The Real Math)

Backprop is just repeated chain rule through a computation graph.

If `L` depends on `a`, and `a = phi(z)`, then:

$$
\\frac{\\partial L}{\\partial z} = \\frac{\\partial L}{\\partial a} \\odot \\phi'(z)
$$

For an affine layer `z = W x + b`:

$$
\\frac{\\partial L}{\\partial W} = \\frac{\\partial L}{\\partial z} x^T,\quad
\\frac{\\partial L}{\\partial b} = \\frac{\\partial L}{\\partial z},\quad
\\frac{\\partial L}{\\partial x} = W^T \\frac{\\partial L}{\\partial z}
$$

PyTorch autograd does this for you, but you still need this mental model to debug.

## 6) Regularization: Overfitting Control

### Weight decay (L2)

Add `lambda ||w||_2^2` to the loss. Equivalent to shrinking weights.

### Dropout

Randomly zero out activations during training (Bernoulli mask). Intuition: prevents co-adaptation and acts like an ensemble.

## 7) Convolutions (CNN Math)

### Convolution as a linear operator

A 2D convolution is a weighted sum of local patches (a sliding dot product).

- Kernel size controls local receptive field.
- Stride controls downsampling.
- Padding controls output size / boundary behavior.

### Pooling

- Max pooling: keep strongest activation in a region (translation tolerance).
- Average pooling: smoothing / downsampling.

## 8) Cross Entropy + Information Theory

### Softmax (multiclass probabilities)

$$
\\mathrm{softmax}(z)_k = \\frac{e^{z_k}}{\\sum_j e^{z_j}}
$$

### Cross entropy loss

For one-hot target `y` and predicted probabilities `p`:

$$
L = -\\sum_k y_k \\log p_k
$$

Intuition: heavily penalizes confident wrong predictions.

## 9) What To Build (Project Hooks)

- Linear regression baseline (closed-form + gradient descent).
- MLP on MNIST (batching, dropout).
- CNN on MNIST (conv + pooling).
- Classification with cross entropy + softmax.
- A simple autoencoder; optionally explore transposed conv for decoding.
