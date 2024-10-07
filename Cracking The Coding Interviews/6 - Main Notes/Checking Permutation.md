2024/10/04
18:50

Status: #adult 
Tags: [[question]]
# Checking Permutation


# Question

Given two strings, write a method to decide if one is a permutation of the other
# Solution

in this question you can ask interviewer we have to think about Uppercase letters for show you understood the problem in this problem we won't think about

to solve this problem we have 2 solution
# Solution 1 Sorting Way

this solution might be not very efficient but it is easy to understand so it is acceptable

```python
word1 = input()
word2 = input()

def isPermutation(word1, word2):

    if len(word1) != len(word2):
        return False

    word1 = sorted(word1)
    word2 = sorted(word2)

    if word1 == word2:
        return True
    else:
        return False

if isPermutation(word1,word2):
    print("YES")
else:
    print("NO")
```

Time Complexity
$O(n \log n)$

Space Complexity
$O(1)$
# Solution 2 Counting Way

this way is more efficient but it harder to come up with (it is not hard it just harder than other way)

```python
from collections import defaultdict

word1 = input()
word2 = input()

def isPermutation(word1,word2):
    word1_letter_count = defaultdict(int)
    for i in word1:
        word1_letter_count[i] += 1
    for i in word2:
        word1_letter_count[i] -= 1
        if word1_letter_count[i] < 0:
            return False

    return True

if isPermutation(word1,word2):
    print("YES")
else:
    print("NO")
```

Time Complexity
$O(N)$

Space Complexity
$O(N)$

# References

[[📙 Cracking The Coding Interviews]]