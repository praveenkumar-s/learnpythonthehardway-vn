In this section, we will run the script along with the parameters

For example, in the following program
```sh
from sys import argv

script, first, second, third = argv

print "The script is called:", script
print "Your first variable is:", first
print "Your second variable is:", second
print "Your third variable is:", third
```
We use 'import' to add features to the script. This makes the program more compact but also means we have to write documents for the program

'argv' is a logical variable, a standard syntax, containing the variables passed when running the script. As in the above example, the variables firt, second, third.

### Hold Up! Features Have Another Name


### What You Should See
```sh
$ python ex13.py first 2nd 3rd
The script is called: ex13.py
Your first variable is: first
Your second variable is: 2nd
Your third variable is: 3rd
$ python ex13.py stuff things that
The script is called: ex13.py
Your first variable is: stuff
Your second variable is: things
Your third variable is: that
```
If we do not pass all 3 input parameters, the program will display an error
````sh
$ python ex13.py first 2nd
Traceback (most recent call last):
  File "ex13.py", line 3, in <module>
    script, first, second, third = argv
ValueError: need more than 3 values to unpack
```
