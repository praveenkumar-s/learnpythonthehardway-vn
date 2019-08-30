It is important that you understand the difference between classes and objects. The problem is, there is no real "difference" between a class and an object. They have similarities. For example, the difference between fish and salmon. The question makes us confused. We see that salmon and fish are different but salmon is a form of fish, it can also be understood that there is no difference between fish and salmon. But salmon is different from other fish. Salmon is different from sharks. So salmon and fish have something in common, but there are also differences.
 
 You don't need to think about the difference between salmon and sharks because you know that they are related. You know salmon is one type of fish and there are other types of fish.
 
Imagine that in an aquarium there are three fish named Frank, Joe and Mary. The question is the difference between Mary and Salmon. Contact the previous question you know that Mary is salmon. and Mary is an example of salmon. Joe and Frank are also examples of salmon.


We now have the following observations: Fish is a class, and salmon is also a class, Mary is also a class. The fish class is an abstract class that is not only specific to each object. Fish are generally for entities that live in water. Salmon is the object of the fish class will have its own characteristics such as red, large, living in the ocean or in fresh water.




## Object-oriented code

```sh
## Animal is-a object (yes, sort of confusing) look at the extra credit
class Animal(object):
    pass

## ??
class Dog(Animal):

    def __init__(self, name):
        ## ??
        self.name = name

## ??
class Cat(Animal):

    def __init__(self, name):
        ## ??
        self.name = name

## ??
class Person(object):

    def __init__(self, name):
        ## ??
        self.name = name

        ## Person has-a pet of some kind
        self.pet = None

## ??
class Employee(Person):

    def __init__(self, name, salary):
        ## ?? hmm what is this strange magic?
        super(Employee, self).__init__(name)
        ## ??
        self.salary = salary

## ??
class Fish(object):
    pass

## ??
class Salmon(Fish):
    pass

## ??
class Halibut(Fish):
    pass


## rover is-a Dog
rover = Dog("Rover")

## ??
satan = Cat("Satan")

## ??
mary = Person("Mary")

## ??
mary.pet = satan

## ??
frank = Employee("Frank", 120000)

## ??
frank.pet = rover

## ??
flipper = Fish()

## ??
crouse = Salmon()

## ??
harry = Halibut()
```

## Learn more

1. Research why Python adds this object class, and what that means. 2. You can use a class as an object 3. Add animal, fish, and people classes in this exercise with the functions 4. Create more new classes with related relationships




## Answer

Q: self.pet = none

Answer: The above statement sets the self attribute to be null

Q: Super command (Employee, self). __ init __ (name) for what?

Answer: The above command is used to call the parent class of Employee class
