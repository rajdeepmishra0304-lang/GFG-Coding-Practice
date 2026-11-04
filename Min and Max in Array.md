## 13. Min and Max in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-minimum-and-maximum-element-in-an-array4428/1)

### Problem Description

**Task:** Given an array arr[]. Your task is to find the minimum and maximum elements in the array.Examples:Input: arr[] = [1, 4, 3, 5, 8, 6]

#### Examples

##### Example 1

- **Output:**
```text
[3, 15]Explanation: minimum and maximum element of array are 3 and 15.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-29 20:47:08
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public ArrayList<Integer> getMinMax(int[] arr) {
        int mini = arr[0];
        int maxi = arr[0];

        for (int i = 1; i < arr.length; i++) {
            if (arr[i] < mini) {
                mini = arr[i];
            }
            if (arr[i] > maxi) {
                maxi = arr[i];
            }
        }

        ArrayList<Integer> res = new ArrayList<>();
        res.add(mini);
        res.add(maxi);
        return res;
    }
}
```

*Generated on: 11/5/2026, 01:05:07 AM*