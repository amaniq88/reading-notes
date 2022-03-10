# Reading Notes Class 05

## Big O: Analysis of Algorithm Efficiency
Big O(oh) notation is used to describe the efficiency of an algorithm or function.
This efficiency is evaluated based on 2 factors:
1- Running Time (also known as time efficiency / complexity): The amount of time a function needs to complete.
2- Memory Space (also known as space efficiency / complexity): The amount of memory resources a function uses to store data and instructions.

it start by descriping the *worstCase*
4 Key Areas for analysis:
- Input Size : the size of the parameter values that are read by the algorithm  (  size of each parameter)
The higher this number, the more likely there will be an increase to Running Time and Memory Space.
- Units of Measurement :
Three Measurements of time:
  - The time in milliseconds from the start of a function execution until it ends.
  - The number of operations that are executed.
  - The number of “Basic Operations” that are executed.

**Four Sources of Memory Usage during function run-time:**
1-The amount of space needed to hold the code for the algorithm.
2-The amount of space needed to hold the input data.
3- The amount of space needed for the output data.
4- The amount of space needed to hold working space during the calculation.

- Orders of Growth :  the Order of Growth represents the increase in Running Time or Memory Space.
- Best Case, Worst Case, and Average Case : 
  -Worst Case: The efficiency for the worst possible input of size n
  - Best Case: The efficiency for the best possible input of size n
  - Average Case: The efficiency for a “typical” or “random” input of size n.
  ![Basic](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/EfficiencyNotations.png)
  
  
  
  ------------------------------
  ## Linked Lists
A Linked List is a sequence of Nodes that are connected/linked to each other. 
The most defining feature of a Linked List is that each Node references the next Node in the link.

**Linked List ** - A data structure that contains nodes that links/points to the next node in the list.

- Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
- Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
- Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
- Next - Each node contains a property called Next. This property contains the reference to the next node.
- Head - The Head is a reference of type Node to the first node in a linked list.
- Current - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.
 


