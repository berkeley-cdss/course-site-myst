---
title: "Unit 1: Intro"
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
math:
  '\trans': '^\mathsf{T}'
  '\eps': '\epsilon'
---

:::{warning}
Code cells are not actually executed when the page is built.
:::

This is the mean of some random numbers using numpy.

```{code-cell} ipython3
import numpy as np
mean = np.mean(np.random.normal(size=100))
print(f"{mean=}")
```

$$
\theta = \int_0^\infty f(x,\theta)d\theta
$$

Use a $\LaTeX$ macro.

$$
A = X \trans Y
$$
