---
layout: post
title: Differential Equations I
category: Math
tags: [math, differential-equations]
---

## Introduction
> The *differential* and *equation* suggest solving some kind of equation that contains derivatives $y'$, $y''$
> Solving differential equations such as $y'' + 2y' + y = 0$ for unknown fuction $y = \phi\left(x\right)$.

# Chapter 1: Introduction to Differential Equations

## 1.1 Definitions and Terminology

#### Definition 1.1.1
> **Differential Equation**\
> An equation containing the derivatives for one or more unknown functions (or dependent variable), concerning one or more independent variables, is said to be a **differential equation (DE)**


### Classification by Type
If a differential equation contains only ordinary derivatives of one or more unknown functions concerning a single independent variable, it is said to be an **ordinary differential equation (ODE)**.
> Example 1.1.1
> 
> $$\frac{dy}{dx} + y = e^{x}$$


If an equation involving partial derivatives of one or more unknown functions of two or more independent variables is a **partial differential equation (PDE)**.
> Example 1.1.2
> 
> $$\frac{\partial^2 y}{\partial x^2} + y = 0$$

### Classification by Order
The order of a differential equation is the order of the highest derivative in the equation.
> Examlple 1.1.3
> 
> $$\frac{dy}{dx} + y = e^{x}$$

The order of the above equation is one.

> **Differential Form**
>
>$$M(x,y)dx + N(x,y)dy = 0$$

### Classification by Linearity
An nth-order ordinary differential equation is called to be linear if *F* is linear in $y,y',...,y^{(n)}$. This means that an nth-order ODE is linear when is

$$ a_n(x)y^{(n)}+a_{n-1}(x)y^{(n-1)} + ... +a_1(x)y'+a_0(x)y - g(x) = 0$$


> Example 1.1.4\
> Linear
> 
> $$y'' -2y' + y = 0$$
> 
> Nonlinear
> 
> $$(1-y)y' +2y = e^{x}$$


### Solutions
>**Solution of an ODE**
>Any function,  $\phi$ defined on an interval I and possessing at least n derivatives that are continuous on I, which when substituted into an -order ordinary differential equation reduces the equation to an identity, is said to be a solution of the equation on the interval.

In other words, a solution of an nth-order ordinary differential equation is simply a form of

$$y = f{(x)}$$ 

or

$$f(x,y) = C $$ 

### Explicit and Implicit Solutions
- Explicit Solution is a form of

$$y = f{(x)}$$

- Implicit Solution is a form of

$$f(x,y) = C $$

### Families of Solutions
The study of DE is similar to that of intergral at calculus. A solving the DE is same as finding an antiderivate or indefinite integral in calculus.\
For example, when solving a first-order DE $F(x,y,y') = 0$ we usually get a solution that contains a constant c. A solution $G(x,y,c) = 0$ called a **one-parameter family of solutions**.\
When solving an nth-order DE $F(x,y,y',...,y^{(n)}) = 0$ we get an nth-parameter family of solutions $G(x,y,c_1,c_2,...,c_n) = 0$ called **nth-parameter family of solutions**

## 1.2 Initial-Value Problems
