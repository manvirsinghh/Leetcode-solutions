# 📌 LeetCode Problem:[476. Number Complement

](https://leetcode.com/problems/number-complement/description/)

# **Problem statement:-The complement of an integer is the integer you get when you flip all the 0's to 1's and all the 1's to 0's in its binary representation.

For example, The integer 5 is "101" in binary and its complement is "010" which is the integer 2.
**Given an integer num, return its complement**



### Solution:-

``` java


class Solution {
    public int findComplement(int num) {
       String Binarystr=Integer.toBinaryString(num);
       StringBuilder str=new StringBuilder();
        for(int i=0;i<Binarystr.length();i++){
            char ch=Binarystr.charAt(i);
            if(ch=='0'){
                str.append('1');
            }
            else{
                str.append('0');
            }
        }
    return Integer.parseInt(str.toString(),2);
    }
}
