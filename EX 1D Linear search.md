# EX 1D Linear search
## DATE: 1.3.25
## AIM:
To write a python program for a search function with parameter list name and the value to be searched 



## Algorithm

1. Input the number of elements and store the elements in a list.

2. Read the target element to be searched in the list.

3. Traverse the list using a loop to compare each element with the target.

4. Return the index if a match is found; otherwise, return -1.

5. Display "Found" if the element exists, else display "Not Found".

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: LISIANA T
Register Number:  212222240053
*/
def search(List1,n):
    for i in range(len(List1)):
        if (List1[i]==n):
            return i
    return -1
List = [] 
x=int(input())
for i in range(x):
    List.append(input())
n =input()
value = search(List, n)
if value!=-1:
	print("Found")
else:
	print("Not Found")

```

## Output:

![image](https://github.com/user-attachments/assets/96ea5f9a-a137-4b89-8347-a97f6c582481)


## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
