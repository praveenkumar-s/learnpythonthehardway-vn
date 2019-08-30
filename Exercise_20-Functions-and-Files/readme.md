# Exercise 20: Functions and Files

## For example

In this lesson, we learned how to combine functions and files.

Script: 

    from sys import argv
    script, input_file = argv
    # đọc file 
    def print_all(f):
        print f.read()
    # di chuyển đến byte đầu tiên của file
    def rewind(f):
        f.seek(0)
    #In ra dòng thứ và in ra dòng 
    def print_a_line(line_count, f):
        print line_count, f.readline()
    current_file = open(input_file)
    print "First let's print the whole file:\n"
    print_all(current_file)
    print "Now let's rewind, kind of like a tape."
    rewind(current_file)
    print "Let's print three lines:"
    current_line = 1
    print_a_line(current_line, current_file)
    current_line = current_line + 1
    print_a_line(current_line, current_file)
    current_line = current_line + 1
    print_a_line(current_line, current_file)

## code 

    $ python ex20.py test.txt
    First let's print the whole file:

    This is line 1
    This is line 2
    This is line 3

    Now let's rewind, kind of like a tape.
    Let's print three lines:
    1 This is line 1

    2 This is line 2

    3 This is line 3

## Practice

* Write comments on each line to understand what this line does * With each time print_a_line is running, you are passing a variable called current_line * Go to each function used, double check * def * to make sure you passed it Correct parameter. * Research on the seek () function. Try pydoc file * Research the character + =





## Question

* What is f in print_all and other functions?     The variable f is the same as the functions in lesson 18. A file in python will look like a big drive, or a DVD drive. It has a "read head", and you can "seek" as a reader to move to a pointer within a file, and then work with it. Each lane you run f.seek (0) you will move to the first value of the file. Each time you run f.readline () you are reading a line from the file, and moving from the beginning to the end of the file by the "\ n" character. * Why not set seek (current_line) instead of seek (0)?     First, the seek () function is a non-line byte. The seek (0) function moves to the first byte of the file. * How does readline () know each line?









    Inside the readline () is the code that can scan each byte of the file until it reaches the "\ n" character, then stop reading the file and return the string. File f is responsible for maintaining the current location of the file.
