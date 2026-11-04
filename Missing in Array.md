## 08. Missing in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/missing-number-in-array1416/1)

### Problem Description

**Task:** Given an array arr[] of size n - 1 containing distinct integers in the range [1, n]. The array represents a permutation of the integers from 1 to n with exactly one element missing.

Find and return the missing element.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** Not found
- **Expected Auxiliary Space Complexity:** Not found

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-28 20:13:51
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    int missingNum(int[] arr) {
        long n = arr.length + 1;
        long s1 = (n * (n + 1)) / 2;
        long s2 = 0;
        for (int i = 0; i < arr.length; i++) {
            s2 += arr[i];
        }
        return (int)(s1 - s2);
    }
}
```

*Generated on: 11/5/2026, 12:49:08 AM*