## 01. Min and Max in Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-minimum-and-maximum-element-in-an-array4428/1)

### Problem Description

**Task:** Given an array arr[]. Your task is to find the minimum and maximum elements in the array.Examples:Input: arr[] = [1, 4, 3, 5, 8, 6]

#### Examples

##### Example 1

- **Output:**
```text
[3, 15]Explanation: minimum and maximum element of array are 3 and 15.
```

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-06-04 11:57:33
- **Status:** Correct
- **Marks:** 1

```java
import java.util.ArrayList;
import java.util.Collections;

class Solution{
    public ArrayList<Integer> getMinMax(int[] arr) {
        ArrayList<Integer>sortedArr=new ArrayList<>();
        for(int num: arr){
            sortedArr.add(num);
        }
        //sorted Arraylist
        Collections.sort(sortedArr);
        
        ArrayList<Integer>result = new ArrayList<>();
    
        
        result.add(sortedArr.get(0));
        result.add(sortedArr.get(sortedArr.size()-1));
        return result;
        
    }
    public static void main(String[]args){
        int[]arr={1,4,3,5,8,6};
        Solution obj = new Solution();
        ArrayList<Integer>result= obj.getMinMax(arr);
        
        System.out.println(result.get(0)+" "+result.get(1));
        
    }
}
```

*Generated on: 24/11/2026, 23:18:39*