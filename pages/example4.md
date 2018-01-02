### Example 4

Here's an example to apply the for loop. 

Consider the staircase we constructed earlier:


In our staircase 





```python
from turtle import *
t = Turtle()

lengths = [1, 4, 2]

for length in lengths:
    t.forward(length)
    t.left(90)
```
