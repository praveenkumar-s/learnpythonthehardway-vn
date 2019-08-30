#Exercise 17: More Files

## For example

Now we will do more about the file, in this article write a script to copy the content from one file to another. 

Code:     from sys import argv     from os.path import exists     script, from_file, to_file = argv     # Print the name of 2 file     prints "Copying from% s to% s"% (from_file, to_file)     # Open the file you want to copy     in_file = open ( from_file)     # Read the entire contents of in_file and return a string stored in indata. The read () function returns a string.     indata = in_file.read ()     print "The input file is% d bytes long"% len (indata)     # Check if the copied file exists.     "Does the output file exist?% r"% exists (to_file)     # Are you sure you want to continue copying if you press any button if not ctrl-c














    print "Ready, hit RETURN to continue, CTRL-C to abort." 
    raw_input () 
    # Opening the file if this file exists will delete the contents of this fileUp, otherwise create a new file. 
    out_file = open (to_file, 'w') 
    # write content from from_file to to_file 
    out_file.write (indata) 
    print "Alright, all done." 
    # Round 2 files again. 
    out_file.close () 
    in_file.close ()


## Copy file code 

    $ echo "This is a test file." > test.txt
    $ python ex17.py test.txt new_file.txt
    Copying from test.txt to new_file.txt
    The input file is 21 bytes long
    Does the output file exist? False
    Ready, hit RETURN to continue, CTRL-C to abort.

Check the content of new_file.txt with the * cat * command to see the result.

## Practice

* Find out why you have to use out_file.close () in the code

## Question

* What is len ()?       It returns the length of the string * I get the following error: * Syntax: EOL while scanning string literal *      You forgot to end the string with quotation marks.






















 
