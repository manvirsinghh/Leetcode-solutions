# 📌 LeetCode Problem 1822. Sign of the Product of an Array
](https://leetcode.com/problems/sign-of-the-product-of-an-array/description/)

# **Problem statement:-Implement a function signFunc(x) that returns:

**1 if x is positive.  
-1 if x is negative.  
0 if x is equal to 0.  
You are given an integer array nums. Let product be the product of all values in the array nums.**

**Return signFunc(product).**

.

### Solution:-

``` java



class Solution {
    public int arraySign(int[] nums) {
        long product = 1;  // Use long to avoid some overflow cases
        
        for (int num : nums) {
            if (num == 0) return 0;  // If any number is 0, return 0 immediately
            product *= (num > 0) ? 1 : -1;  // Track the sign only
        }
        
        return (product > 0) ? 1 : -1;  // If product remains positive, return 1, else -1
    }
}
