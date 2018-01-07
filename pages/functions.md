### More for loops, and Functions

Now, draw this:

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/threesquares.PNG" width="480">

Recall that drawing a square is like this:

```python
for i in range(4):
    t.forward(side_length)
    t.left(90)
```

So drawing three of them in a row is repeating that bit of code 3 times - another for loop. You need a for loop inside a for loop:

```python
side_length = 50
spacing = side_length*2

# repeat three times:
for i in range(3):
    # Draw a square
    for j in range(4):
        t.forward(side_length)
        t.left(90)
        
    # Move forward
    t.penup()
    t.forward(spacing)
    t.pendown()
```

Note that we have to use a different variable in the inner loop because it's taken by the outer loop.

Now try drawing this:

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/squaretrianglepattern1.PNG" width="480">

Again, the solution is to use nested for loops, but this time, there are two for loops inside the overall one, one for the square, and one for the triangel.

```python
# to give us some room
t.penup()
t.back(300)
t.pendown()

side_length = 50
spacing = side_length*2

for i in range(3):
    # draw square
    for j in range(4):
        t.forward(side_length)
        t.left(90)
        
    # Move forward
    t.penup()
    t.forward(spacing)
    t.pendown()
        
     # draw triangle
    for j in range(3):
        t.forward(side_length)
        t.left(120)
        
    # Move forward
    t.penup()
    t.forward(spacing)
    t.pendown()
```

Notice that we can use `j` for both the square and the triangle loops, because they are on the same level. The variable of a for loop is only in use inside the body of the for loop.

Let's add a subtle change to the pattern we want to draw:

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/squaretrianglepattern2.PNG" width="480">

Now what do we do? Try using a for loop.

Suddenly, we can't use a for loop anymore. That's because there is no pattern anymore, so we can't just repeat one pattern over and over again, which is what a for loop does. So now we have to write everything out like this:

```python
# to give us some room
t.penup()
t.back(300)
t.pendown()

side_length = 50
spacing = side_length * 2

# Draw two squares
for i in range(2):
    for i in range(4):
        t.forward(side_length)
        t.left(90)
        
    t.penup()
    t.forward(spacing)
    t.pendown()
    
# Draw two triangles
for i in range(2):
    for i in range(3):
        t.forward(side_length)
        t.left(120)
        
    t.penup()
    t.forward(spacing)
    t.pendown()
    
for i in range(4):
    t.forward(side_length)
    t.left(90)
    
# Move forward
t.penup()
t.forward(spacing)
t.pendown()
    
for i in range(3):
    t.forward(side_length)
    t.left(120)
```

That gets the job done, but it looks nasty - there is a ton of code repetition. If I told you to make it so that the turtle doesn't move it's pen up when moving between shapes, there's several different places you would have to change your shape because the code for moving forward after drawing a shape is scattered everywhere. 

In multiple places, we're repeating the same bits of code, for example drawing a square. We can actually make it so that we only have to write the same bit of code once, and just refer to that each time we need to execute it. We can define a **function** that draws a square:

```python
def draw_square():
    for i in range(4):
      t.forward(side_length)
      t.left(90)
```

Then, when we need to use that bit of code, all we have to type is `draw_square()`. We can call it as many times as we want. So now our code becomes:

```python
# to give us some room
t.penup()
t.back(300)
t.pendown()

side_length = 50
spacing = side_length * 2

def draw_square():
    for i in range(4):
      t.forward(side_length)
      t.left(90)

# Draw two squares
for i in range(2):
    draw_square()
        
    t.penup()
    t.forward(spacing)
    t.pendown()
    
# Draw two triangles
for i in range(2):
    for i in range(3):
        t.forward(side_length)
        t.left(120)
        
    t.penup()
    t.forward(spacing)
    t.pendown()
    
draw_square()
    
# Move forward
t.penup()
t.forward(spacing)
t.pendown()
    
for i in range(3):
    t.forward(side_length)
    t.left(120)
```

which is a bit better. But we can also make functions for drawing a triangle and moving forward with the pen up as well:

```python
# to give us some room
t.penup()
t.back(300)
t.pendown()

side_length = 50
spacing = side_length * 2

def draw_square():
    for i in range(4):
      t.forward(side_length)
      t.left(90)
      
def draw_triangle():
    for i in range(3):
        t.forward(side_length)
        t.left(120)
        
def move_to_next_shape():
    t.penup()
    t.forward(spacing)
    t.pendown()

# Draw two squares
for i in range(2):
    draw_square()
    t.move_to_next_shape()
    
# Draw two triangles
for i in range(2):
    draw_triangle()
    t.move_to_next_shape()
    
draw_square()
t.move_to_next_shape()    
draw_triangle()
```

Now, our code is much better organized and there is minimal repetition. 

We've actually been using functions all the time. For example, `t.forward()` or `t.penup()`. You can tell whether something is a function by whether it has parenthesis or not. One way to think about functions is that they are like variables but instead of standing in for a value, they stand in for a bit of code. After you define a function, you can call it anywhere; when this happens, it's like copy and pasting its definition into where you call it, so that you don't need to retype everything. 

Like variables, defining functions can help you organize your code and keep things in one place. With our latest example, if we wanted to make it so that moving on to the next shape doesn't raise the pen, for example, we just edit the `move_to_next_shape()` definition instead of having to make edits everywhere in the code. 

Note that variables and functions are very different concepts and have different uses, so don't think of them as equivalent, but for the purpose of organizing your code it is a good comparison to make. 

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/example4%20part4.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/morefunctions.md)
