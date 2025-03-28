# 📌 LeetCode Problem   1207. Unique Number of Occurrences
](https://leetcode.com/problems/unique-number-of-occurrences/description/)

# **Problem statement:-Given an array of integers arr, return true if the number of occurrences of each value in the array is unique or false otherwise..**

.

### Solution:-

``` java



class Solution {
    public boolean uniqueOccurrences(int[] arr) {
        HashMap<Integer,Integer>occurences=new HashMap<>();
            Set<Integer> uniqueCounts = new HashSet<>();
        for(int num:arr){
            if(occurences.containsKey(num)){
                occurences.put(num,occurences.get(num)+1);
            }
            else{
                occurences.put(num,1);
            }
        }
        for(int count:occurences.values()){
            if(uniqueCounts.contains(count)){
                return false;
            }
            uniqueCounts.add(count);
        }
    return true;
    }
}
