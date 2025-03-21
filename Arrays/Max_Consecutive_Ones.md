# 📌 LeetCode Problem:[485. Max Consecutive Ones
](https://leetcode.com/problems/max-consecutive-ones/description/)

# **Problem statement:-Given a binary array nums, return the maximum number of consecutive 1's in the array.

### Solution:-

``` java

 class Solution {
    public int findMaxConsecutiveOnes(int[] nums) {
        int consecutive_ones=0;
         int max_ones = 0;
        for(int i=0;i<nums.length;i++){
            if(nums[i]==1){
              consecutive_ones++;
              max_ones=Math.max(consecutive_ones,max_ones);
            }
            else{
              consecutive_ones=0;
            }
        }
   return max_ones;
    }
}
