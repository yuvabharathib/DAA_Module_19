# EX 1B Merge Sort
## DATE:
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1. Take an integer `n` as input which represents the number of elements in the list.  
2. Read `n` floating-point numbers from the user and store them in a list `S`.  
3. If the length of the list is more than 1, find the middle index and divide the list into two halves `l` and `r`.  
4. Recursively apply `Merge_Sort` to both halves `l` and `r`.  
5. Merge the two sorted halves by comparing elements and placing them in order back into the original list. Copy any remaining elements from `l` or `r` to the original list. 

## Program:
```python
Program to implement Merge Sort
Developed by: Yuvabharathi.B
Register Number: 212222230181
def merge_sort(x):
    if len(x)<2:
        return x
    result=[]
    mid=int(len(x)/2)
    y=merge_sort(x[:mid])
    z=merge_sort(x[mid:])
    i=0
    j=0
    while i<len(y) and j<len(z):
        if y[i]>z[j]:
            result.append(z[j])
            j+=1
        else:
            result.append(y[i])
            i+=1
    result+=y[i:]
    result+=z[j:]
    return result
inp_arr=[]
n=int(input())
for i in range(n):
    inp_arr.append(float(input()))
print("Input Array:")
print(inp_arr)
print("Sorted Array:")
print(merge_sort(inp_arr)) 
```

## Output:

![Screenshot 2025-04-29 135320](https://github.com/user-attachments/assets/0f357b7f-2d4f-4c3d-810c-4755fd9481a4)


## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
