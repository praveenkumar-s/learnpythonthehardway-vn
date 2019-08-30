Now we will learn an important concept in Python and is often used as "dicts". Some other languages ​​are called "hashes". We tend to use both names but that's not so important . Let's see what the list does



```sh
>>> things = ['a', 'b', 'c', 'd']
>>> print things[1]
b
>>> things[1] = 'z'
>>> print things[1]
z
>>> things
['a', 'z', 'c', 'd']
```
We can use indexes to get items from the list. In case we want to retrieve an object by keyword, the list does not do this, then we need to use dict. With dict, the key is attached to the value. See the example below

```sh
>>> stuff = {'name': 'Zed', 'age': 39, 'height': 6 * 12 + 2}
>>> print stuff['name']
Zed
>>> print stuff['age']
39
>>> print stuff['height']
74
>>> stuff['city'] = "San Francisco"
>>> print stuff['city']
San Francisco
```
You will see instead of using the numbers we use strings when we want to call objects. We can also insert other objects into the dictionary. We can also pass a key as a number



```sh
>>> stuff[1] = "Wow"
>>> stuff[2] = "Neato"
>>> print stuff[1]
Wow
>>> print stuff[2]
Neato
>>> stuff
{'city': 'San Francisco', 2: 'Neato', 'name': 'Zed', 1: 'Wow', 'age': 39, 'height': 74}```

In this code, I use numbers, and then you can see the numbers and string strings as the key in dict when I want to print them out.

You can also delete elements from the dictionary with * del *

```sh
>>> del stuff['city']
>>> del stuff[1]
>>> del stuff[2]
>>> stuff
{'name': 'Zed', 'age': 39, 'height': 74}```## Example for DictionaryNow we will do an exercise that you must pay close attention to. I want you to type in this code and try to understand them. Please note that when you add dict, get a hash function. This example is mapping countries to their abbreviations, and then abbreviations for cities in the states. Remember, "mapping" or "associating" are important concepts in a dictionary.```sh# create a mapping of state to abbreviationstates = {    'Oregon': 'OR',    California: CA,    Florida: FL,













    'New York': 'NY',
    'Michigan': 'MI'
}

# create a basic set of states and some cities in them
cities = {
    'CA': 'San Francisco',
    'MI': 'Detroit',
    'FL': 'Jacksonville'
}

# add some more cities
cities['NY'] = 'New York'
cities['OR'] = 'Portland'

# print out some cities
print '-' * 10
print "NY State has: ", cities['NY']
print "OR State has: ", cities['OR']

# print some states
print '-' * 10
print "Michigan's abbreviation is: ", states['Michigan']
print "Florida's abbreviation is: ", states['Florida']

# do it by using the state then cities dict
print '-' * 10
print "Michigan has: ", cities[states['Michigan']]
print "Florida has: ", cities[states['Florida']]

# print every state abbreviation
print '-' * 10
for state, abbrev in states.items():
    print "%s is abbreviated %s" % (state, abbrev)

# print every city in state
print '-' * 10
for abbrev, city in cities.items():
    print "%s has the city %s" % (abbrev, city)

# now do both at the same time
print '-' * 10
for state, abbrev in states.items():
    print "%s state is abbreviated %s and has city %s" % (
        state, abbrev, cities[abbrev])

print '-' * 10
# safely get a abbreviation by state that might not be there
state = states.get('Texas')

if not state:
    print "Sorry, no Texas."

# get a city with a default value
city = cities.get('TX', 'Does Not Exist')
print "The city for the state 'TX' is: %s" % city
```

## What you see

```sh
$ python ex39.py
----------
NY State has:  New York
OR State has:  Portland
----------
Michigan's abbreviation is:  MI
Florida's abbreviation is:  FL
----------
Michigan has:  Detroit
Florida has:  Jacksonville
----------
California is abbreviated CA
Michigan is abbreviated MI
New York is abbreviated NY
Florida is abbreviated FL
Oregon is abbreviated OR
----------
FL has the city Jacksonville
CA has the city San Francisco
MI has the city Detroit
OR has the city Portland
NY has the city New York
----------
California state is abbreviated CA and has city San Francisco
Michigan state is abbreviated MI and has city Detroit
New York state is abbreviated NY and has city New York
Florida state is abbreviated FL and has city Jacksonville
Oregon state is abbreviated OR and has city Portland
----------
Sorry, no Texas.
The city for the state 'TX' is: Does Not Exist
```

## But what Dicrionaries can do

Dictionaries are an example of data structures, lists in dictionaries are the most common use of data structures in programming. A dictionary uses map or associate what you want to save as a keyword


## When to use Dictionaries, when to use List

As mentioned in lesson 38. List is used when we want to store or organize things in a list style. The dictionary is similar but different from the list, the dictionary maps the storage object with the key. More clearly, we use dictionary when



1. You have to get things based on some identifiers, like names, addresses, or anything that might be the key 2. When one doesn't need to care about the order. Dictionaries have no concept of order, this list works 3. when you want to add or type elements by keyword



## Learn more

1. Practice the same type of map with cities and states / territories in your country or some other countries 2. Find more documents about dictionaries in Python and try to work with them 3. Find things that you cannot work with dictionaries. 4. Create a dump function like the list, but the function has enough content that you can debug. 5. Make sure you understand the role of the hash function in the code. It is a special function to convert string to integer. You can find out more about * hash *'s role online





## General questions

Q: What is the difference between a list and dictionary?

Answer: A list for an ordered list. A dictionary or dictionary for mapping between items keys and items values


Q: How to use a dictionary

Answer: when we want to get value from dictionary we can call it by keyword

Q: How to use the list

Answer: Use lists for any ordered list and call them according to the index

Q: If I use dictionaries, I need to organize them

Answer: We can use collections.OrderedDict in Python.
