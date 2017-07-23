+++
date = "2017-07-23T22:47:46+08:00"
title = "Variables"
toc = true
weight = 40

+++

### Variables

Sometimes, it is necessary to hold result of computation and to reuse it in future.

For example, to compute \\[(1+2+3+\cdots+10)+(1+2+3+\cdots+10)^2+(1+2+3+\cdots+10)^3\\]

1. Store the result of $$(1+2+3+\cdots+10)$$ to a variable `N`.
1. Compute the result of $$N+N^2+N^3$$.

```python
N = 1+2+3+4+5+6+7+8+9+10
N + N^2 + N^3
```



**We use the operator `=` for storing (assignment)**, 

i.e. to store the result of right-hand-side to the variable on the left.


*When an assignment is used, the result is suppressed.*


### Question

1. What is the result of $$x+x^2+x^3$$?
1. What is the result of the following code? 

```python
a = 10
a = a^2
a = a^2
show(a)
```






