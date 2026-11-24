## 01. Kth Largest

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/kth-largest-element5034/1)

### Problem Description

**Task:** Given an array arr[] and a number k. The task is to find the k^th largest element in the array.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [3, 5, 4, 2, 9], k = 3
```
- **Output:**
```text
4
```
- **Explanation:** Third largest element in the array is 4.

##### Example 2

- **Input:**
```text
arr[] = [4, 3, 7, 6, 5], k = 5
```
- **Output:**
```text
3
```
- **Explanation:** Fifth largest element in the array is 3.

#### Constraints

- **1.** `1 <= k <= arr.size <= 10⁶`
- **2.** `-10⁴ <= arr[i] <= 10⁴^`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n log k)
- **Expected Auxiliary Space Complexity:** O(k)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-31 23:38:25
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public static int kthLargest(int arr[], int k) {
        // code here
        PriorityQueue<Integer>pq=new PriorityQueue<>();
        for(int i=0;i<arr.length;i++){
            pq.offer(arr[i]);
            
            if(pq.size()>k){
                pq.poll();
            }
        }
        return pq.peek();
    }
}
```

*Generated on: 24/11/2026, 23:35:21*