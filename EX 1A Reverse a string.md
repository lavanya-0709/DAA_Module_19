# EX 1A Reverse a String
## DATE: 18/02/2025
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm
1.Start with a string s as input.

2.Check if the string is empty.

3.If it is empty, return the empty string.

4.Otherwise, take the last character of the string.

5.Recursively reverse the rest of the string (excluding the last character).

6.Concatenate the last character with the reversed rest and return the result.    

## Program:
```
/*
Program to implement Reverse a String
Developed by: LAVANYA S
Register Number: 212223230112
*/
def recursive_String(s):
    if(len(s)==0):
        return s
    return s[-1]+recursive_String(s[:-1])
a=(input())
b=recursive_String(a)
print(b)
```

## Output:
![image](https://github.com/user-attachments/assets/ea3eb5d9-f00c-4d7a-8b7d-99859806ad3c)


## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
