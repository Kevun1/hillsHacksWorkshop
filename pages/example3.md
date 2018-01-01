### Example 3

Write a program that divides a hypothetical pizza into an number of equally sized slices, like this for 5 slices:

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/pizza1.md width="360">

In other words, take a number from user input. Using turtle, draw that number of lines equally spaced from each other radiating out from the center. It can be thought of as cutting equally sized slices from a pizza. 

```
from turtle import *
t = Turtle()

slices = input("How many slices? ")
slices = int(slices)

radius = 200

angle = 360 / slices

for i in range(slices):
    t.forward(radius)
    t.back(radius)
    t.right(angle)
```

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/forloop.md) | [Next >]()
