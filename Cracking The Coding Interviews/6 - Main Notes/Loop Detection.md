2024/10/06
21:10

Status: #adult  
Tags: [[question]] [[linked list]] [[two pointer]]
# Loop Detection
# Question

Given a circular linked list implement an algorithms that returns the node at the beginning of the loop

DEFINITION
Circular linked list: A (corrupt) linked list in which a node's next pointer points to an earlier node so as to make a loop in the linked list

EXAMPLE
input: A -> B -> C -> D -> E -> C

output : C
# Solution
it is again a two pointer solution it's code is very straightforward so i won't make any other explanation

```java
LinkedListNode FindBeginning(LinkedlistNode head) {
LinkedListNode slow head;
LinkedlistNode fast = head;

/* Find meeting point. This will be LOOP_SIZE - k steps into the linked list. */
while (fast != null && fast.next != null) {
slow = slow.next;
fast = fast.next.next;
if (slow == fast) {//Collision
	break;
	}
}

/* Error check - no meeting point, and therefore no loop*/
if (fast == null I I fast.next == null) {
	return null;
}

/* Move slow to Head. Keep fast at Meeting Point. Each are k steps from the
* Loop Start. If they move at the same pace, they must meet at Loop Start. */
slow = head;
while (slow!= fast) {
slow slow.next;
fast= fast.next;
}

/* Both now point to the start of the loop. */
return fast;
}
```


# References

[[📙 Cracking The Coding Interviews]]