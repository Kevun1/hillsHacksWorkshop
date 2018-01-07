### Example 4 Continued

Let's add to the last example. It turns out that building staircases is actually really expensive: it costs one dollar for every pixel you draw with the turtle. 

Like before, write a program that will take in a sequence of numbers from the user, and draw a staircase with those numbers as the step lengths. However, this time, keep track of how many units you draw, and at the end display to the user how much the staircase costs. 

Solution:

```python
from turtle import *
t = Turtle()

intput_vales = input("Enter staircase lengths: ")
lengths = intput_vales.split(" ")

cost = 0

for length in lengths:
    length = float(length)
    t.forward(length)
    cost += length
    t.left(90)
    t.forward(30)
    cost += 30
    t.right(90)

print("The staircase costs $" + str(cost))
```


# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/example4%20part2.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/example4%20part4.md)
