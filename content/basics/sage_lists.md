+++
date = "2017-07-23T23:01:48+08:00"
title = "Lists"
toc = true
weight = 60

+++

### Fibonacci sequence

The Fibonacci sequence is: \\[1,1,2,3,5,8,13,\cdots\\]

The $n^{th}$ term is usually denoted $F_n$.

We use `L = [1,1,2,3,5,8,13]` to specify a list (zero-indexed sequence) and stores it to `L`.

One can access the $$1^{st}$$ term with `L[1]`.

```python
L = [1,1,2,3,5,8,13]
```


### Zero-th index property

In programming, list/sequence are usually indexed from zero.

It is common to extend the sequence by the zero-th term, i.e. when $n=0$.

Recall that $$F\_{n+2} = F\_{n+1} + F_n $$, by setting $n=0$, we have $F\_n = 0$.

```python
F = [0,1,1,2,3,5,8,13]
```

Thus, we can align the index in sage as usual sequence.

### List access

To access a single element of a list, we use the square bracket to enclose the index.

Index can be negative (as in modular arithmetic).


```python
F = [0,1,1,2,3,5,8,13]

F[6] # This is 8

F[-1] # The rightmost element

F[-2] # 8 again
```

We can use the **slice** format `[start:stop:step]` to take a sub-list.

The range is specified with inclusive open and exclusive ending.


```python
F = [0,1,1,2,3,5,8,13]

F[1:] # A sub-list with elements of F[1], F[2], ...  (i.e. dropping the 0-th term)

F[:-1] # A sub-list without the last element

F[1:3] # A list of just two elements of F[1], F[2]

F[::2] # A list [0,1,3,8]

```


### Common sequences

To specify a list of consecutive integers, e.g. `[ 3 .. 100 ]`.

`range(100)` can be used to specify a list of 100 consecutive integers starting from 0.


### List comprehension

To construct a list of 10 square numbers: `[k^2 for k in range(10)]`.

To construct a list of 10 even numbers: `[2*k for k in range(10)]`.

### List filtering

A list of numbers within 100 that is not divisible by 3: 

```python
[ k for k in range(100) if k%3 != 0 ]
```

A list of numbers withint 1000 that is divisible by 2 or 3:

```python
[ k for k in range(1000) if k%2 == 0 or k%3 == 0 ]
```


`==` is used for equality comparison

`!=` is used for comparison, i.e. $\neq$.


### List operations

| Name | Description | Example |
| ------------- |:-------------:| -----:|
| `sum` | Total sum | `sum([1..100])` |
| `prod`| Total product | `prod([1..10])` |
| `len` | Total length of list | `len(range(10))` |
| `count`| Number of occurences | `[1,1,2,3,1,1,2,1,1].count(1)`|


### Questions

1. How many integers from 1 to 100 is not divisible by 2 nor divisible by 3?
1. What is the largest 4-digit number that is not a multiple of 13 but is divisible by 7? 
1. How many square numbers (including 0) are less than 2011 and divisible by 7?
1. Find the smallest positive integer which leaves a remainder of 2 when divided by 7 and 4 when divided by 13.
