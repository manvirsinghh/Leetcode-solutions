
# 📌 LeetCode Problem:[860. Lemonade Change

](https://leetcode.com/problems/lemonade-change/description/)

# **Problem statement:-At a lemonade stand, each lemonade costs $5. Customers are standing in a queue to buy from you and order one at a time (in the order specified by bills). Each customer will only buy one lemonade and pay with either a $5, $10, or $20 bill. You must provide the correct change to each customer so that the net transaction is that the customer pays $5.

**Note that you do not have any change in hand at first.**

**Given an integer array bills where bills[i] is the bill the ith customer pays, return true if you can provide every customer with the correct change, or false otherwise.**

### Solution:-

``` java

 class Solution {
    public boolean lemonadeChange(int[] bills) {
        int fiveCount = 0, tenCount = 0;

        for (int bill : bills) {
            if (bill == 5) {
                fiveCount++; // Collect $5 bill
            } else if (bill == 10) {
                if (fiveCount == 0) return false; // No $5 bill for change
                fiveCount--; // Give one $5 bill as change
                tenCount++;  // Store $10 bill
            } else { // bill == 20
                if (tenCount > 0 && fiveCount > 0) { 
                    tenCount--; // Give one $10 bill
                    fiveCount--; // Give one $5 bill
                } else if (fiveCount >= 3) {
                    fiveCount -= 3; // Give three $5 bills
                } else {
                    return false; // Not enough change
                }
            }
        }
        return true; // Successfully gave change to all customers
    }
}
