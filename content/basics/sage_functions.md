+++
date = "2017-07-25T14:26:49+08:00"
title = "Functions"
toc = true
weight = 50

+++

A function/mapping takes objects and returns objects.
It is usually written in the form
$$ F: A \to B $$
Here, $F$ is the name of the function, $A$ is the possible input and $B$ is the possible output.

The mapping when stated explicitly is denoted $x \mapsto y$.

## Example

The real $\sqrt{x}$ is a function that takes a number and returns a non-negative number whose square is the input.

$sqrt : Number \to Number$

$Area$ : $Polygon \to Number$

$angle\\_between\\_hands$ : $Time \to Angle$

$is\\_square$ : $Number \to Boolean$

## Sage function

The sage function `is_square` checks if a given number is a perfect square.

```python
is_square(100)  # This gives True
is_square(3) # This gives False
```



```python
# The below two lines define a sqr function.
def sqr(x):
    return x^2

sqr(10) # This will gives 100
```


```python
# There are more than one ways to compute the last digit of a given integer.

def last_digit(x):
    return x%10

def last_digit2(x):
    return ZZ(x).digits()[0]
```

```python
def first_digit(x):
    return ZZ(x).digits()[-1]
```

```python
def digit_sum(x):
    return sum(ZZ(x).digits())
```

```python
def area_of_square(side):
    return side*side

def area_of_parallelogram(base,height):
    return base*height
```


## Exercise

### Perimeters

File: `Lessons 2/perimeters.sagews`



### Angle between hands

#### Problem

```
Input: A given time t (a pair of number that represents hour and minute).

Output: The angle between them in degree.

```
#### Sample

Input: (03,00)

Output: 90$^{\circ}$

#### Task

Please complete the below functon to compute the required angle.

File: `Lesson 2/angle_between_hands.sagews` 

```python
def angle_between_hands(t):
    hour = t[0]
    minute = t[1]
    angle_of_minute = t[1] * 6
    # Complete below
    angle_of_hour = 0 # C
    ans = abs(angle_of_minute - angle_of_hour)
    return ans
```

