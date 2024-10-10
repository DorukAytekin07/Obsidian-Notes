2024/10/04
18:25

Status: #adult 
Tags: [[data structure]] [[arrays]] [[dynamic arrays]]
# ArrayList & And Resizable Arrays


# Quick Overview

in some languages arrays automatically resizable but is some languages they are not dynamically resizable you have to grow them when they are full

but even this languages they have a data structure that dynamically resize that is ArrayList they are very useful in interviews so id you use a language like that it will be better you get use to use this data structure

and big O complexities of this data structure
Access  Doubling Insertion
O(1)     O(N)     O(1)

# Detailed Research

arrays in the most of the programming languages are static typed this means before you use the array you have to initialize capacity of array after you use it 

but sometimes we don't know length of array we have to decide this is run time so for this we have to use a array typed dynamically but as i said arrays are static so for dynamic array use Array-lists (name of dynamic arrays are change by language to language in C++ we have vectors in Java we have Array-lists even in python we have directly have dynamic arrays called lists)

finally Big O Complexity Of this Data Structure
Access
$O(1)$

Resize (Doubling)
$O(N)$

Insertion
$O(1)$

Delete (Remove)
$O(1)$

# References

[[📙 Cracking The Coding Interviews#Arrays And Strings]]