

# 📌 LeetCode Problem:[2129. Capitalize the Title
](https://leetcode.com/problems/capitalize-the-title/description/)

# **Problem statement:-You are given a string title consisting of one or more words separated by a single space, where each word consists of English letters. Capitalize the string by changing the capitalization of each word such that:

If the length of the word is 1 or 2 letters, change all letters to lowercase.
Otherwise, change the first letter to uppercase and the remaining letters to lowercase.
Return the capitalized title..**


### Solution:-

``` java

class Solution {
    public String capitalizeTitle(String title) {
        StringBuilder str=new StringBuilder();
        String [] words=title.split(" ");
        for(int i=0;i<words.length;i++){
            if(words[i].length()==1 || words[i].length()==2){
                str.append(words[i].toLowerCase());
            }
            else{
                str.append(Character.toUpperCase(words[i].charAt(0))).append(words[i].substring(1).toLowerCase());
            }
            if (i < words.length - 1) { // Add space between words
                str.append(" ");
            }
            
        }
     return str.toString();
    }
}
