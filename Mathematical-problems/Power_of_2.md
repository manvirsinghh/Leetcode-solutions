# 📌 LeetCode Problem:[231. Power of Two
](https://leetcode.com/problems/power-of-two/description/)

### **Problem statement:-Given an integer n, return true if it is a power of two. Otherwise, return false.

**An integer n is a power of two, if there exists an integer x such that n == 2x**



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
