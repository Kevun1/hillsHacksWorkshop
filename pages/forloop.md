
### The For Loop

Let's revisit the square we made at the very beggining.

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

Looking at it again, that seems rather repetitive, doesn't it? Notice that it's just the same bit of code repeated four times. Namely:

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

What you just typed was called a **for loop**. Basically, a loop is when a bit of code is repeated multiple times. What you coded basically functions like this:

```python
repeat 4 times:
    t.forward(50)
    t.left(90)
```

However, instead of repeat 4 times, you have to type `for i in range(4):` 

The for loop is actually more useful than repeating consequtive bits of code. However, we'll get to that a bit later.

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

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/forloop.md) | [Next >]()
