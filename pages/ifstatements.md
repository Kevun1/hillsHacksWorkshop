
### If statements

Now, let's apply everything we learned so far to create another turtle program. Let's design a program where a user can specify a direction, like north, south, east, or west, and then the turtle draws an arrow in that direction. 

First, we need to get user input of what direction they want the turtle to draw in. 

```python
direction = input("What direction would you like to go in? ")
```

This prompts the user for a direction, which is then stored in the `direction` variable.

Now, what do we do? We already know how to draw an arrow, but depending on how the user responds, the program is going to behave differently, since the code of drawing the arrow is different depending on what direction we want it. 

If the user types in north, we want to draw an arrow facing north. If the user types in south, we want to draw an arrow facing south. And so on. Alternatively, we also have to account for the situation where the user might type in some nonsense that's not a direction at all. 

Whenever you have a situation, like this, when the execution of a program can go multiple paths depending on the situation, we use an **if statement**. 

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/userinput.md) | [Next >]()
