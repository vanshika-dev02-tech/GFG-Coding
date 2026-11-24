## 01. Reverse a String

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-a-string/1)

### Problem Description

**Task:** Given a string s, reverse the string.Examples:Input: s = "Geeks"

#### Examples

##### Example 1

- **Output:**
```text
"skeeG"
```

##### Example 2

- **Input:**
```text
s = "for"
```
- **Output:**
```text
"a"
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-06-21 14:50:44
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public static String reverseString(String s) {
        // code here
        String reverse="";
        int n=s.length();
        for(int i=n-1;i>=0;i--){
           char ch = s.charAt(i);
            reverse=reverse + s.charAt(i);
        }
        return reverse;
    }
}
```

*Generated on: 24/11/2026, 23:20:43*