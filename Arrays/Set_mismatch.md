# 📌 LeetCode Problem:[645. Set Mismatch
](https://leetcode.com/problems/set-mismatch/description/)

# **Problem statement:-You have a set of integers s, which originally contains all the numbers from 1 to n. Unfortunately, due to some error, one of the numbers in s got duplicated to another number in the set, which results in repetition of one number and loss of another number.

**You are given an integer array nums representing the data status of this set after the error.**

**Find the number that occurs twice and the number that is missing and return them in the form of an array.**

### Solution:-

``` java


  class Solution {
    public int[] findErrorNums(int[] nums) {
       int[]arr=new int[2];
       HashSet<Integer>seen=new HashSet<>();
       for(int i=0;i<nums.length;i++){
        if(seen.contains(nums[i])){
            arr[0]=nums[i];
            
        }
        seen.add(nums[i]);
       }
       int n=nums.length;
       for(int i=1;i<=n;i++){
        if(!seen.contains(i)){
            arr[1]=i;
        }
       }
    return arr;
    }
}
