# EX 1B Merge Sort
## DATE: 22/02/2025
## AIM:
To write a python program to sort the first half of the list using merge sort with float values.

## Algorithm
1. Divide the array into two halves recursively until each sub-array has one element.

2.Use a merge() function to combine two sorted halves into a single sorted array.

3.In merge(), copy the left and right sub-arrays into temporary arrays.

4.Compare elements from both sub-arrays and place the smaller one into the original array.

5.Copy any remaining elements from both sub-arrays into the main array.

6.Repeat the process until the entire array is sorted.
  

## Program:
```
/*
Program to implement Merge Sort
Developed by: LAVANYA S
Register Number: 212223230112
*/
def merge(arr,l,m,r):
    n1 = m-l+1
    n2 = r-m
    L = [0] * (n1)
    R = [0] * (n2)
    for i in range(0,n1):
        L[i] = arr[l+i]
    for j in range(0,n2):
        R[j] = arr[m+j+1]
    i=j=0
    k=l
    while i<n1 and j<n2:
        if L[i]<R[j]:
            arr[k]=L[i]
            i+=1
        else:
            arr[k]=R[j]
            j+=1
        k+=1
    while i<n1:
        arr[k]=L[i]
        i+=1
        k+=1
    while j<n2:
        arr[k]=R[j]
        j+=1
        k+=1
    
def mergeSort(arr,l,r):
    if l < r:
        mid = (l+r)//2
        mergeSort(arr,mid+1,r)
        merge(arr,l,mid,r)
li=[]
n=int(input())
for i in range(n):
    li.append(float(input()))
print("Given array is")
for i in li:
    print(i,end=" ")
mergeSort(li,0,n-1)
print("\n\nSorted array is")
for i in li:
    print(i,end=" ")
```

## Output:

![image](https://github.com/user-attachments/assets/1f536080-7d02-4cf7-858e-5a8c1df9a927)


## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
