# EX 1B Merge Sort
## DATE:15.02.25
## AIM:
To Write a Program for Implementing merge sort using python recursion

## Algorithm
1. If the array has more than one element, split it into two halves.
2. Recursively apply merge sort on both halves.
3. Compare elements of both halves and merge them into a sorted array.
4. Copy any remaining elements from the left or right half.
5. Return the fully sorted array.  

## Program:
```
/*
Program to implement Merge Sort
Developed by:Nivetha A
Register Number: 212222230101
*/
```

```
def merge(left, right):
    result = []
    i = j = 0
    # Merge the two sorted halves
    while i < len(left) and j < len(right):
        if left[i] < right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    # Append remaining elements
    result.extend(left[i:])
    result.extend(right[j:])
    return result

def merge_sort(arr):
    # Base case: If the array has one or zero elements, it's already sorted
    if len(arr) <= 1:
        return arr
    
    # Divide the array into two halves
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])  # Recursively sort the left half
    right = merge_sort(arr[mid:])  # Recursively sort the right half

    # Merge the sorted halves
    return merge(left, right)

# Input handling
n = int(input())
arr = []

for _ in range(n):
    val = int(input())
    arr.append(val)

print("Given array is")
print(*arr)  # Print the original array
sorted_arr = merge_sort(arr)
print("Sorted array is")
print(*sorted_arr)  # Print the sorted array


```

## Output:
![image](https://github.com/user-attachments/assets/c3d4ffd9-8f64-409a-8aee-3bee3effaadc)



## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
