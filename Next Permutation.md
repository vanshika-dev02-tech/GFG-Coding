## 01. Next Permutation

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/next-permutation5226/1)

### Problem Description

**Task:** Given an array of integers arr[] representing a permutation, implement the next permutation that rearranges the numbers into the lexicographically smallest greater (or next) permutation. If no next permutation exists, rearrange the numbers into the lowest possible order (i.e., sorted in ascending order). Examples:Input: arr[] = [2, 4, 1, 7, 5, 0]

#### Examples

##### Example 1

- **Output:**
```text
[3, 4, 5, 1, 2]
```
- **Explanation:** The next permutation of the given array is [3, 4, 5, 1, 2].

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-06-16 23:34:10
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    void nextPermutation(int[] arr) {
        // code here
        int breakPoint=-1;
        int index =-1;
        for(int i=arr.length-2;i>=0;i--){
            if(arr[i]<arr[i+1]){
                breakPoint=i;
                break;
            }
        }
        if(breakPoint==-1){
            reverse(arr,0);
            
        }else{
            for(int j=arr.length-1;j>=0;j--){
                if(arr[j]>arr[breakPoint]){
                    index=j;
                    break;
                }
            }
            int temp = arr[breakPoint];
            arr[breakPoint]=arr[index];
            arr[index]=temp;
            reverse(arr,breakPoint+1);
        }
    }
    void reverse(int[]arr,int start){
        int end=arr.length-1;
        while(start<end){
            int temp = arr[start];
            arr[start]=arr[end];
            arr[end]=temp;
            end--;
            start++;
        }
    }
}
```

*Generated on: 24/11/2026, 23:09:44*