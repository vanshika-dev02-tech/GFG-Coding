## 01. Solve the Sudoku

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/solve-the-sudoku-1587115621/1)

### Problem Description

**Task:** Given a 9*9 matrix mat[][] representing an incomplete Sudoku puzzle. Each cell contains a digit from 0 to 9, where 0 represents an empty cell and non-zero digits represent fixed values. Fill the empty cells to complete the puzzle. It is guaranteed that the puzzle has exactly one valid solution.A valid Sudoku solution must satisfy the following conditions:Each digit from 1 to 9 appears exactly once in every row.Each digit from 1 to 9 appears exactly once in every column.Each digit from 1 to 9 appears exactly once in each of the nine 3*3 subgrids.Examples:Input: mat[][] =

#### Examples

##### Example 1

- **Output:**
```text
Explanation: Each row, column and 3 x 3 box of the output matrix contains unique numbers.
```
- **Explanation:** Each row, column and 3 x 3 box of the output matrix contains unique numbers.Input: mat[][] =

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(9 ^ (n * n))
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-07-10 21:36:39
- **Status:** Correct
- **Marks:** 8

```java
class Solution {
     public void solveSudoku(int[][] mat) {
         solve(mat);
        // code here
        
    }
    static boolean solve(int[][]mat){
        for(int row=0;row<9;row++){
            for(int col=0;col<9;col++){
                if(mat[row][col]==0){
                    for(int num=1;num<=9;num++){
            if(isSafe(mat,row,col,num)){
                mat[row][col]=num;
                if(solve(mat))
                return true;
                mat[row][col]=0;
            }
                    }
                    return false;
                }
            }
        }
        return true;
    
    }
    static boolean isSafe(int[][]mat,int row,int col,int num){
        for(int j=0;j<9;j++){
            if(mat[row][j]==num)
            return false;
        }
        for(int i=0;i<9;i++){
        if(mat[i][col]==num)
        return false;
        }
        int sr=(row/3)*3;
        int sc=(col/3)*3;
        for(int i=sr;i<sr+3;i++){
        for(int j=sc;j<sc+3;j++){
            if(mat[i][j]==num)
            return false;
        }
        }
        return true;
    }
}
```

*Generated on: 24/11/2026, 23:24:04*