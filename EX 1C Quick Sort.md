# EX 1C Quick Sort
## DATE: 25/02/2025
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm
1.Choose a pivot element (last element in this case).

2.Partition the array so that all elements smaller than or equal to the pivot are on the left, and others on the right.

3.Place the pivot in its correct sorted position.

4.Recursively apply the same process to the left and right sub-arrays.

5.Stop when sub-arrays have only one or zero elements.

6.The entire array becomes sorted as recursion unwinds. 

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: LAVANYA S
Register Number: 212223230112 
*/
def quickSort(arr,l,r):
    if len(arr)==1:
        return arr
    if l<r:
        p=partition(arr,l,r)
        quickSort(arr,l,p-1)
        quickSort(arr,p+1,r)
def partition(arr,l,r):
    pivot,ptr=arr[r],l
    for i in range(l,r):
        if(arr[i]<=pivot):
            arr[i],arr[ptr]=arr[ptr],arr[i]
            ptr+=1
    arr[ptr],arr[r]=arr[r],arr[ptr]
    return ptr
arr=[]
n=int(input())
for i in range(n):
    arr.append(float(input()))
quickSort(arr,0,n-1)
print("Sorted array is:")
for i in range(n):
    print("%.1f"%arr[i])

```

## Output:
![image](https://github.com/user-attachments/assets/58a64d69-de15-42e2-a8a4-ff2c768f9de3)



## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
