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

***

##### Exercise 1

Tell people to make a staircase, like this:

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

***

This seems pretty simple so far, but from these basic commands -------

##### Exercise 2

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

That seems rather repetitive, doesn't it? Notice that it's just the same bit of code repeated four times. Namely:

```python
t.forward(50)
t.left(90)
```

However, there's a shorter way to express that than just repeating it over and over again. In IDLE, type

```python
for i in range(4):
    t.forward(50)
    t.left(90)
```

*Tell people to follow along and type it out before explaining. Make sure to note the indents (1 tab or 4 spaces) and the colon, or else they'll get a syntax error. IDLE automatically indents for you, but not every editor will do it automatically*

### The For Loop

What you just typed was called a **for loop**. Basically, a loop is when a bit of code is repeated multiple times. What you coded basically functions like this:

```python
repeat 4 times:
    t.forward(50)
    t.left(90)
```

However, instead of repeat 4 times, you have to type `for i in range(4):`

*The exact syntax of the for loop will be deconstructed a bit later*

So, when do you use a for loop? Whenever you are typing the same code over and over again in a row. 

Here's another application. Back to the staircase example, what if you wanted to make the staircase longer? Remember, with two "stairs" the code was like this:

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

But if you look closer, this code is actually repeated:

```python
t.left(90)
t.forward(50)
t.right(90)
t.forward(50)
```

This code creates one "step" on the staircase. If you wanted a longer stair case, it would just mean more steps, meaning just repeating that piece of code over and over again. This is when the for loop comes in. So, for 5 steps in the staircase, the code is:

```python
for i in range(5):
    t.left(90)
    t.forward(50)
    t.right(90)
    t.forward(50)
```

Notice how much longer it would be if you had to write that out five times over. 





