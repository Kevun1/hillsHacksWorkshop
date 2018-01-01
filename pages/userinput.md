### User Input

Often, programs are going to interact with someone. 

Let's create a turtle program that asks the user for a number, and then moves forward by that amount. We can do that by using the `input()` function like this:

```python
distance = input("How far should the turtle move? ")
distance = int(distance)
t.forward(distance)
```

`input()` brings up a prompt to the user asking them to type something in, which can then be assigned to a variable. Notice however, that we needed to convert the input into a number first. This is because `input()` interprets user input as strings, literal text.

Note that in this case, you are both the programmer and the "user," but you can imagine in an actual program it's important for other people to be able to control how the program runs.

# [< Prev](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/variables.md) | [Next >](https://github.com/Kevun1/hillsHacksWorkshop/blob/master/pages/example1.md)
