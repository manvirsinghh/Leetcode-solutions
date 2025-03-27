# 📌 LeetCode Problem:[1295. Find Numbers with Even Number of Digits
](https://leetcode.com/problems/find-numbers-with-even-number-of-digits/description/)

# **Problem statement:-Given an array nums of integers, return how many of them contain an even number of digits..**



### Solution:-

``` bash

class Solution {
    public int findNumbers(int[] nums) {
        int count=0;
        for(int num:nums){
int digitcount=0;
int temp=num;
        
        while(temp>0){
            temp/=10;
            digitcount++;
        }
        if(digitcount%2==0){
            count++;
        }
    }
    return count;

}
}
