2024/10/06
20:54

Status: #adult
Tags: [[question]] [[two pointer]] [[reverse]]
# Palindrome
# Question

implement a function to check if a linked list is a palindrome
# Solution
there are many ways to solve this questions but i will only coded only one of them but both ways is easy to code no worry

## Reversed Solution
in this solution we reverse the linked list then we compare two linked list see they are equal or not if they are equal we return true otherwise false

```python
import LinkedList
from LinkedList import PrintValues

linked_list = LinkedList.Node()
A = LinkedList.Node(0)
B = LinkedList.Node(1)
C = LinkedList.Node(2)
D = LinkedList.Node(3)
E = LinkedList.Node(2)
F = LinkedList.Node(1)
G = LinkedList.Node(0)


linked_list.next = A
A.next = B
B.next = C
C.next = D
D.next = E
E.next = F
F.next = G


def reverseAndClone(node):
    head = LinkedList.Node()
    while node is not None:
        n = LinkedList.Node(node.val)
        n.next = head
        head = n
        node = node.next
    return head


def isEqual(one, two):
    while one is not None and two is not None:
        if one.val != two.val:
            return False
        one = one.next
        two = two.next
    two = two.next.next
    return one is None and two is None


def isPalindrome(head):
    reversed = reverseAndClone(head)
    PrintValues(reversed)
    PrintValues(head)
    return isEqual(head.next, reversed)


print(isPalindrome(linked_list))
```

## Two Pointer Solution
in this solution we use fast and slow pointers and fast pointers 1 more than slow pointer until this reach the null ewe store every value of slow pointer after by the way don't forget to this can be also odd length list we iterate slow pointer and we compare the values these values current slow pointer values and old slow pointer values 

```java
boolean isPalindrome(LinkedListNode head) {
LinkedListNode fast= head;
LinkedListNode slow= head;

Stack<Integer> stack= new Stack<Integer>();

/* Push elements from first half of linked list onto stack. When fast runner
* (which is moving at 2x speed) reaches the end of the linked list, then we
* know we're at the middle*/
while (fast != null && fast.next != null) {
stack.push(slow.data);
slow slow.next;
fast= fast.next.next;
}

 /* Has odd number of elements, so skip the middle element*/
if (fast!= null) {
slow= slow.next;
}

 while (slow != null) {
 int top= stack.pop().intValue();
/* If values are different, then it's not a palindrome*/
if (top != slow.data) {
return false;
}
slow= slow.next;
}
return true;
} 
```
# References

[[📙 Cracking The Coding Interviews]]