---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

```{code-cell} ipython3
:tags: [remove-cell]
%matplotlib inline
```

# Arithmetics and variables

## Arithmetic operations

Any arithmetical operation is performed simply by writing its equation. For example, the most usual arithmetic operators are `+`, `-`, `*` and `/`:

```{code-cell}
print(4 + 3)
```

```{code-cell}
print(4 - 3)
```

```{code-cell}
print(4 * 3)
```

```{code-cell}
print(4 / 3)
```

:::{goodpractice} Space between operators
For readability, it is a good practice to put spaces between the operators. To illustrate this practice, look how

```
print(2 * ((4 + 2) / 3))
```

is easier to decipher than

```
print(2*((4+2)/3))
```

This is however only a style convention, it is highly subjective, and both forms work equally. This convention is part of [PEP8 - the Style Guide for Python Code](https://pep8.org/). As PEP8 is followed by many Python projects and programmers, it may be useful to have a look at this document if you want to collaborate with other Python programmers in the future. Using a similar and popular convention always helps in collaborating.
:::

## Variables

A fundamental concept in programming is the variable. A variable is some space in memory that can store a value. In Python, there is no need to declare or allocate variables. All you have to do to define a variable is to assign it a value using the `=` operator. For example, we could have two variables, `a` and `b`, that both store a different number:

```{code-cell}
a = 4
b = 3
```

Now, we can refer to the value of a variable simply by referring to the variable name:

```{code-cell}
print(a + 1)
```

```{code-cell}
print(a + b)
```

We can even assign the result of an operation to a new variable:

```{code-cell}
c = a + b
print(c)
```

Keep in mind that in the last example, we did not tell to Python that `c` must always be equal to `a + b`. This is not how a sequential programming language such as Python works. Instead, we told Python, at this instant, to calculate the result of `a + b` and to store it in a new variable `c`. The sequential nature of Python (and many other languages) is illustrated with this example:

```{code-cell}
c = c + 1
print(c)
````

As with the previous example, we told Python to calculate the result of `c + 1` and to store it in the variable `c`.

:::{important}
Python is case-sensitive. This means that `a` is not the same thing as `A`. Similarly,

```
Print("Hello world")
```

or

```
PRINT("Hello world")
```

would result in an error because neither `Print` or `PRINT` exists. However,

```
print("Hello world")
```

works.
:::

## Exercise

:::{exercise} Timing gates
A sprinter runs through two timing gates spaced by 50 m. Each timing gate records the time (in seconds) at which the sprinter pass through it.

![exercices_illustration -width:normal](_static/images/exercise_timing_gates.png)

Given the following program:

```
time_gate1 = 1.3
time_gate2 = 6.7
distance_gates12 = 50.0
```

Continue this program so that it prints the mean velocity of the sprinter between gates 1 and 2. You can then show a suggested answer by clicking on the plus sign below.
:::

```{code-cell}
:tags: [hide-cell]

time_gate1 = 1.3
time_gate2 = 6.7
distance_gates12 = 50.0

print(distance_gates12 / (time_gate2 - time_gate1))
```

:::{goodpractice} Variable names
It is generally a good idea to use names rather than letters for variables. For example, this code:

```
velocity = distance / duration
print(velocity)
```

is clearer than:

```
v = d / t
print(v)
```

In addition, the [PEP8](https://pep8.org/) recommends to use all lower case for variables, and to generally separate multiple words by underscores (`_`), e.g., `power`, `mean_power`, `peak_power`.
:::
