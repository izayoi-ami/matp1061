+++
date = "2017-07-25T15:27:49+08:00"
icon = "<b></b>"
title = "Projects"
weight = 1000

+++

# Projects

See the folder: `Projects`

## Project 1: Shoelace's formula

Previously, our representation of a triangle is by three numbers (length of its sides). This is a valid representation because of the SSS congruence classification of triangle, i.e. every triangle of the same length of sides has the same geometric properties (including area, perimeter).
The only possible differences are : positions of the triangles, orientations (whether it is a mirror image)

However, we cannot do so for a polygon with more than three sides. For example, a square is not always the same as a rhombus as they can have different interior angle.

It turns out we can represent a convex polygon by a sequence of points (coordinates of its vertices).

For example, a triangle with vertices $A(0,0)$, $B(2,2)$ and $C(0,10)$ has area $\frac{2\times 10}{2}$.

#### Task:

1. Describe two completely different polygons with 5 equal sides.
1. Write a function that takes three sides of a triangle and returns the area of the triangle.
1. Write a function that takes three vertices (in coordinates) of a triangle and returns its area.
1. Write a function that takes four vertices (in coordinates) of a quadrilateral and returns its area.
1. Write a function that takes $n$ vertices (in coordinates) of a polygon and returns its area.

#### Links:
- https://en.wikipedia.org/wiki/Shoelace_formula


---

## Project 2: Divisibility and recurring decimals

In sage, you can write mathematical expressions by starting with the descriptor: `%md`

{{< figure src="/media/markdown.png" title="Markdown and Maths" >}}

1. Click the small arrow on line number 1 to read the source code.
1. Notice the usage of the pair of dollar symbols for math typesettings.


### Tasks

Type your answer using Markdown and LaTeX, and also with the help of Sage.

For the usage or list of mathematical symbols, you can refer to HostMath or detexify (http://detexify.kirelabs.org/classify.html).


1. Show that divisiblity of 37 can be checked by 3-digit group sum.
1. Find the period of the recurring decimal of:
  - $\frac{1}{101}$
  - $\frac{1}{123}$
  - $\frac{1}{1371}$
1. Let $n$ be a positive integer. On a paper, copy it twice. For example, if $n$ is 123, then your paper has the number 123123.
  - Find a $n$ such that the number on the paper is a perfect square.
  - Find the smallest such $n$. *Remember to explain your $n$ is the smallest.*

```python
def duplicate(n):
  return ZZ(str(n)*2)
```



