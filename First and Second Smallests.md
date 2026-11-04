## 12. First and Second Smallests

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-the-smallest-and-second-smallest-element-in-an-array3226/1)

### Problem Description

**Task:** Given an array, arr[] of integers, your task is to return the smallest and second smallest element in the array. If the smallest and second smallest do not exist, return -1.Examples:Input: arr[] = [2, 4, 3, 5, 6]

#### Examples

##### Example 1

- **Output:**
```text
[-1]
```
- **Explanation:** Only element is 1 which is smallest, so there is no second smallest element.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-29 20:45:37
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public ArrayList<Integer> minAnd2ndMin(int[] arr) {
        ArrayList<Integer> res = new ArrayList<>();

        int first = -1;
        int second = -1;

        for (int i = 0; i < arr.length; i++) {
            int current = arr[i];

            if (first == -1) {
                first = current;
            }
            else if (current < first) {
                second = first;
                first = current;
            }
            else if (current != first) {
                if (second == -1 || current < second) {
                    second = current;
                }
            }
        }

        if (second == -1) {
            res.add(-1);
            return res;
        }

        res.add(first);
        res.add(second);
        return res;
    }
}
```

*Generated on: 11/5/2026, 01:02:37 AM*