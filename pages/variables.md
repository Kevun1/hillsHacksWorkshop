
### Variables and Other Basics

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

Variables in Python can be named anything, as long as it starts with a underscore or letter and contains only letters numbers and underscores. So variables can contain numbers as long as they don't start with them, and they can't have symbols in them. They are also case sensitive.

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

But remember that variables are also used to give random values meaning and make code more readable. `x` hardly makes any more sense than `50`. It's a poor choice for a variable name. A better variable name would be:

```python
side_length = 50

t.forward(side_length)

[...]
```

##### Printing and Strings

Before we get back to turtle, there's a few important things we need to know in order to move forward.

Now say you're writing or testing some code. How do you check what the value of a variable is at any given time? After all, it's variable, so it can change any time during the execution of a program. 

You can print it to the screen like this:

```python
some_variable = 1234
print(some_variable)
```

Now you don't have to just print variables. You can print text, like this:

```python
print("Hello, here is some text")
```

The quotation marks are important and required, they signify that what's inside them should be understood as literal text, rather than variables. So if you said `print(Hello)` without quotation marks, the computer would think that you are refering to a variable called `Hello` rather than literal text.

Literal text in python, inclosed in quotations, are known as **strings**, short for *string of characters*. You can do things like assign them to variables. For example,

```python
string = "This is a string"
print(string)
```

You can print multiple strings on one line by *concatenating*, or attaching them together, them using the `+` operator:

```python
string1 = "Hello "
string2 = "World"
print(string1 + string2)
print("Hi " + string2)
```

Note that strings are distinct from numbers, which we have been working with so far. If you tried this, it wouldn't work:

```python
distance = "asdf"
t.forward(distance)
```

Note strings can contain numbers in them, but that doesn't make it an actual number. For example, this is an error:


```python
distance = "6"
t.forward(distance)
```

This is because if you enclose `6` in quotes, it becomes a string, and the computer interprets it as text, not the number 6. 

In regards to printing numbers and strings together, you have to convert numbers into strings. Which you can do by putting a number inside a `str()` function. For example,

```python
some_number = 24
print("My number is " + str(some_number)
```

However, if you are printing a number by itself, like we did earlier when we printed `some_variable`, python automatically converts it to a string.

*Do some more examples to make sure there is no confusion*

##### Modifying Variables

It's important to know how a variable can be modified. After all, the definition of a variable is that it can change.

First, as we have seen, we can assign variables using the `=` operator. Once a variable is assigned, we can change it's value simply by assigning to a new value.

```python
x = 6
print(x)
x = 10
print(x)
```

We can increment numbers like this

```python
x = 0
x = x + 15
print(x)
```

This sets `x` to 0 at first, then increments it by 15. However, there is a shortcut:

```python
x = 0
x += 15
print(x)
```

This code is the same as the previous example. `variable += some_value` is the same as `variable = variable + some_value` which basically increments `variable` by `some value`. 

You can do the same with all other mathematical operations, like subtraction, multiplication, and division.

```python
x = 2
x *= 4
print(x)

y = 4
y /= 2
print(y)

z = 12
z -= 4
print(z)
```

##### Comments

Sometimes when coding, you want to write little notes to yourself, maybe to describe what a piece of code does. You do that by writing a **comment**, which is basically any note to yourself that doesn't actually get run by the computer. Like this:

```python
# this sets the variable x to 5
x = 5

# putting a # in front of a line makes it not get executed
```

Writing comments can help you keep track of what your code is doing.

***

This is a lot of info, but we are going to apply all of it using turtle to do some more advanced things than draw simple shapes.

***

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/README.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/forloop.md)
