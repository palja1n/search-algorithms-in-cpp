# Search Algorithms in C++

Name: Pal Jain  
Class: ENTC A3  
PRN: 24070123067  

**Aim:**
To understand various searching techniques in C++ and implement programs that locate elements in an array.

---

## Theory

Searching is the operation of locating a particular element within a data structure. Among the available techniques, **linear search** and **binary search** are the most commonly studied.

* **Linear Search:**
  This straightforward method checks each element one by one until the required element is found or the array ends. It can be applied on both sorted and unsorted arrays.

* **Binary Search:**
  A faster approach, but it requires the array to be sorted. The algorithm divides the array into halves and continues the search in the relevant half, reducing the comparisons drastically.

**Key Notes:**

* Linear search has a time complexity of **O(n)**.
* Binary search runs in **O(log n)** time.
* Binary search requires the input array to be sorted beforehand.

---

## Program 1: Linear Search (with function)

**Logic:**
A separate function is written to traverse the array. Each element is checked until a match is found. If found, the index is returned; otherwise, `-1` is returned.

**Algorithm:**

1. Start
2. Input array size
3. Enter array elements
4. Input the element to search
5. Traverse array sequentially

   * If match found → return index
   * Otherwise continue
6. If element not found → return -1
7. End

---

## Program 2: Linear Search (inside `main`)

**Logic:**
The search is directly performed in the `main()` function using a loop. A flag variable is used to indicate whether the element is present.

**Algorithm:**

1. Start
2. Input number of elements
3. Enter array elements
4. Input target element
5. Initialize a flag as `false`
6. Traverse array

   * If element matches → print index, set flag `true`, break
7. If flag remains `false` → print "Element not found"
8. End

---

## Program 3: Binary Search

**Logic:**
Since binary search works only on sorted data, two pointers `left` and `right` are used to maintain the search boundaries. The mid element is compared with the target and the search is continued accordingly.

**Algorithm:**

1. Start
2. Input number of elements
3. Input sorted array elements
4. Enter element to search
5. Initialize `left = 0`, `right = size-1`
6. Repeat while `left <= right`

   * Calculate `mid = (left + right)/2`
   * If `arr[mid] == element` → return index
   * Else if `arr[mid] < element` → search right half (`left = mid + 1`)
   * Else → search left half (`right = mid - 1`)
7. If not found → return -1
8. End

---

## Conclusion

Both **linear search** and **binary search** are fundamental searching methods. Linear search is simpler and can be used on any dataset, whereas binary search is significantly more efficient but restricted to sorted arrays. A clear understanding of these approaches helps in writing better and faster algorithms for data lookup.
