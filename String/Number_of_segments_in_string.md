

# 📌 LeetCode Problem:[434. Number of Segments in a String
](https://leetcode.com/problems/number-of-segments-in-a-string/description/)

# **Problem statement:-Given a string s, return the number of segments in the string.

**A segment is defined to be a contiguous sequence of non-space characters.**


### Solution:-

``` java

class Solution {
    public int countSegments(String s) {
        // Check for null or empty string
        if (s == null || s.trim().isEmpty()) {
            return 0; // Return 0 for empty or whitespace-only strings
        }

        // Trim leading and trailing spaces
        s = s.trim();

        // Split the string into words based on whitespace
        String[] words = s.split("\\s+");

        // The number of segments is the length of the resulting array
        return words.length;
    }
}
