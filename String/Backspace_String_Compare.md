

# 📌 LeetCode Problem:[844. Backspace String Compare

](https://leetcode.com/problems/backspace-string-compare/description/)

# **Problem statement:-Given two strings s and t, return true if they are equal when both are typed into empty text editors. '#' means a backspace character.

**Note that after backspacing an empty text, the text will continue empty..**


### Solution:-

``` java

class Solution {
    public boolean backspaceCompare(String s, String t) {
        Stack<Character>first_string=new Stack<>();
        Stack<Character>second_string=new Stack<>();
         for(int i=0;i<s.length();i++){
            if(s.charAt(i)!='#'){
                first_string.push(s.charAt(i));
            }
            else{
                if(!first_string.isEmpty() && s.charAt(i)=='#'){
                    first_string.pop();
                }
            }

         }
   for(int i=0;i<t.length();i++){
            if(t.charAt(i)!='#'){
                second_string.push(t.charAt(i));
            }
            else{
                if(!second_string.isEmpty() && t.charAt(i)=='#'){
                    second_string.pop();
                }
            }

         }

  if(first_string.equals(second_string)) return true;
 return false;
    }
}
