+++
date = "2017-07-23T23:41:30+08:00"
icon = "<b>2. </b>"
title = "Modular arithmetic"
weight = 200

+++

### Chapter II

# Modular arithmetic

An elementary name for the topic is clock arithmetic.

1. Assume that we are using 24-hour system. It is now 11:00.
  - What was the time 12 hours ago?
  - What will the time be 50 hours later?
1. If we only focus on the hour of the time, what are the possible hours in this system?
1. It is now 17:00. It takes 13 hours for John for a single trip between Hong Kong and London. If he takes a round-trip journey now, find the time when he will be back.
1. It is now 03:00. The clock is not working properly, so that the clock advances by 7 hours when one hour has passed. How many hours do you need to wait so that the clock will show the time 12:00?



## Integer Modular Ring 

A clock arithmetic system of $n$ elements is denoted $Z\_n$.

It is called the integer modular ring of $n$ elements.

One can answer the above three questions in sage with modular ring:

```python
clock = Integers(24) # Clock arithmetic system with 24 numbers
T = clock(11)  # T stores the clock hour 11
T - 23 # The hour 23 hours ago
T + 50 # The hour 50 hours later
T + 2*13 # The hour after two single trips.
```

*Another way to specify an element from a given modular arithmetic system is `Mod(number, base)`*

```python
T = Mod(11,24)  # The number 11 of the 24-hour clock.
```


## Solving modular equation

Mathematically, in question 4, we are solving an equation of the form:
$$3 + 7x \equiv 12 \pmod{24}$$

The above notation explicitly states that one is solving the equation using clock arithmetic.

`solve_mod(equation, base, symbol)` returns all possible solutions.

```python
var("x") # Make sure x is an unknown symbol
solve_mod(3 + 7*x == 12, 24, x)
```
