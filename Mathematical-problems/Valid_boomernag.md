# 📌 LeetCode Problem:[1037. Valid Boomerang

](https://leetcode.com/problems/valid-boomerang/description/)

# **Problem statement:-Given an array points where points[i] = [xi, yi] represents a point on the X-Y plane, return true if these points are a boomerang.

**A boomerang is a set of three points that are all distinct and not in a straight line**


### Solution:-

``` java


class Solution {
    public boolean isBoomerang(int[][] points) {
        if(points.length<3){
            return false;
        }
      int x1=points[0][0];
      int x2=points[1][0];
      int x3=points[2][0];
      int y1=points[0][1];
      int y2=points[1][1];
      int y3=points[2][1];

        if ((x1 == x2 && y1 == y2) || (x1 == x3 && y1 == y3) || (x2 == x3 && y2 == y3)) {
            return false;
        }
if((y2-y1)*(x3-x1)==(y3-y1)*(x2-x1)){
return false;
}



 
return true;

    }
}
