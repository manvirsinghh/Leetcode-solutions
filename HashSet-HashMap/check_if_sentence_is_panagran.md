
# 📌 LeetCode Problem:1832. [Check if the Sentence Is Pangram]
(https://leetcode.com/problems/check-if-the-sentence-is-pangram/description/)

# **Problem statement:-A pangram is a sentence where every letter of the English alphabet appears at least once.

Given a string sentence containing only lowercase English letters, return true if sentence is a pangram, or false otherwise.**

### Solution:-

``` java




class Solution {
    public boolean checkIfPangram(String sentence) {
    Set<Character> letters = new HashSet<>();

        // Iterate over the sentence and add characters to the set
        for (char c : sentence.toCharArray()) {
            letters.add(c);
            if (letters.size() == 26) { // If all 26 letters are found, return true early
                return true;
            }
        }

        return false; // Return false if not all letters were found
    }
}
