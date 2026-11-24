## 01. Parenthesis Checker

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/parenthesis-checker2744/1)

### Problem Description

**Task:** Given a string s, composed of different combinations of '(' , ')', '{', '}', '[', ']'. Determine whether the Expression is balanced or not.An expression is balanced if:Each opening bracket has a corresponding closing bracket of the same type.Opening brackets must be closed in the correct order.Examples :Input: s = "[{()}]"

#### Examples

##### Example 1

- **Output:**
```text
true
```
- **Explanation:** All the brackets are well-formed.Input: s = "([]"Output: falseExplanation: The expression is not balanced as there is a missing ')' at the end.Input: s = "([{]})"Output: falseExplanation: The expression is not balanced as there is a closing ']' before the closing '}'.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(n)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-06-23 11:56:17
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public boolean isBalanced(String s) {
        // code here
        String temp="";
        for(int i=0;i<s.length();i++){
            char ch=s.charAt(i);
            if(ch=='('|| ch=='{'||ch=='['){
                temp+=ch;
            }else{
                if(temp.length()==0){
                    return false;
                }
                char last = temp.charAt(temp.length()-1);
                if((ch==')'&& last=='(')||
                (ch=='}' && last=='{')||
                (ch==']'&& last=='[')){
                    temp = temp.substring(0,temp.length()-1);
                }else{
                    return false;
                }
            }
        }
        return temp.length()==0;
    }
}
```

*Generated on: 24/11/2026, 23:50:56*