# 📌 LeetCode Problem:[453. Minimum Moves to Equal Array Elements II
](https://leetcode.com/problems/minimum-moves-to-equal-array-elements-ii/)

 **Problem statement:-Given an integer array nums of size n, return the minimum number of moves required to make all array elements equal.**

**In one move, you can increment or decrement an element of the array by 1.**
**Test cases are designed so that the answer will fit in a 32-bit integer. **

### Solution:-

``` java

 class Solution {
    public int minMoves2(int[] nums) {
            Arrays.sort(nums); // Sort the array
        int median = nums[nums.length / 2]; // Get the median
        int moves = 0;

        for (int num : nums) {
            moves += Math.abs(num - median); // Sum of absolute differences
        }

        return moves;
    }
}
