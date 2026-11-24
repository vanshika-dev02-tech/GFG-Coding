## 01. Friends Pairing Problem

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/friends-pairing-problem5425/1)

### Problem Description

**Task:** Given n friends, each one can remain single or can be paired up with some other friend. Each friend can be paired only once. Find out the total number of ways in which friends can remain single or can be paired up.Examples :Input: n = 3

#### Examples

##### Example 1

- **Output:**
```text
4 {1}, {2}, {3} : All single {1}, {2,3} : 2 and 3 paired but 1 is single. {1,2}, {3} : 1 and 2 are paired but 3 is single. {1,3}, {2} : 1 and 3 are paired but 2 is single. Note that {1,2} and {2,1} are considered same.
```

##### Example 2

- **Input:**
```text
n = 2
```
- **Output:**
```text
1
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-07 00:02:01
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    
        // code here
    long dp[];
    long calc(int n){
        if(n<3) return n;
        return dp[n]=(calc(n-1)+(n-1)*calc(n-2));
    }
    public long countFriendsPairings(int n){
        dp = new long[n+1];
        return calc(n);
    }
    
}
```

*Generated on: 24/11/2026, 23:17:03*