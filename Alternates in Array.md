## 14. Alternates in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/print-alternate-elements-of-an-array/1)

### Problem Description

**Task:** You are given an array arr[], the task is to return a list elements of arr in alternate order (starting from index 0).Examples:Input: arr[] = [1, 2, 3, 4]Output: 1 3Explanation:Take first element: 1Skip second element: 2Take third element: 3Skip fourth element: 4Input: arr[] = [1, 2, 3, 4, 5]

#### Examples

##### Example 1

- **Output:**
```text
1 3 5Explanation:Take first element: 1Skip second element: 2Take third element: 3Skip fourth element: 4Take fifth element: 5
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-29 21:30:59
- **Status:** Correct
- **Marks:** 1

```java
import java.util.ArrayList;

class Solution {
    public ArrayList<Integer> getAlternates(int[] arr) {
        ArrayList<Integer> result = new ArrayList<>();

        for (int i = 0; i < arr.length; i += 2) {
            result.add(arr[i]);
        }

        return result;
    }
}
```

*Generated on: 11/5/2026, 01:06:45 AM*