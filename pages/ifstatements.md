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

This program basically reads: if the side length is greater than 200, print an error message. Otherwise, if the side length is less than 20, print a different error message. Otherwise, if no above condition is met, then execute the rest of the program.

<img src="https://github.com/Kevun1/hillsHacksWorkshop/blob/master/images/ifelif.PNG" width="480">

However, if we didn't have different error messages for the cases where the side length is too big or too small, we would write the code a little bit differently.

```python
if side_length > 200 or side_length < 20:
    print("Sorry, the side length is not valid")
else:
    #run the rest of the program
```

Notice that in if statements, we can use phrases like `or`. This basically combines two conditionals into one if statement. If one of the conditions *or* the other one is true, then the inside is executed. This makes sense if two or more conditionals trigger the same code. 

We can also link two conditionals together with `and`, which makes the if statement true only if both are true. While it doesn't apply to this example, this is used in many places. For example, create a new file and try this program, tweaking the values of `x` and `y` to understand what it does:

```python
x = 5
y = 10

if x > 2 and y < 12:
    print("These conditions are both correct")
else:
    print("One or more of these conditions are false")
```

In python, code appears almost exactly like how you would say it in person, and that's what you should remember. This is how you should remember if statements. Try to describe what you are trying to do in english, and often you can translate it pretty easily into code. Whenever you say something like "if this happens, then do this", you should use an if statement. Likewise, if you ever find yourself saying "if this or that happens, then do something" or "if this and that both happen, then do something", it's pretty clear what you should do in code.

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/example1.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/example2.md)
