# Exercise 5: More Variables and Printing

## I. For example
In the previous lessons, you learned how to print a string on a screen.

n this lesson we can learn how to create a string and attach a variable to it. In this article we will use a concept of format string.

I have the following code:

```sh
# -*- coding: utf-8 -*-
my_name = 'Zed A. Shaw'
my_age = 35 # not a lie
my_height = 74 # inches
my_weight = 180 # lbs
my_eyes = 'Blue'
my_teeth = 'White'
my_hair = 'Brown'

print "Let's talk about %s." % my_name
print "He's %d inches tall." % my_height
print "He's %d pounds heavy." % my_weight
print "Actually that's not too heavy."
print "He's got %s eyes and %s hair." % (my_eyes, my_hair)
print "His teeth are usually %s depending on the coffee." % my_teeth

# this line is tricky, try to get it exactly right
print "If I add %d, %d, and %d I get %d." % (
my_age, my_height, my_weight, my_age + my_height + my_weight)
```

## II. Output of the above code

<img src=http://i.imgur.com/4QdLBd4.png width="60%" height="60%" border="1">


Explain the code a bit:

From lines 2 to 8 is the variable declaration.

Starting from line 10 onwards, we will see% s or% d in the printout, but this parameter is a format string whose purpose is to include the variable in the string. After the end of a string, it will be% of the transfer name. If there are multiple format strings in your string, you can pass the variable with the following syntax:% (namename, name2, ...)

You can use this %rto replace characters %sand %d. Try it and see what happens.

%s used to replace string.

%d used to replace numbers

%r You guessed yourself :blush:


