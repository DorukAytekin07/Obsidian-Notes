2024/10/06
20:27

Status: #adult 
Tags: [[question]] [[linked list]] [[temporary buffer]]
# Partition
# Question

Write code to partition a linked list around a value x such that all nodes less than x come before all nodes greater than or equal to x if x is contained within the list the values of x only need to be after the elements less than x  (see below) the partition element x can appear anywhere in  the right partition it does not need to appear between the left and right partitions

EXAMPLE
input: 3 -> 5 -> 8 -> 5 -> 10 -> 2 -> 1 (partition = 5)

output: 3 -> 1 -> 2 -> 10 -> 5 -> 5 -> 8
# Solution

## Temporary Buffer Solution

```python
import LinkedList
from LinkedList import PrintValues

linked_list = LinkedList.Node()
result = LinkedList.Node()
A = LinkedList.Node(3)
B = LinkedList.Node(5)
C = LinkedList.Node(8)
D = LinkedList.Node(5)
E = LinkedList.Node(10)
F = LinkedList.Node(2)
G = LinkedList.Node(1)


linked_list.next = A
A.next = B
B.next = C
C.next = D
D.next = E
E.next = F
F.next = G

head = []
tail = []
x = 5
linked_list = linked_list.next

PrintValues(linked_list)
while linked_list is not None:
    if linked_list.val < x:
        head.append(linked_list.val)
    else:
        tail.append(linked_list.val)
    linked_list = linked_list.next
left = result

for i in head:
    left.next = LinkedList.Node(i)
    left = left.next

right = left

for i in tail:
    right.next = LinkedList.Node(i)
    right = right.next

PrintValues(result)
```

# References

[[📙 Cracking The Coding Interviews]]