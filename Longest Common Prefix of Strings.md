## 01. Longest Common Prefix of Strings

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/longest-common-prefix-in-an-array5129/1)

### Problem Description

**Task:** Given an array of strings arr[]. Return the longest common prefix among each and every strings present in the array. If there's no prefix common in all the strings, return "".Examples :Input: arr[] = ["geeksforgeeks", "geeks", "geek", "geezer"]

#### Examples

##### Example 1

- **Output:**
```text
""
```
- **Explanation:** There's no common prefix in the given strings.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n*min(|arri|))
- **Expected Auxiliary Space Complexity:** O(min(|arri|))

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-06-23 15:57:48
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public String longestCommonPrefix(String arr[]) {
        // code here
        if(arr.length==0){
            return"";
        
        }
        String prefix=arr[0];
        for(int i=1;i<arr.length;i++){
            while(!arr[i].startsWith(prefix)){
            prefix=prefix.substring(0,prefix.length()-1);
            if(prefix.length()==0){
                return"";
            }
            }
        }
        return prefix;
}
}
```

*Generated on: 24/11/2026, 23:37:53*