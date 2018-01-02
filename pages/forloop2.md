### For Loop and Lists

The for loop is actually far more useful than repeating the exact same piece of code over and over. Often times, when you repeat code, you want slightly different results each time. 

For example, let's say you wanted to make an app to keep track of your homework. When you tell it to, it tells you all of the classes in which you have homework in. It might go something like this:

```python
print("You have homework in biology")
print("You have homework in english")
print("You have homework in history")
print("You have homework in math")
print("You have homework in computer science")
```

Writing this, you might think, "hey, that looks very repetitive, I could probably use a for loop." This is correct, but notice that you aren't repeating the exact same thing each time. You can't just do this:

```python
for i in range(5):
    print("You have homework in ") # what goes here? It changes each time
```

However, you can do this:

```python
subjects_with_homework = ["biology", "english", "history", "math", "computer science"]
for subject in subjects_with_homework:
    print("You have homework in " + subject)
```

Let's break this down.

First, I created what in python is known as a *list*. It's like what it sounds like: a list of elements. They are a bunch of things, (whether strings or numbers or anything else) grouped together. A list can be assigned to a variable, can be however long you want, and has a set order. Basically, it's a *sequence of elements*. 

Before, we said the for loop was for repeating code. That's a slight simplification. Actually, a for loop runs code once for each element in a sequence.

```python
list1 = [1, 2, 3, 4]
for i in list1:
    print(i)

for some_variable in ["a", "b", "c"]:
    print(some_variable)
    
list3 = [1, "asdf", 55.4, "random string", -39423]
for xyz in list3:
    print(xyz)
```

A for loop basically goes through each element in a sequence (which can be a list), sets it equal to a variable it keeps track of, and runs its block of code. So in our above example, the for loop repeats the code `print("You have homework in " + subject)` for every element in the list `subjects_with_homework`, which it assigns to the variable `subject`. 

When we did `for i in range(x):`, the `range(x)` is actually a shorthand notation for a sequence of numbers that's `x` numbers long, making the loop repeat `x` times. 

```python
for i in range(15):
    print(i)
```

As you can see, `i` is actually a variable that you can use inside the loop, and it cycles through each element in the `range` every loop. 










