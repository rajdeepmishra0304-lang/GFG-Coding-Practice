## 01. Array Search

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/search-an-element-in-an-array-1587115621/1)

### Problem Description

**Task:** Given an array, arr[] of n integers, and an integer element x, find whether element x is present in the array. Return the index of the first occurrence of x in the array, or -1 if it doesn't exist.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** Not found
- **Expected Auxiliary Space Complexity:** Not found

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-20 14:24:41
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int search(int arr[], int x) {
        // code here
        for(int i=0; i<arr.length; i++){
            if(arr[i]==x){
                return i;
            }
            
        }
        return -1;
    }
}
```

*Generated on: 11/5/2026, 12:31:40 AM*