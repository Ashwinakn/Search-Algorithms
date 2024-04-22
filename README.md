# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:

Developed By: ASHWINA K N

Register Number: 212223230025

i)	#Use a linear search method to match the item in a list.
```
def search(array,key,n):
    for i in range(0,n):
        if array[i]==key:
            return i
        
    return-1
array=eval(input())
key=int(input())
array.sort()
print(array)
n=len(array)
result=search(array,key,n)
if result==-1:
    print("Element not found")
else:
    print("Element found at index:  {}".format(result))




```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binary(arr,key,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if arr[mid]==key:
            return mid
        elif arr[mid]<key:
            low=mid+1
        elif arr[mid]>key:
            high=mid-1
    return-1
arr=eval(input())
key=int(input())
arr.sort()
low,high=0,len(arr)-1
print(arr)
result= binary(arr,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index:  {}".format(result))

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def binary(arr,key,low,high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==key:
            return mid
        elif arr[mid]<key:
            return binary(arr,key,mid+1,high)
        elif arr[mid]>key:
           return binary(arr,key,low,mid-1)
    return-1
arr=eval(input())
key=int(input())
arr.sort()
low,high=0,len(arr)-1
print(arr)
result= binary(arr,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index:  {}".format(result))




```
## Sample Input and Output:

![EXP-7 1](https://github.com/Ashwinakn/Search-Algorithms/assets/152128332/bb2eb766-55c4-4e14-9b9f-6d7705e10aaf)


![EXP-7 2](https://github.com/Ashwinakn/Search-Algorithms/assets/152128332/62bc4389-4beb-4e07-a7c3-d67322996809)


![EXP-7 3](https://github.com/Ashwinakn/Search-Algorithms/assets/152128332/2528ff14-139b-42c7-9e97-de9a62b4c514)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.
