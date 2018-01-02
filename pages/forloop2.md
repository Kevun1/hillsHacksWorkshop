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



