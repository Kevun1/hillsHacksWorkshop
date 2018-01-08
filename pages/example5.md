### Example 5

Let's finish up the example we've been using to demonstrate functions. We can now draw any given pattern of shapes, so let's write a generalized program that draws a pattern of  squares and triangles based on user input. 

The input will be a sequence of words, either "square" or "triangle", and then the turtle has to draw those shapes in that order. The size of the first shape will be 10, and the size will increase by 10 every shape afterwards. The spacing between each shape should be 20.

So, for example, if the input was "square triangle triangle triangle square triangle square square", the turtle should draw this:

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/squaretrianglepattern4.PNG" width="480">

There are two main ways to go about doing this. The first, which is what most of you likely have done, is like this:

```python
from turtle import *
t = Turtle()
# to give us some room
t.penup()
t.back(350)
t.pendown()

spacing = 20
initial_size = 10
increment_size = 10

def draw_square(length):
    for i in range(4):
      t.forward(length)
      t.left(90)
      
def draw_triangle(length):
    for i in range(3):
        t.forward(length)
        t.left(120)
        
def move_to_next_shape(length):
    t.penup()
    t.forward(length)
    t.pendown()

user_input = input("Enter a sequence of shapes: ")
pattern = user_input.split(" ")

count = 0
for shape in pattern:
    if shape == "square":
        draw_square(initial_size + count*increment_size)
        move_to_next_shape(size + spacing)
    elif shape == "triangle":
        draw_triangle(initial_size + count*increment_size)
        move_to_next_shape(size + spacing)
    else:
        print("Not a recognized shape: " + shape)
    count += 1
```

User input is split by spaces into an array and then iterated over in a for loop (like in the previous example). Now, we include an if statement inside to determine which shape to draw, and then which function to call (The last else statement is optional, I just wanted to print out an error message if the user input contained something wrong). A `count` variable keeps track of what number in the sequence we're in, as the size of the shape is dependent on that. 

A second way of doing this is to define another function entirely, this time with two parameters. We can define and call functions with multiple parameters simply by separating them with commas:

```python
from turtle import *
t = Turtle()
# to give us some room
t.penup()
t.back(350)
t.pendown()

spacing = 20
initial_size = 10
increment_size = 10

def draw_square(length):
    for i in range(4):
      t.forward(length)
      t.left(90)
      
def draw_triangle(length):
    for i in range(3):
        t.forward(length)
        t.left(120)
        
def move_to_next_shape(length):
    t.penup()
    t.forward(length)
    t.pendown()

def draw_shape(shape, size):
    if shape == "square":
        draw_square(size)
        move_to_next_shape(size + spacing)
    elif shape == "triangle":
        draw_triangle(size)
        move_to_next_shape(size + spacing)
    else:
        print("not recognized shape")

user_input = input("Enter a sequence of shapes: ")
pattern = user_input.split(" ")

count = 0
for shape in pattern:
    draw_shape(shape, initial_size + count*increment_size)
    count += 1
```

This does the exact same thing, but instead of doing the stuff in the for loop, it replaces it with a function. Now, for this example, there is no need to define another function, since we only that bit of code once. But, when writing a longer program, you might need to do reuse a bit of code again, and drawing a shape based on a string seems like something that would come in handy if I was creating a more complicated drawing. 

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/functions2.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/challenge.md)
