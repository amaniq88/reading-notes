## In Tests We Trust — TDD with Python
**Unit tests** are some pieces of code to exercise the input, the output and the behaviour of your code.

**Test-Driven Development** is a strategy to think (and write!) tests first.

important details about TDD : 

1- The tests can be considered as your alive documentation. We need to be descriptive about it and to say what is expected and what we are testing.

2- The test file name should follow the same name of module name.

3- Arrange, Act and Assert( organize the data needed to execute -- > execute the code being tested  --- > check if the result (output) is the same as you were expecting )


### The Cycle

🆘 Write a unit test and make it fail 

✅ Write the feature and make the test pass!

🔵 Refactor the code 


## What does the if __name__ == “__main__”: do?

Advantages : 

1- Every Python module has it’s __name__ defined and if this is ‘__main__’, 

it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.

2- If you import this script as a module in another script, the __name__ is set to the name of the script/module.

3- Python files can act as either reusable modules, or as standalone programs.

4-if __name__ == “main”: is used to execute some code only if the file was run directly, and not imported.


## Recursion

Its The process in which a function calls itself directly or indirectly 

**The idea is to represent a problem in terms of one or more smaller problems, and add one or more base conditions that stop the recursion**

if the base case not reached or not define the Stack Overflow error occurs.


### direct and indirect recursion

in direct recursion the function call it self directly but in indirect the function call another function which will call the same function agin .


### tailed and non-tailed recursion.

 recursive function is tail recursive when recursive call is the last thing executed by the function
 
 
 ### How memory is allocated to different function calls in recursion? 
 
When any function is called from main(), the memory is allocated to it on the stack. 

A recursive function calls itself, the memory for a called function is allocated on top of memory allocated to calling function

and different copy of local variables is created for each function call. When the base case is reached, the function returns its

value to the function by whom it is called and memory is de-allocated and the process continues.

Example :
`
def fib(n):
 
    # Stop condition
    if (n == 0):
        return 0
 
    # Stop condition
    if (n == 1 or n == 2):
        return 1
 
    # Recursion function
    else:
        return (fib(n - 1) + fib(n - 2))
 n = 5;
print("Fibonacci series of 5 numbers is :",end=" ")
 
for i in range(0,n):
    print(fib(i),end=" ")`
