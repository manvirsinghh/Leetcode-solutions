

# 📌 LeetCode Problem:[3210. Find the Encrypted String
](https://leetcode.com/problems/find-the-encrypted-string/description/)

# **Problem statement:-You are given a string s and an integer k. Encrypt the string using the following algorithm:

For each character c in s, replace c with the kth character after c in the string (in a cyclic manner).
Return the encrypted string.**

**


### Solution:-

``` java
class Solution {
    public String getEncryptedString(String s, int k) {
          StringBuilder encrypted = new StringBuilder();
        int n = s.length();

        for (int i = 0; i < n; i++) {
            // Find the index of the k-th character after i (wrap around using modulo)
            int newIndex = (i + k) % n;
            encrypted.append(s.charAt(newIndex));
        }

        return encrypted.toString();
    }
}
