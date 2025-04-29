# EX 1B Merge Sort
## DATE: 19.2.25
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1. Input the number of elements and read the array from the user.

2. Divide the array recursively into two halves until each subarray has one element.

3. Merge the sorted subarrays by comparing elements from left and right parts.

4. Place the smaller element into the original array during the merging step.

5. Print the array before and after sorting to show the result.

## Program:
```
/*
Program to implement Merge Sort
Developed by: LISIANA T
Register Number:  212222240053
*/
def merge(arr,left,middle,right):
    n1 = middle - left + 1
    n2 = right - middle
    L = [0] * n1
    R = [0] * n2
    for i in range(n1):
        L[i] = arr[left + i]
    for j in range(n2):
        R[j] = arr[middle + 1 + j]
    i = j = 0
    k = left
    
    while i < n1 and j < n2:
        if L[i] <= R[j]:
            arr[k] = L[i]
            i+=1
        else:
            arr[k] = R[j]
            j+=1
        k+=1
    while i < n1:
        arr[k] = L[i]
        i+=1
        k+=1
    while j < n2:
        arr[k] = R[j]
        j+=1
        k+=1
        
def mergesort(arr,left,right):
    if left < right:
        middle = (left + right)//2
        mergesort(arr, middle+1, right)
        merge(arr, left, middle, right)
        
def print_sort(arr):
    for i in range(len(arr)):
        print(arr[i],end=' ')

n = int(input())
arr = [int(input()) for _ in range(n)]

print("Given array is")
print_sort(arr)
mergesort(arr,0,n-1)
print("\n\nSorted array is")
print_sort(arr)

```

## Output:

![image](https://github.com/user-attachments/assets/27f0d439-2f89-494b-a6cb-78e936ed339d)


## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
