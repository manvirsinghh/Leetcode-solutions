

# 📌 LeetCode Problem:387. First Unique Character in a String

](https://leetcode.com/problems/first-unique-character-in-a-string/)

# **Problem statement:-Given a string s, find the first non-repeating character in it and return its index. If it does not exist, return -1.

### Solution:-

``` java

class Solution {
    public int firstUniqChar(String s) {
     HashMap<Character,Integer>freqmap=new HashMap<>();
     for(char c:s.toCharArray()){
        if(freqmap.containsKey(c)){
            freqmap.put(c,freqmap.get(c)+1);
        }
        else{
            freqmap.put(c,1);
        }
     }
     //find the character with freq 1 i.e non repeating character

     for(int i=0;i<s.length();i++){
        if(freqmap.get(s.charAt(i))==1){
            return i;
        }
     }
    return -1;
    }
}
