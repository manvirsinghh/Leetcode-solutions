# Leetcode:-Power of Two
# [231. Power of Two](https://leetcode.com/problems/power-of-two/description/)

## Solution



'''java

class Solution {
    public boolean isPowerOfTwo(int n) {
        if(n<=0){
            return false;
        }
        return (n&(n-1))==0;
    }
}
