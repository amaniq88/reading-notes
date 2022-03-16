# List Comprehensions in Python
List comprehension is a powerful and concise method for creating lists in Python that becomes essential the more you work with lists, and lists of lists.
**Syntax**
my_new_list = [ expression for item in list ]


**three ingredients are necessary for a python list comprehension to work.**
1- First is the expression we’d like to carry out. expression inside the square brackets.
2-Second is the object that the expression will work on. item inside the square brackets.
3-Finally, we need an iterable list of objects to build our new list from. list inside the square brackets.

**Notes about Lists Comprehensions**
List comprehension methods are an elegant way to create and manage lists. 
In Python, list comprehensions are a more compact way of creating lists. 
More flexible than for loops, list comprehension is usually faster than other methods.

**Create a List with range()**
`# construct a basic list using range() and list comprehensions
# syntax
# [ expression for item in list ]
digits = [x for x in range(10)]

print(digits)`


**Create a List Using Loops and List Comprehension in Python**
`# create a list using a for loop
squares = []

for x in range(10):
    # raise x to the power of 2
    squares.append(x**2)

print(squares)`

**Show the first letter of each word using Python**
`# a list of the names of popular authors
authors = ["Ernest Hemingway","Langston Hughes","Frank Herbert","Toni Morrison",
    "Emily Dickson","Stephen King"]

#create an acronym from the first letter of the author's names
letters = [ name[0] for name in authors ]
print(letters)`


**Parsing a file using list comprehension**
It’s also possible to read files in Python using list comprehension.
#open the file in read-only mode
file = open("dreams.txt", 'r')
poem = [ line for line in file ]

for line in poem:
    print(line)
    
**Using functions in list comprehensions**
# list comprehension with functions
# create a function that returns a number doubled
def double(x):
    return x*2

nums = [double(x) for x in range(1,10)]
print(nums)


