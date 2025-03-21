
# 📌 LeetCode Problem:[290. Word Pattern](https://leetcode.com/problems/word-pattern/description/)

# **Problem statement:-Given a pattern and a string s, find if s follows the same pattern.

**Here follow means a full match, such that there is a bijection between a letter in pattern and a non-empty word in s. Specifically:**

- **Each letter in pattern maps to exactly one unique word in s.**
- **Each unique word in s maps to exactly one letter in pattern.**
- **No two letters map to the same word, and no two words map to the same letter.**

### Solution:-

``` java



class Solution {
    public boolean wordPattern(String pattern, String s) {
        String[] words = s.split(" ");
        if (pattern.length() != words.length) return false;

        HashMap<Character, String> map = new HashMap<>();
        HashSet<String> usedWords = new HashSet<>();

        for (int i = 0; i < pattern.length(); i++) {
            char c = pattern.charAt(i);
            String word = words[i];

            if (map.containsKey(c)) {
                if (!map.get(c).equals(word)) return false; // Mismatch
            } else {
                if (usedWords.contains(word)) return false; // Word already mapped
                map.put(c, word);
                usedWords.add(word);
            }
        }
        return true;
    }
}
