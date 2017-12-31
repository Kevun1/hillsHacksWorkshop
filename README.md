# hillsHacksWorkshop

*This document is for mentors conducting the workshop.*

*Regular/bold text is what you tell people, italicized text are notes to yourself.*

### Introduction

Introduce yourself, say this workshop is for beginners who have little or no experience with computer programming.

What is programming

What you'll learn in this workshop



##### Installation

Go to this URL: https://www.python.org/downloads/, and click on "Download Python 3.6.4" Make sure it's Python 3 and not Python 2. Even if people already have Python, tell them to do it anyway to make sure everyone is using the same version.

Open the downloaded file, and then click next at every step.

The program people should open is called "IDLE," which should've been automatically downloaded

Type these two lines into IDLE. *No explanation is needed yet, tell everyone this is just part of the setup in order to begin.*
```python
from turtle import *
t = Turtle()
```
This should open up a window.


***Open up IDLE and project it onto the board. Every time there is a code snippet, type it out yourself so it is projected on the board, so other people can follow***

***

##### *General notes for IDLE:*

- *A bunch of red text means an error*

- *If a command doesn't finish executing (for example, with a infinite loop), you can use CTRL+C to break out of it (for Windows, at least). Alternatively, restart IDLE, and retype the two lines above to open the turtle window again*

- *If someone exits out of the turtle window, they will have to restart IDLE and retype the above two lines. Otherwise, if they attempt to create a new window, they'll get a bunch of errors*

***

---introduce turtle------------------------------------

### Turtle Basics

- `forward()`, `back()`
- `reset()`
- `left()`,`right()`

`forward(amount)` moves the turtle in the direction it's facing by `amount` pixels.

`back(amount)` moves the turtle in the direction away it's facing from by `amount` pixels.

`reset()` resets everything to the original state.

*Note that these are methods, so you have to call them on the `Turtle` object. So you have to type `t.forward(...)` Don't explain to people what methods are yet, just tell them that's the way to type the commands. Also, if the turtle moves off the screen, that means the number is too big*

Show examples of commands

`left(angle)` turns the turtle left by `angle`. 

`right(angle)` turns the turtle right by `angle`.

*Note, these are with respect to the turtle's original facing direction*

Show examples of commands

This seems pretty simple so far, but from these basic commands -------

***

##### Exercises

Make a staircase, like this:

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/staircase.PNG" width="360">

*\(show the image to everyone)*

The solution is:

```python
t.left(90)
t.forward(50)
t.right(90)
t.forward(50)
t.left(90)
t.forward(50)
t.right(90)
t.forward(50)
```

*Note: The 50 is the length of each segment, which can be replaced with any number*


Now, make a square, like this (make sure to do `t.reset()`!):

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/square.PNG" width="360">

The solution is:

```python
t.forward(50)
t.left(90)
t.forward(50)
t.left(90)
t.forward(50)
t.left(90)
t.forward(50)
t.left(90)
```

Note that there are multiple ways to do this. For example, you could've turned left at the beginning and have drawn the square clockwise. Often with programming, there are many ways to do the same problem. 

Finally, make an arrow, like this:

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/arrow.PNG" width="360">

The solution is:

```python
t.forward(50)
t.left(90+45)
t.forward(25)
t.back(25)
t.left(90)
t.forward(25)
```

Note: there are even more ways to have draw this arrow. This was just one possible solution

### Variables

So far, in these examples I've been using 50 as the "standard" length of a segment. But what if I wanted to draw a square with side lengths of 100 or 6 or 512.3? Of course, I would just change out the 50 for some other number. This is fine in IDLE, where each statement you type is executed immediately, but usually, programmers write out multiple lines in a file and then execute everything at once. So if you had code like:

```python
t.forward(50)
t.left(90)
t.forward(50)
t.left(90)
t.forward(50)
t.left(90)
t.forward(50)
t.left(90)
```

and you wanted to change the 50 to another number, you would have to go to each instance where there is a 50 and replace it with a different number. In an actual program, there could be hundreds of different instances that you would have to replace. Furthermore, it's not clear what the number "50" represents in isolation. Sure, this particular code is simple and you can tell it's the side length of a square, but you can imagine if you're looking at a full computer program and you see the number 50 randomly in there, you can't tell what it does. That makes editing your program very difficult.

The solution is something called variables. In IDLE, type

```python
x = 50
t.forward(x)
```



***

[# Next](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/forloop.md)

