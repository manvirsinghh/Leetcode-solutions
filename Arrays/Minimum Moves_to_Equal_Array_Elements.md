# 📌 LeetCode Problem:[453. Minimum Moves to Equal Array Elements
](https://leetcode.com/problems/minimum-moves-to-equal-array-elements/description/)

 **Problem statement:-Given an integer array nums of size n, return the minimum number of moves required to make all array elements equal.**

**In one move, you can increment n - 1 elements of the array by 1.**

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
