# Experiment No. 1

## Title

**Binary Search Using Recursion**

## Aim

To implement Binary Search using recursion on a sorted array and analyze its time and space complexity.

## Program

```c
#include <stdio.h> 
 
int binarySearch(int arr[], int low, int high, int key) 
{ 
    if (low > high) 
        return -1; 
 
    int mid = (low + high) / 2; 
 
    if (arr[mid] == key) 
        return mid; 
 
    else if (key < arr[mid]) 
        return binarySearch(arr, low, mid - 1, key); 
 
    else 
        return binarySearch(arr, mid + 1, high, key); 
} 
 
int main() 
{ 
    int arr[] = {10, 20, 30, 40, 50, 60, 70}; 
    int n = 7; 
    int key, result; 
 
    printf("Enter element to search: "); 
    scanf("%d", &key); 
 
    result = binarySearch(arr, 0, n - 1, key); 
 
    if (result == -1) 
        printf("Element not found"); 
    else 
        printf("Element found at index %d", result); 
 
    return 0; 
}
```

## Output

The terminal output of the program is shown below:

![Binary Search Terminal Output](https://github.com/vardashinde5-stack/BinarySearch/blob/main/Binary%20Search%20Terminal%20Output.png)

## Time Complexity

| Case         | Time Complexity |
| ------------ | --------------- |
| Best Case    | **O(1)**        |
| Average Case | **O(log n)**    |
| Worst Case   | **O(log n)**    |

### Explanation

In Binary Search, the sorted array is divided into two halves after every comparison. Therefore, the number of elements to be searched is reduced by half at each step.

Hence, the time complexity is:

**O(log n)**

The best case occurs when the required element is found at the middle position during the first comparison, giving **O(1)** time complexity.

## Space Complexity

The recursive implementation uses the function call stack.

* **Auxiliary Space:** **O(log n)**
* This is because the maximum recursion depth is proportional to the height of the binary search process.

## Applications

1. Used for searching elements in sorted arrays.
2. Used for searching records in databases.
3. Used in dictionary and symbol-table lookups.
4. Useful for searching large datasets efficiently.
5. Used as a fundamental searching technique in computer science.
6. Can be used in problems involving sorted data and range searching.

## Conclusion

Binary Search is an efficient searching technique that works on a sorted array. It repeatedly divides the search space into two halves until the required element is found or the search space becomes empty.

The recursive implementation has a time complexity of **O(log n)** in the average and worst cases and requires **O(log n)** auxiliary space due to the recursion stack.

## GitHub Repository

[Binary Search - GitHub](https://github.com/vardashinde5-stack/BinarySearch)

## Output Image

[Binary Search Terminal Output](https://github.com/vardashinde5-stack/BinarySearch/blob/main/Binary%20Search%20Terminal%20Output.png)
