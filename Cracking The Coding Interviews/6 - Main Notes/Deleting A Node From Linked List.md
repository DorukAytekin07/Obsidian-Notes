2024/10/06
20:05

Status: #adult 
Tags: [[operations on data structures]] [[deleting]]
# Deleting A Node From Linked List

# Quick Overview

deleting a node from a linked list is pretty straightforward you just have to change previous and next pointers of node
# Detailed Research

deleting a node from a linked list pretty straight forward 
process all you just have to do find target node and making his prev node next to current next node after you have to assign current next to null value following code is making this and print the first and last state of linked list

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


def DeleteANodeFromLinkedList(head, target):
    curr = head
    prev = curr
    while curr.val != target:
        prev = curr
        curr = curr.next
    nextval = curr.next
    curr.next = None
    prev.next = nextval


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

DeleteANodeFromLinkedList(LinekdList, "B")

PrintValues(LinekdList)
```


# References

[[📙 Cracking The Coding Interviews#LinkedLists]]