---
title: "Resources"
author: "Rohan Gala"
date: "2024-01-17"
date-modified: last-modified
categories: ["general"]
toc: true
number-sections: true
number-depth: 2
highlight-style: pygments
html-math-method: katex
bibliography: "../refs.bib"
code-fold: true
format:
  html:
    theme: cosmo
    css: ../styles.css
---

 - [Matrix reference manual](http://www.ee.ic.ac.uk/hp/staff/dmb/matrix/intro.html#Intro)
 - [Probability distributions explorer](https://distribution-explorer.github.io/)

I think real world systems are only partially changeable. Even a randomly connected Hopfield net stores information in the form of stable points. 

The questions I have are:
 - Can the stable patterns of this system be discovered?
 - Can a smaller system use the stable patterns of a larger system to store information efficiently?


Here is the setup of a Hopfield network that can store arbitrary patterns:

 - Each unit can have two states: $s_i \in \{0,1\}$.
 - Connection between units $i$ and $j$ is $w_{ij}$.
 - Each unit has a threshold $\theta_i$.
 - State changes:
 $s_i(t+1) =  \begin{cases}
              0 &\text{if } \sum_{j}{w_{ij} s_j} \lt \theta_i \\
              1 &\text{if } \sum_{j}{w_{ij} s_j} \geq \theta_i
              \end{cases}$
 - Update rules:

(How are these update rules derived?)

A basic implementation:



Let a physical system described by coordinates $X_1, X_2, \ldots, X_N$, the components of a state vector $\mathbf{X}$. Let the system have locally stable limit points $\mathbf{X_a}, \mathbf{X_b}, \ldots)$. Then, if the system is started sufficiently near any $\mathbf{X_a}$, as at $\mathbf{X} = \mathbf{X_a}+\Delta$, it will proceed in time until $\mathbf{X} \approx \mathbf{X_a}$.

Then we can regard the information stored in the system as the vectors $\mathbf{X_a}, \mathbf{X_b}, \ldots$. The starting point $\mathbf{X} = \mathbf{X_a} + \Delta$ represents a partial knowledge of the item $\mathbf{X_a}$, and the system then generates the total information $\mathbf{X_a}$.

Any physical system whose dynamics in phase space is dominated by a substantial number of locally stable states to which it is attracted can therefore be regarded as a general content-addressable memory.


### References

::: {#refs}
:::