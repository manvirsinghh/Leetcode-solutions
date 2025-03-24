# 📌 LeetCode Problem 1748. Sum of Unique Elements
](https://leetcode.com/problems/sum-of-unique-elements/description/)

# **Problem statement:-You are given an integer array nums. The unique elements of an array are the elements that appear exactly once in the array.

Return the sum of all the unique elements of nums..**



### Solution:-

``` java



import java.util.HashSet;

class Solution {
    public int sumOfUnique(int[] nums) {
        HashSet<Integer> uniqueSet = new HashSet<>();
        HashSet<Integer> duplicateSet = new HashSet<>();
        int sum = 0;

        for (int num : nums) {
            if (!uniqueSet.contains(num) && !duplicateSet.contains(num)) {
                // First occurrence: Add to uniqueSet and sum
                uniqueSet.add(num);
                sum += num;
            } else if (uniqueSet.contains(num)) {
                // Second occurrence: Remove from uniqueSet and sum, add to duplicateSet
                uniqueSet.remove(num);
                duplicateSet.add(num);
                sum -= num;
            }
        }
        
        return sum;
    }
}
