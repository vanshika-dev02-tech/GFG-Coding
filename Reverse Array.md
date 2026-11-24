## 01. Reverse Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-an-array/1)

### Problem Description

**Task:** Given an array of integers arr[], reverse the array in place.Examples:Input: arr = [1, 4, 3, 2, 6, 5]

#### Examples

##### Example 1

- **Output:**
```text
[1]Explanation: The array has only single element, hence the reversed array is same as the original.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-06-04 12:43:42
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public void reverseArray(int arr[]) {
        // code here
        int a[]={1,2,3,4};
        int i=0, j= arr.length-1,temp;
        while(i<j){
            temp = arr[i];
            arr[i]=arr[j];
            arr[j]=temp;
            i++;
            j--;
        }
        
    }
}
```

*Generated on: 24/11/2026, 23:19:39*