# EX 1C Quick Sort
## DATE:25.2.25
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of string values.

## Algorithm
1. Input the number of elements and read the array from the user.

2. Select a pivot element (first element of the subarray) for partitioning.

3. Rearrange elements such that all smaller elements go to the left and larger to the right of the pivot.

4. Recursively apply the Quick Sort to the left and right subarrays around the pivot.

5. Print the sorted array after the sorting process is complete.
## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of string values.
Developed by: LISIANA T
Register Number:  212222240053
*/
def quickSort(alist, start, end):
    if end - start > 1:
        p = partition(alist, start, end)
        quickSort(alist, start, p)
        quickSort(alist, p + 1, end)
 
def partition(alist, start, end):
    pivot = alist[start]
    i = start + 1
    j = end - 1
    #print("Pivot: ",pivot)
    while True:
        while (i <= j and alist[i] <= pivot):
            i = i + 1
        while (i <= j and alist[j] >= pivot):
            j = j - 1
 
        if i <= j:
            alist[i], alist[j] = alist[j], alist[i]
        else:
            alist[start], alist[j] = alist[j], alist[start]
            return j

arr = []
n=int(input())
for i in range(n):
    arr.append(input())
quickSort(arr, 0, n)
print("Sorted array is:")
for i in arr:
    print(i)
```

## Output:

![image](https://github.com/user-attachments/assets/bb96a33f-16d6-488f-bb57-e8ffdde71b3a)



## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
