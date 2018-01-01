### Example 1

Now, let's apply everything we learned so far into an simple example.

Suppose we wanted to create a user interactive program that can draw a triangle of a variable size. But there's a slight twist for some extra side length: it asks the user for what *half* the size length should be, drawing a triangle twice as large as the user specified. So if the user types in 5, the program will draw a triangle of side length 10. 

For creating this program, we're going to step away from using the console in IDLE as we've been doing so far.

Instead of typing into the screen by the `>>>` marks, click "File" then "New File" at the top left of the window. This opens up a new window where you can type code freely. As alluded to earlier, the difference between this and what you using earlier is that with files, all the code is executed at once, while in the console each line is executed as it is typed in. Typically, programmers are always going to write their programs in files, while the console is used for quickly testing a few things. 

At the top of your file, you will have to type in this heading again:

```python
from turtle import *
t = Turtle()
```

Now, try typing in a few lines of turtle code. Then, once you are done, you can execute it by clicking "Run" then "Run Module" at the menu on the top, or press F5 as a shortcut. You will have to save the file somewhere on your computer first, however.

Back to the problem:

First things first, we need to take in a user input for the triangle side length and store it somewhere. Remember we can do so using the `input()` function and then assigning it to a variable.

```python
# Take in a number 
side_length = input("Please enter a number: ")
```

