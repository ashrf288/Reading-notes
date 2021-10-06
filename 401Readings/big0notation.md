## A beginner's guide to Big O Notation


Big O specifically describes the **worst-case scenario,** and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.

**Big O notation will always assume the upper limit where the algorithm will perform the maximum number of iterations.**

 important tool when dealing with algorithms that need to operate at **scale,** allowing you to make the correct choices and acknowledge trade-offs when working with different data sets.

### 1- O(1) :
algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

### 2- O(N)  :
algorithm whose performance will grow linearly and in direct proportion to the size of the input data set. 


### 3- O(N²) : 
 algorithm whose performance is directly proportional to the square of the size of the input data set.

 common with algorithms that involve nested iterations over the data set.

 **Deeper nested iterations will result in O(N³), O(N⁴) etc.**


 ### 4- O(2^N) :
 algorithm whose growth doubles with each addition to the input data set.

 The growth curve of an O(2^N) function is **exponential** — starting off very shallow, then rising meteorically. 
### 5- O(log N) Logarithms :
**extremely efficient when dealing with large data sets.**

 growth curve that peaks at the beginning and slowly flattens out as the size of the data sets increase.

 **Doubling the size of the input data set has little effect on its growth as after a single iteration of the algorithm the data set will be halved**


## linked list:
(data strucutre)

has 3 types:
1- singly: each node refer to the node next to it but the last one refer to null

2-doubly: each node refers to the node befor and the node after

3- circuler: same as singly but the last node refers to the first node in the list

**is often linked with big O notation**



big o notation: is a way to discripe how efficent 
somthing is (algorithems,dataStrucre) 
how will do it perform and how memory does it need


**you can think about them like grades**

## 1- best grade is (A+) : 
**constant** time (no matter if you add or delete it will take the same amount of time or memory(depend on condiditon)) **O(1)**

example: 
adding item to the beginning of a linked-list

so add to link list method takes O(1) 

## 2-(b+) O(n):
take avergae score 

perform in a linear form  where **n** present 
the number of the nodes in the linked-list.

to add somthing to the end of linked list you have to go throw each elemnt of the list a lot of nodes
it will take longer as the list size increases 

## 3- fail(f) O(2^N):
quadatric time

as the input gorws it will takes double the time or memory from befor adding that input


you can start evalute data structre base on how they evalute different things (like insert)
you need to use somthing that will abetter grade big O  that the other 

### example: 
linked -list : uses O(1) for adding to start of array
while array uses O(n) **because it will have to update all  elemnts index** to add 
so we should use O(1) for this useCase


### example : 
searching for item is easier in array more than linked list because index will help us to find what we want more quickly


**the size of the list and what we want to do with list items are keys to help us pick the right approch**
