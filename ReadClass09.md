# Dunder Methods:
a set of predefined methods you can use to enrich your classes.
They are easy to recognize because they start and end with double underscores,
for example __init__ or __str__.
Dunder methods let you emulate the behavior of built-in types. 


Another example is slicing. 
You can implement a __getitem__ method which allows you to use Python’s list slicing syntax: obj[start:stop].

##  the use of dunder methods : 
1- Enriching a Simple Account Class
- Initialization of new objects
- Object representation
- Enable iteration
- Operator overloading (comparison)
- Operator overloading (addition)
- Method invocation
- Context manager support (with statement)

### Object Initialization: __init__
Right upon starting my class I already need a special method.
To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:

### Object Representation: __str__, __repr__
t’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) 
There are two ways to do this using dunder methods:

__repr__: The “official” string representation of an object. This is how you would make an object of the class. 
The goal of __repr__ is to be unambiguous.

__str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

Iteration:
__len__, __getitem__, __reversed__
In order to iterate over our account object I need to add some transactions.
So first, I’ll define a simple method to add transactions.
I’ll keep it simple because this is just setup code to explain dunder methods, 
and not a production-ready accounting system.

Operator Overloading for Comparing Accounts:
__eq__, __lt__
We all write dozens of statements daily to compare Python objects.

Operator Overloading for Merging Accounts:
__add__
In Python, everything is an object.
We are completely fine adding two integers or two strings with the + (plus) operator, it behaves in expected ways

Callable Python Objects:
__call__
You can make an object callable like a regular function by adding the __call__ dunder method. 
For our account class we could print a nice report of all the transactions that make up its balance

Context Manager Support and the With Statement:
__enter__, __exit__



# Tutorial: Basic Statistics in Python — Probability

## What is probability?
probability seeks to answer the question, “What is the chance of an event happening?” An event is some outcome of interest. 
To calculate the chance of an event happening, we also need to consider all the other events that can occur. 
The quintessential representation of probability is the humble coin toss. In a coin toss the only events that can happen are:
Flipping a heads
Flipping a tails
These two events form the sample space, the set of all possible events that can happen.
To calculate the probability of an event occurring, we count how many times are event of interest can occur (say flipping heads) and dividing it by the sample space.
Thus, probability will tell us that an ideal coin will have a 1-in-2 chance of being heads or tails.
By looking at the events that can occur, probability gives us a framework for making predictions about how often events will happen.
However, even though it seems obvious, if we actually try to toss some coins, we’re likely to get an abnormally high or low counts of heads every once in a while.

## Conclusion
We started with descriptive statistics and then connected them to probability.
From probability, we developed a way to quantatively show if two groups come from the same distribution.
In this case, we compared two wine recommendations and found that they most likely do not come from the same score distribution. 
In other words, one wine type is most likely better than the other one. Statistics doesn’t have to be a field relegated to just statisticians. 
As a data scientist, having an intuitive understanding on common statistical measures represent will give you an edge on developing your own theories and the ability to subsequently test these theories.
We barely scratched the surface of inferential statistics here, but the same general ideas here will help guide your intuition in your statistical journey. 
Our article discussed the advantages of the normal distribution, but statisticians have also developed techniques to adjust for distributions that aren’t normal.

