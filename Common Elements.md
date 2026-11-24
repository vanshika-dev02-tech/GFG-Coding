## 01. Common Elements

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/common-elements5420/1)

### Problem Description

**Task:** Given two integer arrays a[] and b[], return an array containing all elements common to both arrays in sorted order. If an element appears multiple times in both arrays, it should appear in the output as many times as it is common to both arrays.Example:Input: a[] = [3, 4, 2, 2, 4] , b[] = [3, 2, 2, 7]

#### Examples

##### Example 1

- **Output:**
```text
[2, 2, 3]
```
- **Explanation:** The common elements in sorted order are 2, 2, 3.Input: a[] = [3, 6, 1, 7, 9, 8, 2, 2] , b[] = [9, 7, 3, 4, 9]Output: [3, 7, 9]Explanation: The common elements in sorted order are 3, 7, 9.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O((n+m)*log(n+m))
- **Expected Auxiliary Space Complexity:** O(n + m)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-06-25 22:11:21
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public static ArrayList<Integer> commonElements(int a[], int b[]) {
        // Your code here
        ArrayList<Integer>result=new ArrayList<>();
        Arrays.sort(a);
        Arrays.sort(b);
        
        int i=0,j=0;
        while (i<a.length && j<b.length){
            if(a[i]<b[j]){
                i++;
            }
            else if(b[j]<a[i]){
                j++;
            } else{
              
                 
                      
                   result.add(a[i]);
               
                i++;
                j++;
                
        
            }
        }
        return result;
        
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-06-25 22:07:23
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public static ArrayList<Integer> commonElements(int a[], int b[]) {
        // Your code here
        ArrayList<Integer>result=new ArrayList<>();
        Arrays.sort(a);
        Arrays.sort(b);
        
        int i=0,j=0;
        while (i<a.length && j<b.length){
            if(a[i]<b[j]){
                i++;
            }
            else if(b[j]<a[i]){
                j++;
            } else{
              
                 
                      
                   result.add(a[i]);
               
                i++;
                j++;
                
        
            }
        }
        return result;
        
    }
}
```

*Generated on: 24/11/2026, 23:49:06*