### If statements

Now let's add on to the previous program we made. Imagine that we wanted to put a maximum limit on the size of the triangle that is drawn. Let's say we don't want the side length of the triangle exceeding 200. If the side length (based on user input) is greater than 200, the program notifies the user that the triangle is too big and doesn't do anything.

In order to modify the program, we need to consider two scenarios. After the user inputs a number (and after it is multiplied by two), it might be greater than the maximum limit or not. We need a way to change how the program runs depending on what the value of the `side_length` variable is.

Any time you have a scenario where the execution of the program varies depending on certain conditions, you use what's called an **if statement**, like this:

```python
if side_length > 200:
    print("Sorry, the side length is too big")
```

The if statement works as you would expect: if something is true, then do this. In this particular case, the program checks to see whether `side_length` is greater than 200, and if it is, it executes whatever is inside the if statement.

But this still doesn't solve our problem. We successfully managed to print an error message if `side_length` ends up greater than 200, but the program will still continue on afterwards and draw the triangle anyway. We only want the triangle to be draw if the conditional statement fails.

The solution is writing `else`:

```python
if side_length > 200:
    print("Sorry, the side length is too big")
else:
    # run the rest of the program
    t.forward(side_length)
    t.left(120)
    t.forward(side_length)
    t.left(120)
    t.forward(side_length)
```

In an *if else statement*, the if condition is evaluated to see if it's true or not. If it is true, whatever inside the if statement is run. Otherwise if the statement is false, it runs whatever is inside the else statement. By putting ther rest of the program in the else statement, it only gets run if `side_length > 200` is false. 

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/ifelse.PNG" width="480">

But now say we wanted to add more conditions. For example, what if also added in a rule that said that triangles can have a minimum size of 20? So if the side length is less than 20, it isn't drawn. We can add to if statements to make them take more conditions. 

```python
if side_length > 200:
    print("Sorry, the side length is too big")
elif side_length < 20:
    print("Sorry, the side length is too small")
else:
    # run the rest of the program
    t.forward(side_length)
    t.left(120)
    t.forward(side_length)
    t.left(120)
    t.forward(side_length)
```

In between an if and else clause, we can include as many `elif` conditionals as possible, which stand for "else if". 

This program basically reads: if the side length is greater than 200, print an error message. Otherwise, if the side length is less than 20, print an error message. Otherwise, if no above condition is met, then execute the rest of the program.

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/ifelif.PNG" width="480">


# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/example1.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/example2.md)
