## 01. N-Queen Problem

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/n-queen-problem0315/1)

### Problem Description

**Task:** The N-Queens puzzle is the problem of placing N queens on an N * N chessboard such that no two queens attack each other. Two queens attack each other if they are placed in the same row, the same column, or the same diagonal.
Given an integer n representing the number of queens, find all distinct solutions to this puzzle. Each solution should be represented as an array of size n, where the ith element (1-based indexing) denotes the column position of the queen placed in the ith row.

> **Note:** You may return the solutions in any order.

#### Examples

##### Example 1

- **Input:**
```text
n = 1
```
- **Output:**
```text
[1]
```
- **Explanation:** Only one queen can be placed in the single cell available.

##### Example 2

- **Input:**
```text
n = 4
```
- **Output:**
```text
[[2, 4, 1, 3], [3, 1, 4, 2]]
```
- **Explanation:** There are 2 possible solutions for n = 4.

##### Example 3

- **Input:**
```text
n = 3
```
- **Output:**
```text
[]
```
- **Explanation:** There are no possible solutions for n = 3.

#### Constraints

- **1.** `1 ≤ n ≤ 10`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n!)
- **Expected Auxiliary Space Complexity:** O(n^2)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-09 11:24:00
- **Status:** Correct
- **Marks:** 8

```java
class Solution {
    public ArrayList<ArrayList<Integer>> nQueen(int n) {
        // code here
        ArrayList<ArrayList<Integer>>ans=new ArrayList<>();
        int[]board=new int[n];
        solve(0,n,board,ans);
        return ans;
    }
    static void solve(int row,int n,int[]board,
       ArrayList<ArrayList<Integer>>ans){
           if(row==n){
        ArrayList<Integer>temp=new ArrayList<>();
        for(int i=0;i<n;i++){
            temp.add(board[i]+1);
        }
        ans.add(temp);
        return;
           }
           for(int col=0;col<n;col++){
               if(isSafe(row,col,board)){
                   board[row]=col;
                   solve(row+1,n,board,ans);
               }
           }
       }
       static boolean isSafe(int row,int col,int[]board){
           for(int i=0;i<row;i++){
               //same column
               if(board[i]==col)
               return false;
               //same diagonal
               if(Math.abs(board[i]-col)==Math.abs(i-row))
                   
               return false;
           }
           return true;
       }
}
```

*Generated on: 24/11/2026, 23:26:37*