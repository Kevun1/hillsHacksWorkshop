### Example 4 continued

Now, while we have met the specifications of one particular stair manufacturer, it's a good idea to make it more general. Imagine an program where anybody can enter a sequence of numbers, and a staircase is constructed with those numbers as the length of each step.

So for example, the program would first prompt me to enter a sequence of values. Let's say I enter "50 30 40 11.5". Now, it constructs a staircase with step lengths 50, 30, 40, and 11.5 (let's keep the height at 30).

In order to make this program, we would need some way to create a list from the user input. The easiest way would be to do it like this:

```python
intput_vales = input("Enter staircase lengths: ")
lengths = intput_vales.split(" ")
print(lengths)
```

The `split()` function splits a string into a list. It determines where to split the string based on a *delimiter* you pass in. In this case, we used " ", which splits the input string by spaces. So think of it like taking a knife and cutting the string wherever you see a space, and then putting the pieces as elements into a list. 

Now that we have the list of step lengths, the rest of the code looks exactly the same, right? However, if you run it, you will get an error. Something about a TypeError.

The problem is that when the string is split into the list, it doesn't convert each element into numbers. You can't call .forward() with a string.

The solution is to convert elements into a number before moving the turtle, with `float()`. The final code looks like:

```python
from turtle import *
t = Turtle()

intput_vales = input("Enter staircase lengths: ")
lengths = intput_vales.split(" ")

for length in lengths:
    length = float(length)
    t.forward(length)
    t.left(90)
    t.forward(30)
    t.right(90)
```


