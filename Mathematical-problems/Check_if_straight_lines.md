# 📌 LeetCode Problem:[1232. Check If It Is a Straight Line

](https://leetcode.com/problems/check-if-it-is-a-straight-line/description/)

# **Problem statement:-You are given an array coordinates, coordinates[i] = [x, y], where [x, y] represents the coordinate of a point. Check if these points make a straight line in the XY plane.



### Solution:-

``` java


class Solution {
    public boolean checkStraightLine(int[][] coordinates) {
        if(coordinates.length<2){
            return false;
        }
        int x1=coordinates[0][0];
        int y1=coordinates[0][1];
        int x2=coordinates[1][0];
        int y2=coordinates[1][1];
       

        for(int i=2;i<coordinates.length;i++){
          int x3=coordinates[i][0];
          int y3=coordinates[i][1];
 if ((y2 - y1) * (x3 - x1) != (y3 - y1) * (x2 - x1)) {
                return false; // If slopes are not equal, points are not collinear
            }
        }
            
        return true;
    }
}
