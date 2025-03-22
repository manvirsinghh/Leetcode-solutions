# 📌 LeetCode Problem1023. Camelcase Matching
](https://leetcode.com/problems/camelcase-matching/description/)

# **Problem statement:-Given an array of strings queries and a string pattern, return a boolean array answer where answer[i] is true if queries[i] matches pattern, and false otherwise.

**A query word queries[i] matches pattern if you can insert lowercase English letters into the pattern so that it equals the query. You may insert a character at any position in pattern 
or you may choose not to insert any characters at all.**

.

### Solution:-

``` java



class Solution {
    public List<Boolean> camelMatch(String[] queries, String pattern) {
        List<Boolean> result = new ArrayList<>();
        
        for (String query : queries) {
            result.add(matches(query, pattern));
        }
        
        return result;
    }
    
    private boolean matches(String query, String pattern) {
        int i = 0; // Pointer for pattern
        
        for (char ch : query.toCharArray()) {
            if (i < pattern.length() && ch == pattern.charAt(i)) {
                i++; // Move pattern pointer if character matches
            } else if (Character.isUpperCase(ch)) {
                return false; // Extra uppercase letter that doesn’t match pattern
            }
        }
        
        return i == pattern.length(); // Pattern should be fully matched
    }
}
