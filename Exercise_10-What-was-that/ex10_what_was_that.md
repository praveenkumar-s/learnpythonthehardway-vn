There are two ways to create multi-line strings. The first is to insert "\ n" in the middle. The second is in the string entered at the end of the line we type "Enter"
For example
```sh
print "thanh \n ha"
```
hoặc là 
    
    print """thanh
    ha"""

To create an equivalent space, type the "Tab" key and use \ t. to use the "" character in the string we use "\". One more note is that when we want to add quotation marks "into the string we cannot enter the following string

    print " thanh ha in "VDC""
    
then we have to use single quotes instead of double quotes
```sh
print 'thanh ha in "VDC"'
```
You can also use "" "in this case.

In case we want to add single quotes to the string, do the opposite

Run the following program
```sh
tabby_cat = "\tI'm tabbed in."
persian_cat = "I'm split\non a line."
backslash_cat = "I'm \\ a \\ cat."

fat_cat = """
I'll do a list:
\t* Cat food
\t* Fishies
\t* Catnip\n\t* Grass
"""

print tabby_cat
print persian_cat
print backslash_cat
print fat_cat
```
### What You Should See
```sh
  I'm tabbed in.
I'm split
on a line.
I'm \ a \ cat.

I'll do a list:
        * Cat food
        * Fishies
        * Catnip
        * Grass
```
