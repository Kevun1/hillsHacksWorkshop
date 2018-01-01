### Example 2

Again, let's apply everything we learned to a new problem.

Let's design a program where a user can specify a direction, like north, south, east, or west, and then the turtle draws an arrow in that direction. 

First, we need to get user input of what direction they want the turtle to draw in. 

```python
direction = input("What direction would you like to go in? ")
```

This prompts the user for a direction, which is then stored in the `direction` variable.

Now, what do we do? We already know how to draw an arrow, but depending on how the user responds, the program is going to behave differently, since the code of drawing the arrow is different depending on what direction we want it. 

If the user types in north, we want to draw an arrow facing north. If the user types in south, we want to draw an arrow facing south. And so on. Alternatively, we also have to account for the situation where the user might type in some nonsense that's not a direction at all. 

Whenever you have a situation, like this, when the execution of a program can go multiple paths depending on the situation, we use an if statement. It's basically a direct translation of what we described above into code.

```python
if direction == "north":
    #draw north facing arrow
    t.left(90)
    t.forward(50)
    t.left(90 + 45)
    t.forward(25)
    t.back(25)
    t.left(90)
    t.forward(25)
```

So this code translates to: if the `direction` variable (which refers to the user's input) is equal to `"north"`, then run the code below, which draws an arrow facing north. 

Note that we use two equal signs `==` for equals. This is because one equals sign `=` means variable assignment, when we set a variable equal to some value. It's extremely important that in if statements you use two equals signs, it's a very common mistake to only use one equals sign, which is an error in python. 

Now, we have the north condition settled, we have to account for all the other possible inputs. We can use multiple elif cases:

```python
elif direction == "south":
    #draw south facing arrow
    t.right(90)
    t.forward(50)
    t.left(90 + 45)
    t.forward(25)
    t.back(25)
    t.left(90)
    t.forward(25)
elif direction == "west":
    #draw a west facing arrow
    t.right(180)
    t.forward(50)
    t.left(90 + 45)
    t.forward(25)
    t.back(25)
    t.left(90)
    t.forward(25)
elif direction == "east":
    #draw an east facing arrow
    t.forward(50)
    t.left(90 + 45)
    t.forward(25)
    t.back(25)
    t.left(90)
    t.forward(25)
```

If the user types in `"north"`, `"south"`, `"east"`, and `"west"`, your program will draw the corresponding arrow. But of course, the user might type in something completely random, like `"asd0f92041290af"`. Our program should warn the user that they didn't type in a valid input. So we add a final `else` condition to catch everything else that's not covered by our conditions.

```python
else:
    print("Not a valid direction")
```

A quick sidenote:

Note that comparing string equality is case sensitive, so if the user typed in "North", the program would say it's not valid since it's not equal to "north". To fix this, we can change the user input to all lowercase letters, so that uppercase/lowercase doesn't matter. We can use the `lower()` function to do that, like this:

```python
direction = lower(direction)
```

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/ifstatements.md) | [Next >]()
