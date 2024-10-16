2024/10/06
20:55

Status: #adult 
Tags: [[question]] [[linked list]]
# Intersection
# Question

Given two (singly) linked lists determine if the two list intersect return the intersecting node note that the intersection is defined based on reference not value that is if the kth node of the first linked list is the exact same node (by reference) as the jth node of the school linked list then they are intersecting
# Solution
i won't implement this question because i am to exhausted from working also i have chemistry homework i will do that so i will just write the explanation 

1. Run through each linked list to get the lengths and the tails. 

2. Compare the tails. If they are different (by reference, not by value), return immediately. There is no inter section. 

3. Set two pointers to the start of each linked list. 

4. On the longer linked list, advance its pointer by the difference in lengths. 

5. Now, traverse on each linked list until the pointers are the same.
# References

[[📙 Cracking The Coding Interviews]]