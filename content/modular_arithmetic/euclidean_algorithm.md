+++
date = "2017-07-25T15:54:17+08:00"
title = "Euclidean algorithm"
toc = true
weight = 250

+++

## Property

Greatest common divisor (gcd) and lowest common factor (lcm) of numbers $a$ and $b$ are related by


$$a\times b= \mathrm{gcd}(a,b) \times \mathrm{\ell cm}(a,b)$$

---

The gcd function (which takes two inputs) has the following properties:

$$\mathrm{gcd}(a,b) = \mathrm{gcd}(b,a)$$
$$\mathrm{gcd}(a,b) = \mathrm{gcd}(a,b-a)$$
$$\mathrm{gcd}(a,0) = a $$ 

By repeated application of the second rule, we have

$$\mathrm{gcd}(a,b) = \mathrm{gcd}(a,b \bmod a)$$

---

Example

$$\mathrm{gcd}(300,144) = \mathrm{gcd}(144,300 - 2\times 144) = \mathrm{gcd}(144,12) = \mathrm{gcd}(12, 144 - 12\times12) = 12 $$


Another way to express the above computation is 

$$\mathrm{gcd}(300,144) = \mathrm{gcd}(144, 300 \bmod 144) = \mathrm{gcd}(144,12) = \mathrm{gcd}(12, 144 \bmod 12) = 12 $$



```python
gcd(300,144)  # Take two numbers as input

gcd([300,144]) # Take a single input which is a list of two numbers

lcm(300,144)

lcm([300,144])
```

The list version is useful when more than two numbers are considered.

---

### Extended Euclidean algorithm

It turns out the algorithm produces a pair of integers $m,n$ such that $$300m + 144n = 12$$

It is always true that one can get a pair of integers $m,n$ such that $$ma + nb = \mathrm{gcd}(a,b)$$

*Do you still remember the coin exchange problem in the test? This is the key to solve it.*

### Modular linear equation

To solve the equation $3x+3 = 4 \pmod{13}$ by hand as usual to get $ 3x  = 1 \pmod{13} $.

By trial and error, we know that $3\times9=27=1\pmod{13}$. 

Hence, $x=9 \pmod{13}$ is a possible solution.

---

Alternatively, note that $\mathrm{gcd}(3,13) = 1$. We can find a pair $m,n$ such that $$3m+13n = 1$$

The pair and the gcd can be computed at the same time in sage:

```python
d,m,n = xgcd(1,3,13)
```

Giving $$(-4)\times 3 + (1) \times 13 = 1$$

by taking modulo 13, we have $$(-4)\times 3 = 1 \pmod{13}$$

## Task

1. In addition to the pair $(-4,1)$, can you find some other pairs?
1. Finish ProjectEuler Problem 5 (https://projecteuler.net/problem=5).


### Further readings

- Postage stamp problem:
  - https://en.wikipedia.org/wiki/Postage_stamp_problem
  - https://brilliant.org/wiki/postage-stamp-problem-chicken-mcnugget-theorem/
- Tabular method to compute the pair and gcd: https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm#Example
