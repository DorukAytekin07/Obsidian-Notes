2024/10/19
21:25

Status: #adult 
Tags: [[question]] [[sorting]] [[stacks]]
# Sort Stacks
# Question
Write a program to sort a stack such that the smallest items are on the top you can use additional temporary buffer but you may not copy the elements into any other data structure (such as array) the stack supports the following operations push pop peek and isEmpty 
# Solution
to sort these stacks we will two stacks with this algorithm we have two stacks s1 and s2 s1 our unsorted stacks and s2 will sorted stack we pop values from s1 for place to s2 and we will add s2 when next value is smaller than it and if next value is bigger than it we will pop this bigger value and add this value to s1 stacks and we will iterate this until s1 stack is empty with isEmpty() function that we already implemented
for better understanding look to the book

Page 237
# References

[[📙 Cracking The Coding Interviews#Stack And Queues]]