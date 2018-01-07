### Example 4 Continued

Now, let's say you have a maximum of $200 to spend. You can't go over the limit. Extend the previous example so that if you end up having to draw over 200 units, stop drawing immediately and print a message saying you ran out of money. 

Before we going into the example, here's how you can exit a loop:

```python
for i in range(10):
    print(i)
    if i == 5:
        break
```

You can use the `break` statement to break out of loops. Whenever the program hits the break statement, it exits out of whatever loop it's in. You can use the `break` statement in this example to terminate the drawing if you end up going over 200 units.

Solution:

```python
from turtle import *
t = Turtle()

intput_vales = input("Enter staircase lengths: ")
lengths = intput_vales.split(" ")

cost = 0
max_cost = 200

for length in lengths:
    length = float(length)

    if cost + length > max_cost:
        print("Too expensive to continue!")
        break
    else:
        t.forward(length)
        cost += length

    t.left(90)

    if cost + 30 > max_cost:
        print("Too expensive to continue!")
        break
    else:
        t.forward(30)
        cost += 30

    t.right(90)

print("The staircase costs $" + str(cost))
```

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/example4%20part3.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/functions.md)
