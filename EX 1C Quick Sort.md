# EX 1C Quick Sort
## DATE:18.02.25
## AIM:
Write a python program to implement quick sort on the given float  array values.

## Algorithm
1. Select a pivot element from the array (commonly the first or last element).
2. Partition the array into two subarrays: elements less than pivot and elements greater than or equal to pivot.
3. Place the pivot between the two subarrays at its correct position.
3. Recursively apply Quick Sort to the left subarray.
4. Recursively apply Quick Sort to the right subarray. 

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: Nivetha A
Register Number: 212222230101
*/
```
```
def qsort(L):
    if L==[]:
        return[]
    pivot=L[0:1]
    left=qsort([x for x in L[1:]if x<L[0]])
    right=qsort([x for x in L[1:]if x>=L[0]])
    print("left: ",left)
    print("right: ",right)
    return left+pivot+right
list1=[]
n=int(input())
for i in range(n):
    list1.append(float(input()))
print(qsort(list1))
 ```

## Output:
![image](https://github.com/user-attachments/assets/60f6f2e2-4dd2-429f-aff9-50e450fc6ff5)


## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
