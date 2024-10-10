2024/10/04
18:43

Status: #adult 
Tags: [[question]] [[hash table]]
# Is Unique

# Question

Implement an algorithm to determine if a string has all unique characters. What if you cannot use additional data structure

# Solution

this is the exactly solution that wanting from question and the time and space complexity is
Time           Space
$O(N^2)$           $O(1)$

but as you see question says us to we cannot use additional data structure 

what if we can use additional data structure in this station we have better solution than O($N^2$)

```python
word1 = input()
word2 = input()

is_unique = True

for i in range(len(word1)):
    for j in range(len(word2)):
        if word1[i] == word2[j]:
            is_unique = False

if is_unique:
    print("The words has no common letter")
else:
    print("words has common letters")
```

Hash Table Solution
this solution is more efficient as a time complexity but in space complexity it grows to $O(N)$ complexity
Time Complexity         Space Complexity
     $O(N)$                    $O(N)$

```python
from collections import defaultdict

word1 = input()
word2 = input()

is_unique = True

character_of_word1 = defaultdict(int)

for i in word1:
    character_of_word1[i] += 1
for i in word2:
    if i in character_of_word1:
        is_unique = False

if is_unique:
    print("words have no common letter")
else:
    print("words have common letter")
```
# References

[[📙 Cracking The Coding Interviews]]