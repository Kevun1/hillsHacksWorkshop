### Lists (arrays)

Before we go forward, let's understand a bit better how turtle works. You can actually think of the screen that the turtle moves on as a standard coordinate plane, with the starting point of the turtle as the origin.

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/coordplane.PNG" width="360">

There's actually a function for turtle that allows it to go to a specific coordinate: 

```python
t.goto(30, 40)
t.goto(60, -40)
t.goto(0, 0)
t.goto(-99.1, 0)
```

If you treat the screen like a coordinate plane, you can tell the turtle to travel in a straight line to a particular coordinate point using the `goto` function. 

Try making a square only using `goto`:

```python
t.goto(50, 0)
t.goto(50,50)
t.goto(0, 50)
t.goto(0, 0)
```

Arrow:

```python
t.goto(50, 0)
t.goto(25, 25)
t.goto(50, 0)
t.goto(25, -25)
```



