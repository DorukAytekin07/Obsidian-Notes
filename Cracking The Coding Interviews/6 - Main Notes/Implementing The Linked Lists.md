2024/10/06
20:03

Status: #adult 
Tags: [[implementing data structure]] 
# Implementing The Linked Lists


# Quick Overview

implementing the linked list are not very hard task it just take some knowledge about the programming language but as i said it is not very hard task
# Detailed Research

here is the implementing of linked lists in python it is implement a linked list and print all of the values in the linked lists

```python
class Node:
    def __init__(self, data=None):
        self.val = data
        self.next = None


def PrintValues(head):
    curr = head
    while curr is not None:
        if curr.val is not None:
            print(curr.val, end=" -> ")
        curr = curr.next
    print("Null")


LinekdList = Node()
A = Node("A")
B = Node("B")
C = Node("C")
D = Node("D")
E = Node("E")
F = Node("F")


LinekdList.next = A
A.next = B
B.next = C
C.next = D
D.next = E
E.next = F


PrintValues(LinekdList)
```


# References

[[📙 Cracking The Coding Interviews#LinkedLists]]