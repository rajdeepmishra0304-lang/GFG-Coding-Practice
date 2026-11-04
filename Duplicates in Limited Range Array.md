## 16. Duplicates in Limited Range Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-duplicates-in-an-array/1)

### Problem Description

**Task:** Given an array arr[] of size n, containing elements from the range 1 to n, and each element appears at most twice, return an array of all the integers that appears twice.Note: You can return the elements in any order but the driver code will print them in sorted order.Examples:Input: arr[] = [2, 3, 1, 2, 3]

#### Examples

##### Example 1

- **Output:**
```text
[2, 3]
```
- **Explanation:** 2 and 3 occur more than once in the given array.Input: arr[] = [3, 1, 2] Output: []Explanation: There is no repeating element in the array, so the output is empty.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-29 21:45:02
- **Status:** Correct
- **Marks:** 2

```java
import java.util.ArrayList;

class Solution {
    public ArrayList<Integer> findDuplicates(int[] arr) {
        int n = arr.length;
        ArrayList<Integer> result = new ArrayList<>();

        int[] count = new int[n + 1];

        for (int i = 0; i < n; i++) {
            int currentNum = arr[i];
            count[currentNum]++;
        }

        for (int i = 1; i <= n; i++) {
            if (count[i] == 2) {
                result.add(i);
            }
        }

        return result;
    }
}
```

*Generated on: 11/5/2026, 01:08:02 AM*