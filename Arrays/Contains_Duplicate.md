# 📌 LeetCode Problem:[217. Contains Duplicate
](https://leetcode.com/problems/contains-duplicate/description/)

# **Problem statement:-Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.

### Solution:-

``` java

 class Solution {
    public boolean containsDuplicate(int[] nums) {
        HashMap<Integer,Integer>map =new HashMap<>();
        for(int num:nums){
            if(map.containsKey(num)){
                map.put(num,map.get(num)+1);
            }
            else{
                map.put(num,1);
            }
        }
        int frequency=0;
        for(int key:map.keySet()){
            if(map.get(key)>=2){
                return true;
            }
        }
    return false;
    }
}
