

# 📌 LeetCode Problem:[415. Add Strings
](https://leetcode.com/problems/add-strings/description/)

# **Problem statement:-Given two non-negative integers, num1 and num2 represented as string, return the sum of num1 and num2 as a string.

**You must solve the problem without using any built-in library for handling large integers (such as BigInteger). You must also not convert the inputs to integers directly.**


### Solution:-

``` java

class Solution {
    public String addStrings(String num1, String num2) {
        while(num1.length()<num2.length()){
            num1="0"+num1;
        }
        while(num2.length()<num1.length()){
            num2="0"+num2;
        }
        StringBuilder result=new StringBuilder();
        int carry=0;

        for(int i=num1.length()-1;i>=0;i--){
            int digit1=num1.charAt(i)-'0';
            int digit2=num2.charAt(i)-'0';
            int sum=digit1+digit2+carry;
            if(sum>9){
                carry=sum/10;
                result.append(sum%10);
            }
            else{
                carry=0;
                result.append(sum);
            }
        }
        if(carry>0){
            result.append(carry);
        }
          return result.reverse().toString();
    }
}
