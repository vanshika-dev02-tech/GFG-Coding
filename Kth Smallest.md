## 01. Kth Smallest

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/kth-smallest-element5635/1)

### Problem Description

**Task:** Given an integer array arr[] and an integer k, find and return the k^th smallest element in the given array.Examples :Input: arr[] = [10, 5, 4, 3, 48, 6, 2, 33, 53, 10], k = 4Output: 5

#### Examples

##### Example 1

- **Explanation:** 3rd smallest element in the given array is 7.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n log k)
- **Expected Auxiliary Space Complexity:** O(k)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-31 23:45:28
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public int kthSmallest(int[] arr, int k) {
        // Code here
        PriorityQueue<Integer>pq=new PriorityQueue<>(Collections.reverseOrder());
        for(int i=0; i<arr.length; i++){
            pq.offer(arr[i]);
            if(pq.size()>k){
                pq.poll();
            }
        }
        return pq.peek();
    }
}
```

*Generated on: 24/11/2026, 23:32:39*