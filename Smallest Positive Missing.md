## 11. Smallest Positive Missing

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/smallest-positive-missing-number-1587115621/1)

### Problem Description

**Task:** You are given an integer array arr[]. Your task is to find the smallest positive number missing from the array.Note: Positive number starts from 1. The array can have negative integers too.Examples:Input: arr[] = [2, -3, 4, 1, 1, 7]

#### Examples

##### Example 1

- **Output:**
```text
3
```
- **Explanation:** Smallest positive missing number is 3.

##### Example 2

- **Input:**
```text
arr[] = [5, 3, 2, 5, 1]
```
- **Output:**
```text
1
```
- **Explanation:** Smallest positive missing number is 1.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-29 20:37:51
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public int missingNumber(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n; i++) {
            while (arr[i] > 0 && arr[i] <= n && arr[i] != arr[arr[i] - 1]) {
                int t = arr[i];
                arr[i] = arr[t - 1];
                arr[t - 1] = t;
            }
        }
        for (int i = 0; i < n; i++) {
            if (arr[i] != i + 1) {
                return i + 1;
            }
        }
        return n + 1;
    }
}
```

*Generated on: 11/5/2026, 12:57:10 AM*