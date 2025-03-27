
# 📌 LeetCode Problem:[1189. Maximum Number of Balloons]
(https://leetcode.com/problems/maximum-number-of-balloons/description/)

# **Problem statement:-Given a string text, you want to use the characters of text to form as many instances of the word "balloon" as possible.

You can use each character in text at most once. Return the maximum number of instances that can be formed.**

### Solution:-

``` java




import java.util.*;

class Solution {
    public int maxNumberOfBalloons(String text) {
        // Step 1: Count frequency of each character in text
        Map<Character, Integer> freqMap = new HashMap<>();
        for (char c : text.toCharArray()) {
            freqMap.put(c, freqMap.getOrDefault(c, 0) + 1);
        }

        // Step 2: Initialize minCount with a large value
        int minCount = Integer.MAX_VALUE;

        // Step 3: Use containsKey() to check before accessing the map
        if (freqMap.containsKey('b')) {
            minCount = Math.min(minCount, freqMap.get('b') / 1);
        } else {
            return 0;
        }

        if (freqMap.containsKey('a')) {
            minCount = Math.min(minCount, freqMap.get('a') / 1);
        } else {
            return 0;
        }

        if (freqMap.containsKey('l')) {
            minCount = Math.min(minCount, freqMap.get('l') / 2); // 'l' appears twice
        } else {
            return 0;
        }

        if (freqMap.containsKey('o')) {
            minCount = Math.min(minCount, freqMap.get('o') / 2); // 'o' appears twice
        } else {
            return 0;
        }

        if (freqMap.containsKey('n')) {
            minCount = Math.min(minCount, freqMap.get('n') / 1);
        } else {
            return 0;
        }

        return minCount;
    }

  
}
