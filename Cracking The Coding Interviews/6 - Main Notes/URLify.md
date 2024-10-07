2024/10/04
18:54

Status: #adult 
Tags: [[question]]
# URLify
# Question

Write a method to replace all spaces in a string with '%20'. You may assume that string sufficient space at the end to hold the additional characters, and that you are given the "true" length of string 
# Solution

in this solution we use built in functions of python also if you select python as your main interview language you will be ease with it because in situations like that python have built in functions

```python
word = input()

words = word.split()

result = ""
times = 1

for i in words:
    result += i
    if times < len(words):
        result += "%20"
    times += 1
    
print(result)
```

Time Complexity
$O(N)$

Space Complexity
$O(1)$
# References

[[📙 Cracking The Coding Interviews]]