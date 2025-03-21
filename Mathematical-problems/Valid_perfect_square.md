
# 📌 LeetCode Problem:[367. Valid Perfect Square
](https://leetcode.com/problems/valid-perfect-square/description/)

### **Problem statement:-Given a positive integer num, return true if num is a perfect square or false otherwise.

**A perfect square is an integer that is the square of an integer. In other words, it is the product of some integer with itself.**

**You must not use any built-in library function, such as sqrt.**



### Solution:-

``` java
class Solution {
    public boolean isPerfectSquare(int num) {
    int odd = 1;
        while (num > 0) {
            num -= odd;
            odd += 2; // Next odd number
        }
        return num == 0;
    }
}
