```python
def linear_search(data, target):
    """
    Performs a linear search on the given data list to find the index of the target element.

    Args:
        data: The list of elements to search through.
        target: The element to search for.

    Returns:
        The index of the target element if found, otherwise -1.
    """

    for i in range(len(data)):
        if data[i] == target:
            return i

    return -1

# Get user input for the data list
data = []
while True:
    value = input("Enter an element (or 'done' to finish): ")
    if value.lower() == 'done':
        break
    data.append(value)

# Get user input for the target element
target = input("Enter the element to search for: ")

# Perform linear search and print the result
index = linear_search(data, target)
if index != -1:
    print(f"Element found at index: {index}")
else:
    print("Element not found in the list.")
```


```python
def binary_search(arr, target):
    """
    Performs binary search on a sorted list to find the index of the target element.

    Args:
        arr (list): The sorted list to search in.
        target (int): The element to search for.

    Returns:
        int: The index of the target element if found, otherwise -1.
    """

    low = 0  # Initialize the starting index
    high = len(arr) - 1  # Initialize the ending index

    while low <= high:  # Continue searching while the search space is valid
        mid = (low + high) // 2  # Calculate the middle index
        if arr[mid] == target:  # Check if the target is found
            return mid
        elif arr[mid] < target:  # If the target is greater, search in the right half
            low = mid + 1
        else:  # If the target is smaller, search in the left half
            high = mid - 1

    return -1  # Target not found

# Get user input for the sorted list
sorted_list = []
while True:
    num = input("Enter a number (or 'q' to quit): ")
    if num.lower() == 'q':
        break
    try:
        sorted_list.append(int(num))
    except ValueError:
        print("Invalid input. Please enter a number.")

sorted_list.sort()  # Ensure the list is sorted

# Get user input for the target element
target = int(input("Enter the target element to search for: "))

# Perform binary search
index = binary_search(sorted_list, target)

if index != -1:
    print("Target found at index:", index)
else:
    print("Target not found in the list.")
```


```python
def find_max_min(arr):
    """
    Finds the maximum and minimum elements in a list using divide-and-conquer.

    Args:
        arr (list): The list to search.

    Returns:
        tuple: A tuple containing the maximum and minimum elements.
    """

    if len(arr) == 1:  # Base case: single element
        return arr[0], arr[0]

    mid = len(arr) // 2  # Calculate the middle index
    max_left, min_left = find_max_min(arr[:mid])  # Find max and min in the left half
    max_right, min_right = find_max_min(arr[mid:])  # Find max and min in the right half

    return max(max_left, max_right), min(min_left, min_right)

# Get user input for the list
arr = []
while True:
    num = input("Enter a number (or 'q' to quit): ")
    if num.lower() == 'q':
        break
    try:
        arr.append(int(num))
    except ValueError:
        print("Invalid input. Please enter a number.")

if not arr:
    print
```


```python

```
