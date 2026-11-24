## 01. Java ArrayList Operations

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/arraylist-operations/1)

### Problem Description

**Task:** Implement the following operations on an ArrayList < Integer > a:void add(ArrayList < Integer > a, int x): Add the element x to the end of the ArrayList.int remove(ArrayList < Integer > a): Remove and return the last element of the ArrayList. If the ArrayList is empty, return -1.int get(ArrayList < Integer > a, int index): Return the element at the specified index. If the ArrayList is empty, return -1.void reverse(ArrayList < Integer > a): Reverse the order of the elements in the ArrayList.void sort(ArrayList < Integer > a): Sort the elements of the ArrayList in ascending order.int size(ArrayList < Integer > a): Return the number of elements currently present in the ArrayList.You are given a sequence of q queries, represented in numeric form:1 x - Call add(a, x)2 - Call remove(a)3 index - Call get(a, index)4 - Call reverse(a)5 - Call sort(a)6 - Call size(a)The driver code will process the queries, call the corresponding functions, and print the outputs of remove(), get(), and size() operations. You only need to implement the above six functions.Examples:Input: queries[][] = [[1, 10], [1, 5], [1, 20], [2], [3, 1], [4], [6]]Output: [20, 5, 2]Explanation: Operations on the ArrayList will process as follows:add(10): Add 10 to the end of the list. ArrayList = [10].add(5): Add 5 to the end of the list. ArrayList = [10, 5].add(20): Add 20 to the end of the list. ArrayList = [10, 5, 20].remove(): Remove and return the last element, 20. ArrayList = [10, 5].get(1): Return the element at index 1, which is 5.reverse(): Reverse the list. ArrayList = [5, 10].size(): The list contains two elements, so return 2.Input: queries[][] = [[1, 4], [1, 2], [1, 9], [5], [3, 0], [2], [4], [6]]Output: [2, 9, 2]Explanation: Operations on the ArrayList will process as follows:add(4): Add 4 to the end of the list. ArrayList = [4].add(2): Add 2 to the end of the list. ArrayList = [4, 2].add(9): Add 9 to the end of the list. ArrayList = [4, 2, 9].sort(): Sort the list in ascending order. ArrayList = [2, 4, 9].get(0): Return the element at index 0, which is 2.remove(): Remove and return the last element, 9. ArrayList = [2, 4].reverse(): Reverse the list. ArrayList = [4, 2].size(): The list contains two elements, so return 2.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(q * n * log n)
- **Expected Auxiliary Space Complexity:** O(q + n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-06-24 16:58:56
- **Status:** Correct
- **Marks:** 2

```java
class Solution {

    public static void add_to_ArrayList(ArrayList<Integer> A, int x) {
        // Your code here
        A.add(x);

        // Just add, don't print anything
    }

    public static void sort_ArrayList_Asc(ArrayList<Integer> A) {

        Collections.sort(A);
        // Your code here
        // Just sort, don't print anything
    }

        
    public static void reverse_ArrayList(ArrayList<Integer> A) {
        // Your code here
      Collections.reverse(A);
        // Just reverse, don't print anything
    }
        

    public static int size_Of_ArrayList(ArrayList<Integer> A) {
        // Your code here
        return A.size();
        
        // Return the size of ArrayList
        
    }

    public static void sort_ArrayList_Desc(ArrayList<Integer> A) {
        // Your code here
        Collections.sort(A,Collections.reverseOrder());
        
        // Just sort in desc order, don't print anything
    }

    public static void print_ArrayList(ArrayList<Integer> A) {
        // Your code here
        for(int i=0; i<A.size();i++){
            System.out.print(A.get(i)+" ");
        }
        // Print the elements of A, don't add new line
    }
}
```

*Generated on: 24/11/2026, 23:46:14*