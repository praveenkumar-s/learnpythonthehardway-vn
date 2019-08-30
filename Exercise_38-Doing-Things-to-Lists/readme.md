In the previous lessons you learned about lists. Use the while loop to add the segments to the list and print them out. You can return to previous posts to review

In the previous lesson, we already knew the * append * function to add elements to a list. However, maybe you do not fully understand how append works with the list, the example below will show you more clearly that.

When you write mystuff.append('hello') you are actually setting off a chain of events inside Python to cause something to happen to the mystuff list. Đây là cách nó hoạt động

1. Python sees you referring to the mystuff variable. Notice that after we assign "=", it is a function parameter, or a global variable. 2. Python notices a "." and look at the variables that are part of mystuff 3. Then the mystuff list will find all the functions it handles. If append is included, append is used 4. Python calls the function and inserts parameters into it.   5. Python actually calls append (mystuff, hello) rather than the function. mystuff.append ('hello')





For the most part you don't need to know that this is happening, but it helps when you get error messages from Python like this:

```sh
$ python
Python 2.6.5 (r265:79063, Apr 16 2010, 13:57:41)
[GCC 4.4.3] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> class Thing(object):
...     def test(hi):
...             print "hi"
...
>>> a = Thing()
>>> a.test("hello")
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: test() takes exactly 1 argument (2 given)
>>>


```

Looking at the code above, we have called the test function in the Thing class, but the command output to the screen in the function has not been run. Error message * test () takes exactly 1 argument. meanwhile we give 2 arguments, so OpenStack will replace a.test ("hello") with test (a, "hello")


We consider the exercise below

```sh
ten_things = "Apples Oranges Crows Telephone Light Sugar"

print "Wait there are not 10 things in that list. Let's fix that."

stuff = ten_things.split(' ')
more_stuff = ["Day", "Night", "Song", "Frisbee", "Corn", "Banana", "Girl", "Boy"]

while len(stuff) != 10:
    next_one = more_stuff.pop()
    print "Adding: ", next_one
    stuff.append(next_one)
    print "There are %d items now." % len(stuff)

print "There we go: ", stuff

print "Let's do some things with stuff."

print stuff[1]
print stuff[-1] # whoa! fancy
print stuff.pop()
print ' '.join(stuff) # what? cool!
print '#'.join(stuff[3:5]) # super stellar!
```

##What would you see

Running the above program we will see 
```sh
$ python ex38.py
Wait there are not 10 things in that list. Let's fix that.
Adding:  Boy
There are 7 items now.
Adding:  Girl
There are 8 items now.
Adding:  Banana
There are 9 items now.
Adding:  Corn
There are 10 items now.
There we go:  ['Apples', 'Oranges', 'Crows', 'Telephone', 'Light', 'Sugar', 'Boy', 'Girl', 'Banana', 'Corn']
Let's do some things with stuff.
Oranges
Corn
Corn
Apples Oranges Crows Telephone Light Sugar Boy Girl Banana
Telephone#Light
```

## What list can do

Now create a game based on GoFish. If you do not know GoFish, please take some time to consult on the internet. What you have to do is create different scripts and put them into the Python program. List is one of the most common data structures that programmers use. Simply the ordinal number of the events you want to store and random or linear access by index. What is that about?



##When to Use Lists

You use a list whenever you have something that fits the list's useful data structure features.

1. If you need to maintain order. Remember, this is listed in order, not sorted. The list does not sort for you 2. If you need access to the content by a random number. Remember, this is using a count starting at 0 3. If you need to go from start to finish, the for loop will be used.



## Study Drills

1. Each fuction in Python shows the steps that Python calls them, using more_stuff.pop () as pop (more_stuff) 2. Translate two ways to see functions. For example more_stuff.pop () reads as "Call * pop * on * more_stuff * . Meanwhile pop (more_stuff) calls * pop * function with the parameter * more_stuff * and how the two ways are similar 3. Reading object-oriented programming online 4. Reading classes in Python Not reading class history documents of other languages, it just makes you lie .



If you find it difficult to object-oriented programming, do not worry, try functional programming 6. Find 10 examples of what you find in reality and fill in the list. and write scripts to work with them


## Common Student Questions
Q: What role does [3: 5] play?

Answer: The above function retrieves element 3 and element 4 in stuff, does not retrieve the fifth element
