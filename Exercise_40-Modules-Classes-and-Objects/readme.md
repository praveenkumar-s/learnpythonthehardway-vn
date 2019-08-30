
##  40: Modules, Classes, and Objects

Python is called an "object-oriented programming language." Use classes in programming to make the program clearer. Now I will show you the beginning steps of object-oriented programming, classes, objects and modules.

## Modules are like Dictionaries

You have learned that a dictionary is created and used to map between key and value. That means if you created a key that is "apple" and you want to retrieve the content that key contains, do the following:
```sh
mystuff = {'apple': "I AM APPLES!"}
print mystuff['apple']```


Keep the "get X from Y" thought in your mind and now think about the module. I temporarily define it as

1. A Python file with functions or functions in it 2. You import files 3. You can access functions or variables in a module with dots



Suppose you have a module named mystuff.py and have funtion * apple * . Module content * mystuff.py *

```sh
# this goes in mystuff.py
def apple():
    print "I AM APPLES!"```

In your program, you can use the MyStuff module with the * import * function and then access the funtion * apple * :

```sh
import mystuff
mystuff.apple()```


You can also add a variable named * tangerine * :
```sh
def apple():
    print "I AM APPLES!"# this is just a variabletangerine = "Living reflection of a dream"```




and access variables
```sh
import mystuffmystuff.apple()print mystuff.tangerine```




Recall the dictionary and you'll start to see it uses almost the same dictionary but only has different syntax. Compare:
```sh
mystuff['apple'] # get apple from dict
mystuff.apple() # get apple from the module
mystuff.tangerine # same thing, it's just a variable```

This means we have a very common type in Python:

1. create a key = value 2. Retrieve the content by the name of the key


In dictionary, key is string and syntax is [key]. In the module, the key and sign and the syntax is .key. They are almost similar

## Class is like a module

You can think of a module as a specialized dictionary that can store Python code so you can access it with dots. Python also has a structure that serves a similar purpose called classes. A class is a way to have a group of functions and data placed on them so you can access them via dots.

If you create a class as a module mystuff. You do the following
```sh
class MyStuff(object):    def __init__(self):        self.tangerine = "And now a thousand years between"    def apple(self):        print "I AM CLASSY APPLES!"```







Perhaps here you will wonder how to use the MyStuff class instead of the mystuff module with the apple function . You also find it confusing with the __ init __ function as well as how to declare the variable self.tangerine. You should also know about objects and how objects work with mystuff



## Object as Import

If the class is considered a mini-module. When we import a class and create a new one, it is called an instance. An instance is called by the class function as follows

```sh
thing = MyStuff()
thing.apple()
print thing.tangerine```

We consider the components that make up the MyStuff class

1. Call MyStuff () to see that it is a class that has been defined. 2. Python initializes an empty object with all the internal features using * def * 3. The __ init_ __ function calls the function to initialize the newly created empty object. 4. In the __ init __ function, the variable * seft * is an empty Python object for me, and I can set variables on it just like you would with a module, dictionary, or other object 5. In the above case * self.tanger * is a variable 6. Now Python can include this object as a variable *





thing*

## Getting things from things

Now we have three ways to get the value from the key
```sh
# dict style
mystuff['apples']# module stylemystuff.apples()print mystuff.tangerine# class stylething = MyStuff()thing.apples()print thing.tangerine```










## Class example

You will probably see the similarity of the three key = value declarations and have questions
```sh
class Song(object):    def __init__(self, lyrics):        self.lyrics = lyrics    def sing_me_a_song(self):        for line in self.lyrics:            print linehappy_bday = Song(["Happy birthday to you",                   "I don't want to get sued",                   "So I'll stop right there"])bulls_on_parade = Song(["They rally around tha family",                        "With pockets full of shells"])happy_bday.sing_me_a_song()bulls_on_parade.sing_me_a_song()```



















## What you see
```sh
$ python ex40.py
Happy birthday to you
I don't want to get sued
So I'll stop right there
They rally around tha family
With pockets full of shells```

## Learn more

1. write a few songs and print out the lyrics 2. Put the lyrics in a separate variable, then pass that variable to the class to use 3. Learn online about object-oriented programming



## Some general questions

Q. Using seft in __ init __ function

Answer: * seft * means itself. When initializing an instance we will pass this object to seft. for example * thing = mystuff () * and using variable * thing.cheese * then map with seft.cheese in the class declaration

