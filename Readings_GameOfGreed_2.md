## Modules: The Global Scope
the notions of global scope and global names are tightly associated with module files. For example, if you define a name at the top level of any Python module,
then that name is considered global to the module. That’s the reason why this kind of scope is also called module scope.

Note: Global names can be updated or modified from any place in your global Python scope.
Beyond that, the global statement can be used to modify global names from almost any place in your code, as you’ll see in The global Statement.

Modifying global names is generally considered bad programming practice because it can lead to code that is:

Difficult to debug: Almost any statement in the program can change the value of a global name.
Hard to understand: You need to be aware of all the statements that access and modify global names.
Impossible to reuse: The code is dependent on global names that are specific to a concrete program.
Good programming practice recommends using local names rather than global names. Here are some tips:

Write self-contained functions that rely on local names rather than global ones.
Try to use unique objects names, no matter what scope you’re in.
Avoid global name modifications throughout your programs.
Avoid cross-module name modifications.
Use global names as constants that don’t change during your program’s execution.


## The nonlocal Statement
Similarly to global names, nonlocal names can be accessed from inner functions, but not assigned or updated. 
If you want to modify them, then you need to use a nonlocal statement. With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.

The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas.
These names will refer to the same names in the enclosing Python scope. 


## Big O# 
  it is a mesure of How long the algorlthim is take to do someTking in  term of Time / Space ( how much memory its take ) 
  it is a way of compairing algorithem with each other.
  as the amount of data increases how this alogirithem response in a term of time or space 
  its about the worst Case senario  // Not the Best Case senario 
  Types : 
  1- Constant comlexsity 
  2- Logarithmic complexity 
  3- Linear complexity 
  4- Quadratic 
  5- Exponentioal 
