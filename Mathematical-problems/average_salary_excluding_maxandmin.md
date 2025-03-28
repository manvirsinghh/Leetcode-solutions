# 📌 LeetCode Problem:[1491. Average Salary Excluding the Minimum and Maximum Salary


](https://leetcode.com/problems/average-salary-excluding-the-minimum-and-maximum-salary/description/)

# **Problem statement:-You are given an array of unique integers salary where salary[i] is the salary of the ith employee.**

**Return the average salary of employees excluding the minimum and maximum salary. Answers within 10-5 of the actual answer will be accepted.**





### Solution:-

``` java


class Solution {
    public double average(int[] salary) {
        Arrays.sort(salary);
        double sal=0;
        int count=0;
         for(int i=1;i<salary.length-1;i++){
            sal+=salary[i];
            count++;
         }
   return sal/count;
    }
}
