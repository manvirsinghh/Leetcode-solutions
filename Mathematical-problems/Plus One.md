# 📌 LeetCode Problem:[66. Plus One
](https://leetcode.com/problems/plus-one/description/)

# **Problem statement:-You are given a large integer represented as an integer array digits, where each digits[i] is the ith digit of the integer. The digits are ordered from most significant to least significant in left-to-right order. The large integer does not contain any leading 0's.

**Increment the large integer by one and return the resulting array of digits..**



### Solution:-

``` java
import java.math.BigInteger;
class Solution {
    public int[] plusOne(int[] digits) {
        
       // Convert array to a string
        StringBuilder numStr = new StringBuilder();
        for (int digit : digits) {
            numStr.append(digit);
        }

        // Convert string to BigInteger and add 1
        BigInteger num = new BigInteger(numStr.toString()).add(BigInteger.ONE);

       //convert number back to array
       String resultstr=String.valueOf(num);
       int[] arr=new int[resultstr.length()];
       for(int i=0;i<resultstr.length();i++){
        arr[i]=resultstr.charAt(i)-'0'; // Convert char to int
       }
 
  return arr;
    }
}
