#Kanokporn Hudsree 1630902656 ++ CE312 Homework:Lab 9 ++ Section 336B

arr = [7,10,12,14,16,20,29,37]
def linear_search(values, search_for):
   search_at = 0
   search_res = False
	
   while search_at < len(values) and search_res is False:
      if values[search_at] == search_for:
         search_res = True
      else:
         search_at = search_at + 1
   return search_res

print("In Element have 14 is % s" %linear_search(arr, 14))
print("In Element have 29 is % s" %linear_search(arr, 29))

def binarySearch(arr, l, r, x):
	if r >= l:

		mid = l + (r - l) // 2
		if arr[mid] == x:
			return mid
		elif arr[mid] > x:
			return binarySearch(arr, l, mid-1, x)
		else:
			return binarySearch(arr, mid + 1, r, x)
	else:
		return -1

x = 14
result = binarySearch(arr, 0, len(arr)-1, x)

if result != -1:
	print("Element(14) is present at index % d" % result)
else:
	print("Element(14) is not present in array")
	
y = 29	
result1 = binarySearch(arr, 0, len(arr)-1, y)

if result1 != -1:
	print("Element(29) is present at index % d" % result1)
else:
	print("Element(29) is not present in array")	

