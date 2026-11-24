## 01. Search in Rotated Sorted Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/search-in-a-rotated-array4618/1)

### Problem Description

**Task:** Given an array arr[] of distinct elements, which was initially sorted in ascending order but then rotated at some unknown pivot, the task is to find the index of a target key. If the key is not present in the array, return -1.Examples :Input: arr[] = [5, 6, 7, 8, 9, 10, 1, 2, 3], key = 3

#### Examples

##### Example 1

- **Output:**
```text
1
```
- **Explanation:** 42 is found at index 1.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-06-16 22:49:01
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    int search(int[] arr, int key) {
        // code here
        int l=0;
        int r=arr.length-1;

    
        
        //binary search wala logic
        while(l<=r){
            int m=(l+r)/2;
            if(arr[m]==key){
                return m;
            }
            if(arr[l]<=arr[m]){
                if(key>=arr[l] && key<arr[m]){
                    r =m-1;
                }else{
                    l=m+1;
                }
            }
            else{
            if(key>=arr[m]&& key<=arr[r]){
                l=m+1;
            }
         else{
             r=m-1;
         }
            }
        }
        return -1;
    }
}
```

*Generated on: 24/11/2026, 23:30:42*