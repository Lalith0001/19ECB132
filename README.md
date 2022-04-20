# python 3 program to implement
# binary search in sorted array

def binarySearch(arr, low, high, key):
	# low + (high - low)/2
	mid = (low + high)/2

	if (key == arr[int(mid)]):
		return mid

	if (key > arr[int(mid)]):
		return binarySearch(arr,
		(mid + 1), high, key)

	if (key < arr[int(mid)]):
		return binarySearch(arr,low, (mid-1), key)
	
	return 0

# Driver program to check above functions
# Let us search 3 in below array
arr = [5, 6, 7, 8, 9, 10]
n = len(arr)
key = 10
print("Index:", int(binarySearch(arr, 0, n-1, key) ))

# This code is contributed by
#LALITH
