# 📌 LeetCode Problem:[1281. Subtract the Product and Sum of Digits of an Integer
](https://leetcode.com/problems/subtract-the-product-and-sum-of-digits-of-an-integer/description/)

# **Problem statement:-Given an integer number n, return the difference between the product of its digits and the sum of its digits.
.**



### Solution:-

``` java

class Solution {
    public int subtractProductAndSum(int n) {
        int sum=0;
        int product=1;
        while(n>0){
            product*=n%10;
            sum+=n%10;
            n/=10;
        }
      return product-sum;
    }
}
