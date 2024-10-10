2024/10/04
18:57

Status: #adult 
Tags: [[question]] [[counting]]
# Palindrome Permutation
# Question

Given a string, write a function to check if it is a permutation of a palindrome. A palindrome is a word or phrase that is the same forwards and backwards. A permutation is a rearrangement of letters. The palindrome does not need to be limited to just dictionary  words

EXAMPLE
input: Tact Coa

output: True (Permutations: "taco cat" , "atco cta", etc.)


# Solution

in this question we can came up with 3 optimize solution and one of them is Counting Solution
# Counting Solution I

in this solution we count all the occurrence of each letter and if we find more than one odd count letter we will return False otherwise true because in palindrome we always have to have 2 and his multiples if we did not we cannot create a palindrome

```python
from collections import defaultdict

word = input()

def PalindromePermutation(word):
    characters_count = defaultdict(int)
    odd_character_count = 1
    
    for i in word:
        if i != " ":
            characters_count[i] += 1
    for i in characters_count.keys():
        if characters_count[i] % 2 == 1:
            odd_character_count -= 1
        if odd_character_count < 0:
            return False
    return True

if PalindromePermutation(word):
    print("True")
else:
    print("False")
```

Time Complexity
$O(N)$

Space Complexity
$O(N)$

# Counting Solution II

this solution have same complexity with previous one but (actually it is more optimal because of we have a less n for loop compare the other) but this is not important now we just write the solutions that we came up

```python
from collections import defaultdict

word = input()

def PalindromePermutation(word):
    characters_count = defaultdict(int)
    odd_character_count = 0
    
    for i in word:
        if i != " ":
            characters_count[i] += 1
            if characters_count[i] % 2 == 1:
                odd_character_count += 1
            else:
                odd_character_count -= 1
    if odd_character_count > 1:
        return False
    return True

if PalindromePermutation(word):
    print("True")
else:
    print("False")
```

Time Complexity
$O(N)$

Space Complexity
$O(N)$
# References

[[📙 Cracking The Coding Interviews]]