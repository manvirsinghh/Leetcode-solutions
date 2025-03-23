

# 📌 LeetCode Problem:[345. Reverse Vowels of a String
](https://leetcode.com/problems/add-strings/description/)

# **Problem statement:-Given a string s, reverse only all the vowels in the string and return it.

**The vowels are 'a', 'e', 'i', 'o', and 'u', and they can appear in both lower and upper cases, more than once.**


### Solution:-

``` java

class Solution {
    public String reverseVowels(String s) {
         StringBuilder sb = new StringBuilder(s);
        
        // Create a set to store the vowels (both lowercase and uppercase)
        Set<Character> set = new HashSet<>();
        set.add('a');
        set.add('e');
        set.add('i');
        set.add('o');
        set.add('u');
        set.add('A');
        set.add('E');
        set.add('I');
        set.add('O');
        set.add('U');
        
        // Two pointers approach
        int left = 0;
        int right = sb.length() - 1;
        
        while (left < right) {
            // If left character is not a vowel, move left pointer
            if (!set.contains(sb.charAt(left))) {
                left++;
            }
            // If right character is not a vowel, move right pointer
            else if (!set.contains(sb.charAt(right))) {
                right--;
            }
            // If both left and right characters are vowels, swap them
            else {
                char temp = sb.charAt(left);
                sb.setCharAt(left, sb.charAt(right));
                sb.setCharAt(right, temp);
                left++;
                right--;
            }
        }
        
        return sb.toString();
    }
}
