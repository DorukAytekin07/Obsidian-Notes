2024/10/04
19:06

Status: #child 
Tags: [[question]] [[two pointer]]
# String Compression
# Question

Implement a method  to perform basic string compression using the counts of repeated characters. For example, the string aabcccccaaa would become a2b1c5a3 if the "compressed" string would not become smaller than the original string , your method should return the original string. You can assume the string has only uppercase and lowercase letters (a-z)

# Solution

it is a clear two pointer question it is very upon to understand so i just say two pointer not anything other

```python
sentence = input()

def StringCompression(sentence):
    fast = 1
    slow = 0
    result = ""
    while fast < len(sentence):
        if sentence[fast] != sentence[slow]:
            result += sentence[slow] + str(fast - slow)
            slow = fast

        fast += 1
    result += sentence[slow] + str(fast - slow)
    return result

if len(StringCompression(sentence)) < len(sentence):
    print(StringCompression(sentence))
else:
    print(sentence)
```

# References

[[📙 Cracking The Coding Interviews]]