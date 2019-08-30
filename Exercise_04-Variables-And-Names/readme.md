# Exercise 4: Variables And Names 

## I. For example
Now you can print everything with print and you can do it with operations. The next step is learning about variables. In programming, the variable is just a name, similar to "My name is Zed, who wrote this book".

Variables are often names to recall in the code. If the variable is named badly, chances are you will read it again and you'll forget what you wrote.

Syntax:

```sh
name variable = value value
```

Có đoạn code: 

```sh
# -*- coding: utf-8 -*-

cars = 100
space_in_a_car = 4.0
drivers = 30
passengers = 90 
cars_not_driven = cars - drivers 
cars_driven = drivers 
carpool_capacity = cars_driven * space_in_a_car
average_passengers_per_car = passengers / cars_driven

print "There are", cars, "cars available."
print "There are only", drivers, "drivers available."
print "There will be", cars_not_driven, "empty cars today."
print "We can transport", carpool_capacity, "people today."
print "We have", passengers, "to carpool today."
print "We need to put about", average_passengers_per_car, "in each car."
```

## II. The result of the above source code

<img src=http://i.imgur.com/Fbz84x0.png width="60%" height="60%" border="1">

## III. Luyện Tập 
- Use 4.0 for variables space_in_a_carinstead of 4. What if I left it as 4. Try it.
- 4.0 is a dynamic number type.

## IV. Câu hỏi 
- What is the difference between ampersands =and ==?
