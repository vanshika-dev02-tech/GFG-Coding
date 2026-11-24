## 01. Nearly Sorted

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/nearly-sorted-1587115620/1)

### Problem Description

**Task:** Given an array arr[], where each element is at most k positions away from its correct position in the sorted order. Your task is to restore the sorted order of arr[] by rearranging the elements in place.Examples:Input: arr[] = [2, 3, 1, 4], k = 2

#### Examples

##### Example 1

- **Output:**
```text
[7, 9, 14]Explanation: All elements are already stored in the sorted order.
```
- **Explanation:** All elements are at most k = 2 positions away from their correct positions.Element 1 moves from index 2 to 0Element 2 moves from index 0 to 1Element 3 moves from index 1 to 2Element 4 stays at index 3Input: arr[] = [7, 9, 14], k = 1

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n log k)
- **Expected Auxiliary Space Complexity:** O(k)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-08-03 00:44:48
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    public void nearlySorted(int[] arr, int k) {
        // code here
        PriorityQueue<Integer> pq= new PriorityQueue<>();
        int index=0;
        //first k+1 elements
        for(int i=0;i<=k;i++){
            pq.offer(arr[i]);
            
        }
        // remaining elements
        for(int i=k+1;i<arr.length;i++){
            arr[index++]=pq.poll();
            pq.offer(arr[i]);
        }
        // remaining heap elements
        while(!pq.isEmpty()){
            arr[index++]=pq.poll();
            
        }
    }
}
```

*Generated on: 24/11/2026, 23:34:04*