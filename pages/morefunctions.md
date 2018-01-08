### Functions Continued

Now, what if we wanted to draw the same shape pattern as before, but have each shape be a different size? Let's say, in order, the side lengths of the shapes are 50, 100, 75, 150, 50, and 25.



We can't use the functions we defined earlier anymore, since now we're not repeating the exact same code anymore. What we could do is change the `side_length` variable before every function call, but that would get pretty messy.

If you remember, with other functions we looked at before, like `forward()` or `left()`, we could pass in a value into the parenthesis. This would determine how the function behaved. We can do the same with our function definition:

```python
def draw_square(length):
    t.forward(length)
    t.left(90)
```

We include what's called a **parameter** into the function. When you call your own function later, you have to pass in a value, like `draw_square(50)`. This value then becomes the `length` variable that's used inside the function. Defining functions with parameters allows you to make the function behave differently every time you call it, so you can use it in situations like here where you need to repeat similar, but not identical bits of code.

We also need to redefine our `draw_triangle()` and `move_on_to_next_shape()` functions:

```python
def draw_triangle(length):
    t.forward(length)
    t.left(120)

def move_on_to_next_shape(length):
    t.penup()
    t.forward(length + 50)
    t.pendown()
```

Now, when we call the functions in our code, we can specify each time what side length we want to draw:

```python
draw_square(50)
move_to_next_shape(50)

draw_square(100)
move_to_next_shape(100)

draw_triangle(75)
move_to_next_shape(75)

draw_triangle(150)
move_to_next_shape(150)

draw_square(50)
move_to_next_shape(50)

draw_triangle(25)
```

Imagine if we didn't have functions, we would have to write out everything using only turtle commands and it would be very unorganized.

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/functions.md) | [Next >]()
