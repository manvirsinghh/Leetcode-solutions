
# 📌 LeetCode Problem Running Sum of 1d Array
](https://leetcode.com/problems/running-sum-of-1d-array/description/)

# **Problem statement:-Given an array nums. We define a running sum of an array as runningSum[i] = sum(nums[0]…nums[i]).

**Return the running sum of nums.**

.

### Solution:-

``` java



class Solution {
    public int[] runningSum(int[] nums) {
         for (int i = 1; i < nums.length; i++) {
            nums[i] += nums[i - 1]; // Update nums[i] to be the sum of previous elements
        }
        return nums; // Return the modified nums array
    }
}
