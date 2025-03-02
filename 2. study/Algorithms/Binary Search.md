- search a value in a sorted array by selecting the middle point and comparing it to the target value. If the the middle value is less than the target repeat the process for the values in front of the middle point.
- 

``` python
arr = [1,2,3,4,5]
target = 2
leftPointer = 0
rightPointer = len(arr)

while l < r :
	middlePointer = l + (r - l)//2
	if arr[middlePointer] == target:
		return middlePointer
	#if value in the middle is smaller than target search the front half
	elif arr[middlePointer] < target:
		r = m - 1
	else:
		l = m + 1
		

```