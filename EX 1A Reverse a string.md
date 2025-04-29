# EX 1A Reverse a String
## DATE:11.02.25
## AIM:
To Write a Program to Create a recursive function to reverse a string

## Algorithm
1. Take input string s.
2. If length of s is 0 or 1, return s (base case).
3. Otherwise, recursively call the function with s[1:].
4. Append s[0] to the result of the recursive call.
5. Return the final reversed string. 

## Program:
```
/*
Program to implement Reverse a String
Developed by: Nivetha A
Register Number: 212222230101
*/
```
```

def reverse_string(s):
    # Base case
    if len(s) <= 1:
        return s
    # Recursive case
    return reverse_string(s[1:]) + s[0]

# Get input from user
user_input = input()
reversed_str = reverse_string(user_input)
print(reversed_str)

```

## Output:
![image](https://github.com/user-attachments/assets/e9a32c25-a0de-45b9-a327-04c0226e5a4e)





## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
