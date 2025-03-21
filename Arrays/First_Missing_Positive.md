# 📌 LeetCode Problem:[41. First Missing Positive](https://leetcode.com/problems/first-missing-positive/description/)

# **Problem statement:-Given an unsorted integer array nums. Return the smallest positive integer that is not present in nums.**

# **You must implement an algorithm that runs in O(n) time and uses O(1) auxiliary space.**

### Solution:-

``` java

class Solution {
    public int firstMissingPositive(int[] nums) {
        int i=0;
        while(i<nums.length){
            int correctindex=nums[i]-1;
            if(nums[i]>0 && nums[i]<nums.length && nums[i]!=nums[correctindex]){
                int temp=nums[i];
                nums[i]=nums[correctindex];
                nums[correctindex]=temp;
            }
            else{
                i++;
            }

        }
        for( i=0;i<nums.length;i++){
            if(nums[i]!=i+1){
                return i+1;
            }
        }
  return nums.length+1;
    }
}
