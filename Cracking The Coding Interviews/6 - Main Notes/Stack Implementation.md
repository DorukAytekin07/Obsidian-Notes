2024/10/17
19:26

Status: #adult  
Tags: [[stacks]] [[implementing data structure]]
 
 # Stack Implementation

# Quick Overview
the stack data structure is pretty straightforward data structure
it uses LIFO principle also this is a homework for better understand i suggest implementing it with following operations

pop(): Remove item from top of stack
push(item):push an item to top of stack
peek():return an item from top of stack
isEmpty():check the stack it is empty or not if it is empty return True otherwise return False

write benefits of stacks also disadvantages and do not forget implement them
# Detailed Research

```python
class Stack:
    def __init__(self, values):
        self.values = values

    def pop(self):
        self.values.pop()

    def push(self, item):
        self.values.append(item)

    def peek(self):
        return self.values[-1]

    def imEmpty(self):
        if len(self.values) == 0:
            return True
        else:
            return False

    def printItems(self):
        for i in self.values:
            print(i, end=" ")


stack = Stack([1, 2, 3, 4, 5])

stack.push(6)

stack.printItems()

print("\nThe Last Item = " + str(stack.peek()))

stack.pop()

stack.printItems()

print("\nThe Stack Is Empty" if stack.imEmpty() else "\nThe Stack Is Not Empty")
```

## Advantages:
1. they are very simple to use and understand 

2. they provide $O(1)$ access time for top element and also constant element push add pop

3. they can be use to reverse the order of something also they mainly use at undo/redo applications
## Disadvantages:
1. they only provide constant access time for only top element not other element

2. also they are not efficient for searching

3. finally if they are full you cannot add any more element and this is know as drawback

# References

[[📙 Cracking The Coding Interviews#Stack And Queues]]
