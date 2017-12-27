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

Type these two lines into IDLE. 
```python
from turtle import *
t = Turtle()
```
This should open up a window.

*No explanation is needed yet, tell everyone this is just part of the setup in order to begin.*

##### *General notes for IDLE:*

- *A bunch of red text means an error*

- *If a command doesn't finish executing (for example, with a infinite loop), you can use CTRL+C to break out of it*

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

##### First Exercise

Tell people to make a staircase, like this:





