# Stacks and Queues

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)


**A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.**

## 1- PUSH
`Push` - Nodes or items that are put into the stack are pushed
Pushing a Node onto a stack will always be an O(1) operation

When adding a Node, you `push` it into the stack by assigning it as the new `top`, with its `next` property equal to the original top.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/pushStack3.PNG)


Here is the pseudocode to `push` a value onto a stack:
```
ALOGORITHM push(value)
// INPUT <-- value to add, wrapped in Node internally
// OUTPUT <-- none
   node = new Node(value)
   node.next <-- Top
   top <-- Node
```

## 2- Pop 
( the action of removing a Node from the top)

the`top` Node will be re-assigned to the Node that lives below and the `top Node` is `returned` to the user.

**check isEmpty before conducting a pop. This will ensure that an exception is not raised.**




`Pop` - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack4.PNG)

**return the value of the temp Node that was just popped off.**

```
ALGORITHM pop()
// INPUT <-- No input
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   Node temp <-- top
   top <-- top.next
   temp.next <-- null
   return temp.value
   ```

## 3- top
`Top` - This is the top of the stack.

`Peek` - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack1.PNG)



`IsEmpty` - returns true when stack is empty otherwise returns false


# What is a Queue :

`Enqueue` - Nodes or items that are added to the queue. (O(1))
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Enqueue3.PNG)

`Dequeue` - Nodes or items that are removed from the queue. (O(1))

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Dequeue3.PNG)

`Front` - This is the front/first Node of the queue.

`Rear` - This is the rear/last Node of the queue.



`Peek` - When you peek you will view the value of the front Node

you want to check isEmpty before conducting a peek. This will ensure that an exception is not raised. 

`sEmpty` - returns true when queue is empty otherwise returns false (O(1))



![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG)


## Stacks follow these concepts:

1-FILO (First In Last Out)
2-LIFO (Last In First Out)




