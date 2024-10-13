2024/10/06
20:23

Status: #adult 
Tags: [[question]] [[linked list]]
# Delete Middle Node
# Question

Implement an algorithm to delete a node in the middle (no matter what node except fist and last) of a singly linked list given only access to that node

EXAMPLE
input: the node c from the linked list a -> b -> c -> d -> e -> f

output: the new linked list is a -> b -> d -> e -> f
# Solution
in this question you don't know the head of linked list so all you have to do is just determine given node is not last or first node if it doesn't then return True else False

```python
import LinkedList

linked_list = LinkedList.Node(None)
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


def DeleteMiddle(linked_list):
    if linked_list.val is None or linked_list.next is None:
        return False
    next = linked_list.next
    linked_list.val = next.val
    linked_list.next = next.next
    return True


if DeleteMiddle(A):
    print("Yes The Node Can Be Middle Node")

else:
    print("No The Node Cannot Be Middle Node")
```
# References

[[📙 Cracking The Coding Interviews]]