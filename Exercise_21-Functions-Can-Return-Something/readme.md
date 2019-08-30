# Exercise 21: Functions Can Return Something

## For example

You have used the "=" character to name and assign numbers and strings to them. Now we'll give you an idea once again by showing you how to use the "=" character and a new return word to set a value using a function in python.

Script: 

    def add(a, b):
        print "ADDING %d + %d" % (a, b)
        return a + b
    
    def subtract(a, b):
        print "SUBTRACTING %d - %d" % (a, b)
        return a - b
    def multiply(a, b):
        print "MULTIPLYING %d * %d" % (a, b)
        return a * b
    def divide(a, b):
        print "DIVIDING %d / %d" % (a, b)
        return a / b


    print "Let's do some math with just functions!"
    age = add(30, 5)
    height = subtract(78, 4)
    weight = multiply(90, 2)
    iq = divide(100, 2)
    print "Age: %d, Height: %d, Weight: %d, IQ: %d" % (age, height, weight, iq)
    print "Here is a puzzle."
    what = add(age, subtract(height, multiply(weight, divide(iq, 2))))
    print "That becomes: ", what, "Can you do it by hand?"


Guessing the script above makes our mathematical functions. But what's important is that the last line here we say is return a + b

##  code 

    python ex21.py
    Let's do some math with just functions!
    ADDING 30 + 5
    SUBTRACTING 78 - 4
    MULTIPLYING 90 * 2
    DIVIDING 100 / 2
    Age: 35, Height: 74, Weight: 180, IQ: 50
    Here is a puzzle
    DIVIDING 50 / 2
    MULTIPLYING 180 * 25
    SUBTRACTING 74 - 4500 
    ADDING 35 + -4426
    That becomes:  -4391 Can you do it by hand?

## Practice

* If you are not sure about return, try writing some of your functions and return some values * Somewhat, write a simple formula and use functions as a way to calculate


## Question

* Can I use raw_input () to enter my value?     Remember int (raw_input ())? The problem with this is that you cannot type a float, instead use float (raw_input ()).
