2024/10/04
19:19

Status: #adult  
Tags: [[question]] [[string]]
# String Rotation
# Question

Assume you have a method isSubstring which checks if one word is a substring of another. Given two strings s1 and s2 write code to check if s2 is a rotation of s1 using only one call to isSubstring

EXAMPLE
waterbottle -> erbottlewat
# Solution

to solve this question you  have to assume we have a method for checking s1 is substring of s2 if you understand this we can start the solution

```Python
def isRotation(s1,s2):
	if len(s1) == len(s2) and len(s1) > 0:
		s1s1 = s1 + s1
		return isSubstring(s1s1,s2)
	return False
```

Time Complexity
$O(A + B)$ or $O(N)$

Space Complexity
$O(1)$
# References

[[📙 Cracking The Coding Interviews]]