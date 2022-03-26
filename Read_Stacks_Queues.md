# Stacks and Queues
Stack :  A stack is a data structure that consists of Nodes.

Each Node references the next Node in the stack, but does not reference its previous.

# main functions of this data structure : 

Push - Nodes or items that are put into the stack are pushed
Pop - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
Top - This is the top of the stack.
Peek - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
IsEmpty - returns true when stack is empty otherwise returns false.


# the main concept of the stack  : 

1- FILO :  means First In Last Out

This means that the first item added in the stack will be the last item popped out of the stack.

2- LIFO :-Last In First Out

This means that the last item added to the stack will be the first item popped out of the stack.

Stack

Push O(1)
Pushing a Node onto a stack will always be an O(1) operation. This is because it takes the same amount of time no matter how many Nodes (n) you have in the stack.

When adding a Node, you push it into the stack by assigning it as the new top, with its next property equal to the original top.

Let’s walk through the steps:

First, you should have the Node that you want to add. Here is an example of a Node that we want to add to the stack. Push to Stack 01
Next, you need to assign the next property of Node 5 to reference the same Node that top is referencing: Node 4 Push to Stack 02
