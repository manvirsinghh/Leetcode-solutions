

# 📌 LeetCode Problem:[242. Valid Anagram
](https://leetcode.com/problems/valid-anagram/description/)

# **Problem statement:-Given two strings s and t, return true if t is an anagram of s, and false otherwise.


### Solution:-

``` java

class Solution {
    public boolean isAnagram(String s, String t) {
        if(s.length()!=t.length()){
            return false;
        }
        char[] chararray=s.toCharArray();
        char [] chararray1=t.toCharArray();
        Arrays.sort(chararray);
        Arrays.sort(chararray1);

    for(int i=0;i<chararray.length;i++){
        if(chararray[i]!=chararray1[i]){
            return false;
        }
    }
    return true;
    }
}
