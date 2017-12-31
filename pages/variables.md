
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

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/README.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/forloop.md)
