2024/10/06
20:35

Status: #adult  
Tags: [[question]] [[linked list]] [[temporary buffer]]
# Sum Lists
# Question

You have two numbers represented by a linked list where each node contains a single digit the digits are stored in reverse order such that the 1's digit is at the head of the list write a function that add two numbers and returns the sum as a linked list

EXAMPLE
input: (7 -> 1 -> 6) + (5 -> 9 -> 2) that is 617 + 295

output: 2 -> 1 -> 9 that is 912
# Solution
to solve this question you can use many algorithms but i will only implement this with temporary buffer solution but if you find another this also good
## Temporary Buffer Solution

```python
import LinkedList
from LinkedList import PrintValues

linked_list1 = LinkedList.Node()
linked_list2 = LinkedList.Node()
result = LinkedList.Node()
A = LinkedList.Node(2)
B = LinkedList.Node(3)
C = LinkedList.Node(8)
D = LinkedList.Node(2)
E = LinkedList.Node(9)
F = LinkedList.Node(3)

linked_list1.next = A
A.next = B
B.next = C

linked_list2.next = D
D.next = E
E.next = F

num1 = ""
num2 = ""

linked_list1 = linked_list1.next
linked_list2 = linked_list2.next
while linked_list1 is not None:
    num1 = str(linked_list1.val) + num1
    linked_list1 = linked_list1.next
while linked_list2 is not None:
    num2 = str(linked_list2.val) + num2
    linked_list2 = linked_list2.next
sum = int(num1) + int(num2)

current = result
for i in str(sum):
    digit = LinkedList.Node(i)
    current.next = digit
    current = current.next
PrintValues(result)
```

Time Complexity 
$O(n)$

Space Complexity
$O(n)$
# References

[[📙 Cracking The Coding Interviews]]