# 📌 LeetCode Problem:[693. Binary Number with Alternating Bits


](https://leetcode.com/problems/binary-number-with-alternating-bits/description/)

# **Problem statement:-Given a positive integer, check whether it has alternating bits: namely, if two adjacent bits will always have different values.





### Solution:-

``` java


class Solution {
    public boolean hasAlternatingBits(int n) {
        String Binarystr=Integer.toBinaryString(n);
        for(int i=0;i<Binarystr.length()-1;i++){
            if(Binarystr.charAt(i)==Binarystr.charAt(i+1)){
             return false;   
            }
        }
    return true;
    }
}
