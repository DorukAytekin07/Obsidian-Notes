2024/10/06
20:14

Status: #adult 
Tags: [[question]] [[linked list]] [[brute force]]
# Remove Duplicates
# Question

Write code to remove duplicates from an unsorted linked list
# Solution

## Temporary Buffer Solution
to solve this problem we can use a temporary buffer to store the values of linked list and if we found it in this buffer we will delete a solution like this can be coded in python as that

```python
import LinkedList
from LinkedList import PrintValues

linked_list = LinkedList.Node()
A = LinkedList.Node("A")
B = LinkedList.Node("B")
C = LinkedList.Node("C")
D = LinkedList.Node("C")
E = LinkedList.Node("D")
F = LinkedList.Node("A")

linked_list.next = A
A.next = B
B.next = C
C.next = D
D.next = E
E.next = F

elements = []


PrintValues(linked_list)

curr = linked_list.next
previous = LinkedList.Node()
while curr is not None:
    if curr.val in elements:
        previous.next = curr.next
    else:
        elements.append(curr.val)
        previous = curr
    curr = curr.next

PrintValues(linked_list)
```

## Brute Force Solution
alright what if he said we cannot use temporary buffer in this time we will search through whole linked list and if we found a duplicate we will remove this approach can be coded like that\

```python
import LinkedList
from LinkedList import PrintValues

linked_list = LinkedList.Node()
A = LinkedList.Node("A")
B = LinkedList.Node("B")
C = LinkedList.Node("C")
D = LinkedList.Node("C")
E = LinkedList.Node("D")
F = LinkedList.Node("A")

linked_list.next = A
A.next = B
B.next = C
C.next = D
D.next = E
E.next = F


PrintValues(linked_list)

curr = linked_list.next
while curr is not None:
    runner = curr
    while runner.next is not None:
        if runner.next.val == curr.val:
            runner.next = runner.next.next
        else:
            runner = runner.next
    curr = curr.next
    
PrintValues(linked_list)
```

# References

[[📙 Cracking The Coding Interviews]]