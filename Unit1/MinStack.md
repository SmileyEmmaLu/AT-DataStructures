# MinimumStack

A class that acts like a stack with one new method: ```min```.

```java

void push(Comparable element)    //add an element
Comparable pop()                 //remove and return the top element
boolean isEmpty()   
int size()

//new method
Comparable min()                 //returns (does not remove) the smallest element in the stack currently

//not required, but common
Comparable peek()                //look at the top element without removing

```
## Solution 1:
Keep a stack of min-so-far elements in addition to the regular stack. Only works with ```Comparable``` objects.
* Push: if x is less than top of min stack, push x on both stacks.
* Pop: if the top of the min stack equals the top of the full stack, pop off of both. 
* Peek: peek off of full stack
* min: peek off of min stack
### Pros:
* Min takes constant time O(1).
* works for any Comparable type object
### Cons:
* the stack takes up to O(n) extra space

## Solution 2:
Save minElem as instance data, encode info about previous min inside element pushed on the stack.
* Push: if x is less than minElem, store 2*x - minElement on the stack.
* Pop: if popped item y is less than minElem, use the formula 2*minElem - y to get the previous minElem.
* Peek: if top item is less than minElem, return minElem.
* min: return minElem
### Pros:
* Min takes constant time O(1).
* Storage takes constant ammount of extra space O(1)
### Cons:
* Elements must be able to be added, subtracted and multiplied.


