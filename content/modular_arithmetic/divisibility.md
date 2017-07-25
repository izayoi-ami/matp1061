+++
date = "2017-07-25T16:19:12+08:00"
title = "Divisibility"
toc = true
weight = 210

+++

## Divisibility for 7, 11 and 13

We have the alternating 3-digit sum for 7, 11 and 13: 

To find $210600900 \bmod{} 7$, we can proceed by: $(900-600+210) \bmod{} 7$.

The idea behind is 

$$210600900 =210\times1000^{2}+600\times1000+900$$
$$1  =1$$
$$1000  =\left(1001\right)-1$$
$$1000^{2}  =1001M+1$$
where $M$ is some integer, hence $1000^2$ is the sum of $1$ and a multiple of $1001$.

Since $7 \times 11 \times 13 = 1001 = 1000 + 1 = 10^3 + 1$, any multiple of $1001$ is automatically that of $7$, $11$ and $13$.

Therefore,
$$210600900 =210\times\left(1001M-1\right)+600\times\left(1001-1\right)+900\times1$$
$$\therefore 210600900 \equiv 210-600+900 \pmod{7}$$

#### Modular arithmetic way

The above operation can be written compactly:

$$ 1000^n = \left(-1\right)^n \pmod{7} $$
$$ 210600900 = 210 \times (-1)^2 + 600 \times (-1) + 900 \pmod{7} $$
$$ 210600900 = 210 - 600 + 900 \pmod{7} $$

*Note: the clock element $-1$  is the same as $6$.*

### Alternative checking for 11

Is $1023$ a multiple of $11$? 

One can check as follows:

$$1023 = 10 + 23 = 33 \equiv 0 \pmod{11} $$

since we have $100 = 99 + 1 \equiv 1 \pmod{11}$.

The above is called the 2-digit sum of 1023, where we group digits two by two and compute the total sum.

# Task

1. Verify the above computation in sage by using modulus operator `%`.
1. Verify the above step in sage by using `Mod` or `Integers`.

### Question

1. Why do we group digits three by three but not four by four etc.?
1. We know that divisiblity for 3 and 9 can be checked by digit sum. Are they any other integers with this property? Why?
  - Hint: Find all $n$ such that $ 10 = 1 \pmod{n} $.
1. Which number can be checked by alternating 2-digit sum?

## Additive and Multiplicative Order

**Definition**: Let $a$ be an element of $Z_n$ (i.e. all operations are under modulo $n$).

- Its **additive order** is the smallest positive integer $m$ such that $$a + a + \cdots + a = 0$$ (add $m$ times). In short, $$ma = 0 \pmod{n}$$
- Its **multiplicative order** is the smallest positive integer $k>1$ such that $$a \times a \times \cdots \times a = 1$$ (multiply $m$ times) (if exists). In short, $$a^k = 0 \pmod{n}$$


#### Example

The additive order of 3 in $Z_11$ is 4 by checking.

The multiplicative order of 1000 in $Z_7$ is 2 as shown above. Alternatively, we have $1000 = 6 \pmod{7}$ and hence $$1000^2 = 36 = 1 \pmod{7}$$



The additive order is computed by `element.order()`:

```python
Mod(3,11).order()
```

The multicative order is computed by `element.multiplicative_order()`:
```python
Mod(1000,7).multiplicative_order()

```

# Task

1. Find the multiplicative order of $10$ in $Z_7$.
1. What is the period of recurring decimal of $\frac{1}{7}$?
1. Find the multiplicative order of $37$ in $Z_7$.
1. What is the period of recurring decimal of $\frac{1}{37}$?


