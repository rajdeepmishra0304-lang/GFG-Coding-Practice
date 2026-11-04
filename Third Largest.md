## 07. Third Largest

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/third-largest-element/1)

### Problem Description

**Task:** Given an array, arr[] of positive integers. Find the third largest element in it. Return -1 if the third largest element is not found.Examples:Input: arr[] = [2, 4, 1, 3, 5]Output: 3Explanation: The third largest element in the array [2, 4, 1, 3, 5] is 3.Input: arr[] = [10, 2]Output: -1Explanation: There are less than three elements in the array, so the third largest element cannot be determined.Input: arr[] = [5, 5, 5]Output: 5Explanation: In the array [5, 5, 5], the third largest element can be considered 5, as there are no other distinct elements.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-28 20:12:51
- **Status:** Correct
- **Marks:** 2

```java
import java.util.List;

class Solution {
    int thirdLargest(List<Integer> arr) {
        int n = arr.size();

        if (n < 3) {
            return -1;
        }

        int firstIdx = -1;
        int secondIdx = -1;
        int thirdIdx = -1;

        for (int i = 0; i < n; i++) {
            int currentVal = arr.get(i);

            if (firstIdx == -1 || currentVal > arr.get(firstIdx)) {
                thirdIdx = secondIdx;
                secondIdx = firstIdx;
                firstIdx = i;
            } 
            else if (secondIdx == -1 || currentVal > arr.get(secondIdx)) {
                thirdIdx = secondIdx;
                secondIdx = i;
            } 
            else if (thirdIdx == -1 || currentVal > arr.get(thirdIdx)) {
                thirdIdx = i;
            }
        }

        return arr.get(thirdIdx);
    }
}
```

*Generated on: 11/5/2026, 12:47:34 AM*