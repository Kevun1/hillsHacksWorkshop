### Example 4

Here's an example to apply the for loop. 

Consider the staircase we constructed earlier:


In our staircase each step was the same, fixed width long, as you would expect a staircase to be. But it doesn't have to be like that, each step could be varying lengths, like this:


Let's say your turtle was hired to build a staircase for a very particular manufacturer who wanted each step to be a very specific length long. This particular manufacturer wants a staircase with 10 steps, and steps 1-10 are 25, 45, 66, 10.5, 110, 9, 12, 18, 25, and 40 units long, respectively. He also wants each step to be 50 units high. Create a staircase with these specifications. 

```python
from turtle import *
t = Turtle()

lengths = [25, 90, 166, 50.5, 110, 90, 12, 30, 75, 50]

for length in lengths:
    t.forward(length)
    t.left(90)
    t.forward(50)
    t.right(90)
```

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/forloop2.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/example4 part2.md)
