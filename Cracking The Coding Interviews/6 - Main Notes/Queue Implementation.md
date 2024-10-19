2024/10/17
19:36

Status: #adult  
Tags: [[queue]] [[implementing data structure]]
# Queue Implementation


# Quick Overview
a queue use FIFO principle they are also required implementation for better understanding like stacks so if you will implement them it will be better with these operations

add(item):add an item to tail (end) of the list
remove():remove head (first) node of the list
peek():return the top of the queue
isEmpty():check the list is empty or not

a queue can be implementing with linked list but if you want you can implement with other methods

also they are widely used in BFS algorithm
# Detailed Research
```python
import LinkedList as ll

class Queue:
    def __init__(self, values):
        self.first = ll.Node()
        queue = self.first

        for i in values:
            queue.next = ll.Node(i)
            queue = queue.next
        self.first = self.first.next

    def printItems(self):
        queue = self.first
        while queue is not None:
            print(queue.val, end=" -> ")
            queue = queue.next
        print("Null")

    def add(self, item):
        queue = self.first
        while queue.next is not None:
            queue = queue.next
        queue.next = ll.Node(item)

    def remove(self):
        self.first = self.first.next

    def peek(self):
        return self.first.val

    def isEmpty(self):
        return self.first is None


queue = Queue([1, 2, 3, 4, 5])
queue.printItems()
queue.add(6)
queue.printItems()
queue.remove()
queue.printItems()
print(queue.peek())
print(queue.isEmpty())

```

queues is used in BFS algorithms which is very important in graph algorithms so be sure you understand them in the future you will use them so much
# References

[[📙 Cracking The Coding Interviews#Stack And Queues]]