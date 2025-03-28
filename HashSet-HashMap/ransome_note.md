
# 📌 LeetCode Problem:[383. Ransom Note](https://leetcode.com/problems/ransom-note/description/)

# **Problem statement:-Given two strings ransomNote and magazine, return true if ransomNote can be constructed by using the letters from magazine and false otherwise.

Each letter in magazine can only be used once in ransomNote..**

### Solution:-

``` java



class Solution {
    public boolean canConstruct(String ransomNote, String magazine) {
        HashMap<Character,Integer>ransomfreq=new HashMap<>();
        for(char c:ransomNote.toCharArray()){
            if(ransomfreq.containsKey(c)){
                ransomfreq.put(c,ransomfreq.get(c)+1);
            }
            else{
                ransomfreq.put(c,1);
            }
        }

        for(char c:magazine.toCharArray()){
            if(ransomfreq.containsKey(c)){
                ransomfreq.put(c,ransomfreq.get(c)-1);
                if(ransomfreq.get(c)==0){
                    return true;
                }
            }
        }
    return false;
    }
}
