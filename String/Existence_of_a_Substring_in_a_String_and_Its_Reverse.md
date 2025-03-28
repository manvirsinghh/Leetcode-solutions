

# 📌 LeetCode Problem:[3083. Existence of a Substring in a String and Its Reverse
](https://leetcode.com/problems/add-strings/description/)

# **Problem statement:-Given a string s, find any substring of length 2 which is also present in the reverse of s.

**Return true if such a substring exists, and false otherwise.**


### Solution:-

``` java

class Solution {
    public boolean isSubstringPresent(String s) {
        String str=new StringBuilder(s).reverse().toString();
        List<String>list=new ArrayList<>();
        for(int i=0;i<s.length()-1;i++){
            list.add(s.substring(i,i+2));
        }

        for(int i=0;i<str.length()-1;i++){
            if(list.contains(str.substring(i,i+2))){
                return true;
            }
        }
    return false;
    }
}
