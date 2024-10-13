2024/10/06
20:22

Status: #adult 
Tags: [[question]] [[linked list]] [[two pointer]]
# Return Kth to Last
# Question

Implement an algorithm to find the kth to last element of a singly linked list
# Solution

## Solution Length Size Is Know
if you know the size of linked list all you have to is just traverse the list length - k times i won't implement this because it is very easy job you can make this

## Iterative (Two Pointer) Solution
in this solution we use second pointer technique and we firstly iterate p1 k times and after we will iterate two pointers together until p1 reach the finish or null which one do you prefer 

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

k = 0

PrintValues(linked_list)

p1 = linked_list.next
p2 = linked_list.next

if k == 0:
    k += 1

for i in range(k):
    if p1 is None:
        p2.val = None
        break
    p1 = p1.next

while p1 is not None:
    p1 = p1.next
    p2 = p2.next

print(p2.val)
```



# References

[[📙 Cracking The Coding Interviews]]