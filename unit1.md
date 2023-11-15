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

:::{tip}
Code cells on this Markdown page are not executed when the page is built.
:::

This is the mean of some random numbers using numpy.

```{code-cell} python3
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

:::{tip} Tip with Title
This is an example of a callout with a title.
:::

Here's a tabset

::::{tab-set}
:::{tab-item} R
:sync: tab1

```{code} R
:name: R example
:caption: fizz_buzz definition in R
fizz_buzz <- function(fbnums = 1:50) {
  output <- dplyr::case_when(
    fbnums %% 15 == 0 ~ "FizzBuzz",
    fbnums %% 3 == 0 ~ "Fizz",
    fbnums %% 5 == 0 ~ "Buzz",
    TRUE ~ as.character(fbnums)
  )
  print(output)
}

fizz_buzz(3)
```

:::
:::{tab-item} Python
:sync: tab2
```{code} python
:name: Python example
:caption: fizz_buzz definition in Python

def fizz_buzz(num):
  if num % 15 == 0:
    print("FizzBuzz")
  elif num % 5 == 0:
    print("Buzz")
  elif num % 3 == 0:
    print("Fizz")
  else:
    print(num)

fizz_buzz(3)
```
:::
::::
