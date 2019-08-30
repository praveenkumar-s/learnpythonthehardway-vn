Instead of using the input () function, we use input ("String") to suggest the user to enter

Run the following program
```sh
age = input("How old are you? ")
height = input("How tall are you? ")
weight = input("How much do you weigh? ")

print ("So, you're %r old, %r tall and %r heavy." % (
    age, height, weight))
```
### What You Should See
```sh
>>> ================================ RESTART ================================
>>> 
How old are you? fine
How tall are you? 1m74
How much do you weigh? 68
So, you're 'fine' old, '1m74' tall and '68' heavy.
```
