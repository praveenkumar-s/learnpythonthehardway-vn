You have learned * if-statements * , functions and list. Now we will review this knowledge. Execute the following program and see what the program does:

```sh
from sys import exit

def gold_room():
    print "This room is full of gold.  How much do you take?"

    choice = raw_input("> ")
    if "0" in choice or "1" in choice:
        how_much = int(choice)
    else:
        dead("Man, learn to type a number.")

    if how_much < 50:
        print "Nice, you're not greedy, you win!"
        exit(0)
    else:
        dead("You greedy bastard!")


def bear_room():
    print "There is a bear here."
    print "The bear has a bunch of honey."
    print "The fat bear is in front of another door."
    print "How are you going to move the bear?"
    bear_moved = False

    while True:
        choice = raw_input("> ")

        if choice == "take honey":
            dead("The bear looks at you then slaps your face off.")
        elif choice == "taunt bear" and not bear_moved:
            print "The bear has moved from the door. You can go through it now."
            bear_moved = True
        elif choice == "taunt bear" and bear_moved:
            dead("The bear gets pissed off and chews your leg off.")
        elif choice == "open door" and bear_moved:
            gold_room()
        else:
            print "I got no idea what that m

def cthulhu_room():
    print "Here you see the great evil Cthulhu."
    print "He, it, whatever stares at you and you go insane."
    print "Do you flee for your life or eat your head?"

    choice = raw_input("> ")

    if "flee" in choice:
        start()
    elif "head" in choice:
        dead("Well that was tasty!")
    else:
        cthulhu_room()


def dead(why):
    print why, "Good job!"
    exit(0)

def start():
    print "You are in a dark room."
    print "There is a door to your right and left."
    print "Which one do you take?"

    choice = raw_input("> ")

    if choice == "left":
        bear_room()
    elif choice == "right":
        cthulhu_room()
    else:
        dead("You stumble around the room until you starve.")


start()
```



### What You Shoud See
Run the above program and enter options, for example 

```sh
$ python ex35.py
You are in a dark room.
There is a door to your right and left.
Which one do you take?
>  left
There is a bear here.
The bear has a bunch of honey.
The fat bear is in front of another door.
How are you going to move the bear?
>  taunt bear
The bear has moved from the door. You can go through it now.
>  open door
This room is full of gold.  How much do you take?
>  1000
You greedy bastard! Good job!
```

### Study Drills

1. Draw a diagram of the game and how to get past it 2. Fix all your errors, including syntax errors 3. Write notes for funtions you don't understand 4. Add to the game , simple 5. In the * gold_room * function ask the user to enter a number. Getting an error when the user enters not an integer. Use the int () function to do this




 
### Common Student Questions
Q1: Why write * while True * ?

Answer: infinite loop, only exits when there is a branch statement or the command to switch to another function

Q2: * exit (0) * for what?

Answer: Many systems can be canceled with * exit (0) * , if it is * exit (1) * then there will be errors. so we can use * exit (1) * and * exit (2) * for different errors

Q3: Why are some cases using raw_input (), some using raw_input ('>')?

Answer: All string strings in raw_input are intended to suggest and prompt the user to enter
