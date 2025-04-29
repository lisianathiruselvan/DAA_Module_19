# EX 1A Reverse a String
## DATE:18.2.25
## AIM:
Write a python program to calculate the length of the given string using recursion

## Algorithm
1. Start by reading a string from the user.

2. Check if the string is empty ("").

3. If empty, return 0 as the base case of recursion.

4. If not empty, call the function recursively with the substring excluding the first character.

5. Add 1 to the result of the recursive call and return it.
  

## Program:
```
/*
Program to implement Reverse a String
Developed by: LISIANA T
Register Number:  212222240053
*/
def length(str):
    if str == "":
        return 0
    
    else:
        return 1+length(str[1:])
        
str = input()
print(f"length of {str} is {length(str)}")
```

## Output:
c
![image](https://github.com/user-attachments/assets/6834f717-db14-40c1-879f-8f3e6c330e98)



## Result:
The program successfully calculates the length of the input string using recursion. When the user provides an input string, the output displays the correct length by recursively counting each character until the end of the string is reached.
