

# 📌 LeetCode Problem:[1078. Occurrences After Bigram
](https://leetcode.com/problems/occurrences-after-bigram/description/)

# **Problem statement:-Given two strings first and second, consider occurrences in some text of the form "first second third", where second comes immediately after first, and third comes immediately after second.

Return an array of all the words third for each occurrence of "first second third".**


### Solution:-

``` java

class Solution {
    public String[] findOcurrences(String text, String first, String second) {
        String [] words=text.split(" ");
          List<String> result = new ArrayList<>();
        for(int i=0;i<words.length-2;i++){
            if(words[i].equals(first) && words[i+1].equals(second)){
              result.add(words[i+2]);
            }
        }
  return result.toArray(new String[0]);
    }
}
