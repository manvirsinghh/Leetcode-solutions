

# 📌 LeetCode Problem:[1108. Defanging an IP Address
](https://leetcode.com/problems/defanging-an-ip-address/description/)

# **Problem statement:-Given a valid (IPv4) IP address, return a defanged version of that IP address.

**A defanged IP address replaces every period "." with "[.]".**


### Solution:-

``` java

class Solution {
    public String defangIPaddr(String address) {
        StringBuilder str=new StringBuilder();
         for(char ch:address.toCharArray()){
            if(Character.isDigit(ch)){
                str.append(ch);
            }
            if(ch == '.'){
                 str.append("[.]");
            }
         }
    return str.toString();
    }
}
