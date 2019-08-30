As we know getting input from users with raw_input or argv. Now we will retrieve data from the file. Here in the same folder we need to have two files. An ex15.py file and an ex15_test.txt file. Suppose we want to print the contents of the file ex15_test.txt
```sh
Phong nghien cuu và phat trien giai phap Cloud-Computing
Trung tam VDC-IT
Nguyen Phong Sac, Cau Giay, Ha Noi
```
The solution is to combine argv and raw_input to get the file name data
```sh
from sys import argv

script, filename = argv

txt = open(filename)

print "Here's your file %r:" % filename
print txt.read()

print "Type the filename again:"
file_again = raw_input("> ")

txt_again = open(file_again)

print txt_again.read()
```
### What You Should See

Create ex15_test.py file and run the script
```sh
$ python ex15.py ex15_test.txt
Phong nghien cuu và phat trien giai phap Cloud-Computing
Trung tam VDC-IT
Nguyen Phong Sac, Cau Giay, Ha Noi

Type the filenae again:
>  ex15_test.txt
Phong nghien cuu và phat trien giai phap Cloud-Computing
Trung tam VDC-IT
Nguyen Phong Sac, Cau Giay, Ha Noi
```
### Study Drills

### Common Student Questions


