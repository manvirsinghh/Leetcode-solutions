# 📌 LeetCode Problem:[1051. Height Checker
](https://leetcode.com/problems/height-checker/description/)

## **Problem statement:-A school is trying to take an annual photo of all the students. The students are asked to stand in a single file line in non-decreasing order by height. Let this ordering be represented by the integer array expected where expected[i] is the expected height of the ith student in line.

**You are given an integer array heights representing the current order that the students are standing in. Each heights[i] is the height of the ith student in line (0-indexed).**

**Return the number of indices where heights[i] != expected[i].**

### Solution:-

``` java

 class Solution {
    public int heightChecker(int[] heights) {
   
        int indices=0;
        int[]expected=heights.clone();
         Arrays.sort(expected);
        
        for(int i=0;i<heights.length;i++){
            if(heights[i]!=expected[i]){
                indices++;
            }
        }
    return indices;
    }
}
