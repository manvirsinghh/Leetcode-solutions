# 📌 LeetCode Problem  3190. Find Minimum Operations to Make All Elements Divisible by Three
](https://leetcode.com/problems/find-minimum-operations-to-make-all-elements-divisible-by-three/description/)

# **Problem statement:-You are given an integer array nums. In one operation, you can add or subtract 1 from any element of nums.

Return the minimum number of operations to make all elements of nums divisible by 3..**

.

### Solution:-

``` java


class Solution {
    public int minimumOperations(int[] nums) {
        int operations=0;
        for(int num:nums){
            if(num%3==1) {
                num-=1;
                operations++;
            }
            else if(num%3==2){
                num+=1;
                operations++;
            }
            
        }
    return operations;
    }
}
