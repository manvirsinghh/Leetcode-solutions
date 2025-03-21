
# 📌 LeetCode Problem:[125. Valid Palindrome
](https://leetcode.com/problems/valid-palindrome/description/)

# **Problem statement:-A phrase is a palindrome if, after converting all uppercase letters into lowercase letters and removing all non-alphanumeric characters, it reads the same forward and backward. Alphanumeric characters include letters and numbers.

**Given a string s, return true if it is a palindrome, or false otherwise.**

### Solution:-

``` java

class Solution {
    public boolean isPalindrome(String s) {
       s=s.toLowerCase();  
    StringBuilder str=new StringBuilder();
    for(char c:s.toCharArray()){
        if(Character.isLetterOrDigit(c)){
            str.append(c);
            
        }
    }
     StringBuilder str1=new StringBuilder();
    for(int i=s.length()-1;i>=0;i--){
        if(Character.isLetterOrDigit(s.charAt(i))){
            str1.append(s.charAt(i));
            
        }
    }
  if(str.toString().equals(str1.toString())){
    return true;
  }
   return false;
    }
}
