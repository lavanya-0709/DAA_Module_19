# EX 1D Linear search
## DATE: 01/03/2025
## AIM:
To write a python program for a search function with parameter list name and the value to be searched using string values.



## Algorithm
1.Take a list of elements as input.

2.Read the target element to search.

3.Traverse each element in the list one by one.

4.If the current element matches the target, return "Found".

5.If the loop ends without a match, return "Not Found".

6.Display the result accordingly. 
 

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: LAVANYA S
Register Number: 212223230112
*/
def search(List,n):
    for i in range(len(List)):
        if List[i]==n:
            return True
    return False
List=[]
x=int(input())
for i in range(x):
    List.append((input()))
n=(input())
if(search(List,n)):
    print("Found")
else:
    print("Not Found")
```

## Output:

![image](https://github.com/user-attachments/assets/456f48c5-7906-4039-b747-85229ae9b94b)


## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
