## 01. Anagram

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/anagram-1587115620/1)

### Problem Description

**Task:** Given two non-empty strings s1 and s2, consisting only of lowercase English letters, determine whether they are anagrams of each other or not. Two strings are considered anagrams if they contain the same characters with exactly the same frequencies, regardless of their order.Examples:Input: s1 = "geeks" s2 = "kseeg"Output: true Explanation: Both the string have same characters with same frequency. So, they are anagrams.Input: s1 = "allergy", s2 = "allergyy" Output: false Explanation: Although the characters are mostly the same, s2 contains an extra 'y' character. Since the frequency of characters differs, the strings are not anagrams. Input: s1 = "listen", s2 = "lists" Output: false Explanation: The characters in the two strings are not the same — some are missing or extra. So, they are not anagrams.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n + m)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-06-21 16:40:59
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public static boolean areAnagrams(String s1, String s2) {
        // code here
        
        if(s1.length()!=s2.length()){
            // length check ke liye for nhi if use hota h
            return false;
        }
            int[] freq = new int[26];
            for(int i=0;i<s1.length();i++){
                freq[s1.charAt(i)-'a']++;
                freq[s2.charAt(i)-'a']--;
                
            }
            for(int count:freq){
                if(count !=0){
                return false;
            }
            }
            return true;
        }
    }
```

*Generated on: 24/11/2026, 23:52:52*