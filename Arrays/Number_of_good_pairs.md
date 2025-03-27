# 📌 LeetCode Problem 1512. Number of Good Pairs

](https://leetcode.com/problems/number-of-good-pairs/description/)

# **Problem statement:Given an array of integers nums, return the number of good pairs.

**A pair (i, j) is called good if nums[i] == nums[j] and i < j..**

.

### Solution:-

``` java


class Solution {
    public int numIdenticalPairs(int[] nums) {
    int good_pairs=0;
    for(int i=0;i<nums.length;i++){
        for(int j=i+1;j<nums.length;j++){
            if(nums[i]==nums[j]){
                good_pairs++;
            }
        }
    }   
    return good_pairs;
    }
}
