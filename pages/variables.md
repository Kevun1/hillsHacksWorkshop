
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

In this case, `x` is a variable. Variables basically stand in for some kind of value. In this case, `x` stands in for 50, so every time you type `x` in your code, it really stands for 50. 

But you don't have to call it `x`. You can call it whatever you want, with some constraints. For example:

```python
y = 500
t.back(y)

asdf = 33.2
t.right(asdf)

this_is_a_variable = 9999
t.left(this_is_a_variable)

numbers123 = 55
t.forward(numbers123)
```

Variables in Python can be named anything, as long as it starts with a underscore or letter and contains only letters numbers and underscores. So variables can contain numbers as long as they don't start with them, and they can't have symbols in them.

So why use variables again?

Well, you can now rewrite the square code like this:


```python
x = 50

t.forward(x)
t.left(90)
t.forward(x)
t.left(90)
t.forward(x)
t.left(90)
t.forward(x)
t.left(90)
```

So now if you instead want to have a square that is of side length 100, all you have to do is type

```python
x = 100
```

and the rest of the code automatically updates. No need for changing numbers in four different places. Of course again, in IDLE, since statements are executed line by line only once, you do actually have to type everything out again but if this were a single document, like code is usually in, you wouldn't have to do so.



***

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/README.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/forloop.md)
