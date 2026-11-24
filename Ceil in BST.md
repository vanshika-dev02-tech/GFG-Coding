## 01. Ceil in BST

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/implementing-ceil-in-bst/1)

### Problem Description

**Task:** Given a root binary search tree and an integer x , find the Ceil of x in the tree.Ceil(x) is a number that is either equal to x or is immediately greater than x. If Ceil could not be found, return -1.Examples:Input: root = [5, 1, 7, N, 2, N, N, N, 3], x = 3

#### Examples

##### Example 1

- **Output:**
```text
3
```
- **Explanation:** We find 7 in BST, so ceil of 6 is 7.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-25 23:14:53
- **Status:** Correct
- **Marks:** 4

```java
/*
Definition for Node
class Node {
    int data;
    Node left, right;

    Node(int val) {
        this.data = val;
        left = right = null;
    }
} */

class Solution {
    int findCeil(Node root, int x) {
        // code here
        int ans=-1;
        while(root!=null){
            if(root.data==x){
                ans=root.data;
                return ans;
            }
            if(root.data<x){
                root=root.right;
                
            }
            else{
                ans=root.data;
                root=root.left;
            }
            
        }
        return ans;
    }
}
```

*Generated on: 24/11/2026, 23:55:35*