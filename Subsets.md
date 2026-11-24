## 01. Subsets

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/subsets-1613027340/1)

### Problem Description

**Task:** Given an array arr[] of distinct positive integers, your task is to find all its subsets.

> **Note:** You can return the subsets in any order, the driver code will print them in sorted order.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [1, 2, 3]
```
- **Output:**
```text
[[], [1], [1, 2], [1, 2, 3], [1, 3], [2], [2, 3], [3]]
```
- **Explanation:** The subsets of [1, 2, 3] in lexicographical order are: [], [1], [1, 2], [1, 2, 3], [1, 3], [2], [2, 3], [3]

##### Example 2

- **Input:**
```text
arr[] = [2, 4]
```
- **Output:**
```text
[[], [2], [2, 4], [4]] The subsets of [2, 4] in lexicographical order are: [], [2], [2, 4], [4]
```

#### Constraints

- **1.** `1 ≤ arr.size() ≤ 10 1 ≤ arr[i] ≤ 10³`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(2^n * n^2)
- **Expected Auxiliary Space Complexity:** O(n * 2^n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-08 12:10:57
- **Status:** Correct
- **Marks:** 4

```java
import java.util.*;
class Solution {
    public ArrayList<ArrayList<Integer>> subsets(int arr[]) {
        // code here
        //base case
    ArrayList<ArrayList<Integer>>ans=new ArrayList<>();
    generate(arr,0,new ArrayList<>(),ans);
    return ans;
    }
    public void generate(int[] arr,int index, ArrayList<Integer> current, ArrayList<ArrayList<Integer>>ans){
               // base case
               if(index==arr.length){
                   ans.add(new ArrayList<>(current));
                   return;
                   
               }
               //include
               current.add(arr[index]);
               generate(arr,index + 1,current,ans);
               // backtrack
               current.remove(current.size()-1);
               //exclude
               generate(arr,index + 1,current,ans);
           }
           
    }
```

*Generated on: 24/11/2026, 23:28:56*