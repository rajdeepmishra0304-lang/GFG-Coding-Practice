## 10. Remove Consonants

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/c-program-to-remove-consonants-from-a-string1945/1)

### Problem Description

**Task:** Given a string s, remove all consonants and return the modified string containing only vowels.
If the string does not contain any vowels, return an empty string.

#### Examples

##### Example 1

- **Input:**
```text
s = "abEkipo"
```
- **Output:**
```text
"aEio"
```
- **Explanation:** a, E, i, o are only vowels in the string.

##### Example 2

- **Input:**
```text
s = "rrty"
```
- **Output:**
```text
""Explanation: There are no vowels.
```

#### Constraints

- **1.** `1 ≤ n ≤ 10⁵, n is length of the stringThe string should consist of only alphabets.`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-09-29 20:35:30
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public String remConsonants(String s) {
        StringBuilder sb = new StringBuilder();

        for (int i = 0; i < s.length(); i++) {
            char ch = s.charAt(i);
            if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' ||
                ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U') {
                sb.append(ch);
            }
        }

        return sb.toString();
    }
}
```

*Generated on: 11/5/2026, 12:54:12 AM*