+++
date = "2017-07-23T18:40:17+08:00"
title = "Exact Arithmetic"
toc = true
weight = 30

+++

Try to type the following code in the edtior.

### Integer addition
```python
2+5
```
### Addition of fractions

$\frac{1}{3} + \frac{1}{6}$

```python
1/3 + 1/6
```

*You will see the answer `1/2` is shown as inline form.*

### Math formatting

Use the function `show` to enclose the expression for mathematical (LaTeX) display.

```python
show(1/3+1/6)
```

### Symbolic addition

In Sage, we can handle symbolic computation $x+y+x+x+y$.

```python
var("x y") # This line explicitly declares that x and y as symbolic variables.
x+y+x+x+y
```
_Note that, the answer is displayed as `3*x+2*y` instead of $3x+2y$._

### Last result

Again, one can enclose the expression by show. But, we will use Python's magic variable `_`.

The `_` holds the last computed result.

```python
show(_)
```

### Multiplication

To compute $a\times b$, we use `*`. 


```python
142857*7
```

### Power

Power is expressed by `^` (Sage-only) or `**` (Pythonic way).

```python
2^100
```

*Unlike traditional programming languages C,C++, Java etc., there is no limitation of the size of numbers to be evaluated.*


These are the upper limit of in usual programming languages:
```python
2^31 - 1  # 2147483647
2^63 - 1  # 9223372036854775807
```


### Quotient and Modulus (Remainder)

To evaluate the quotient and remainder when $a$ is divided by $b$, we use the operators `//` and `%`.

```python
50000 // 9  # This computes the quotient
50000 % 9   # This computes the modulus (remainder)
```

### Solving equation

To solve equation like $3x+7 = 10$, we use `solve`.

```python
solve(3*x+7==10,x)
```


### Exercises

1. Can you tell what is so special about the number $142857$?
1. Find the largest prime number that is less than $2025$.
1. If $n$ is an odd perfect square, find all possible values of the remainder when $n$ is divided by 4.

### Olympiad corner

1. (PCIMC-2009) Let $n$ be a positive integer. It is known that 20090124 leaves a remainder of 4 when divided by $n$. Find the smallest possible value of $n$.
1. (PCIMC-2009) What is the remainder when the 2009-digit $1000\cdots 0001$ is divided by 11?
1. (PCIMC-2009) What is the remainder when the 2009-digit $1000\cdots 0001$ is divided by 7?
1. (PCIMC-2010) Find the first four digits of $20100123^2$.
