## leetcode-probelm:[704. Binary Search](https://leetcode.com/problems/binary-search/description/)

## Problem-statement:-Given an array of integers nums which is sorted in ascending order, and an integer target, write a function to search target in nums. If target exists, then return its index. Otherwise, return -1.

**You must write an algorithm with O(log n) runtime complexity.**

```java 
class Solution {
    public int search(int[] nums, int target) {
        int low=0;
        int high=nums.length-1;
      

        while(low<=high){
              int mid=(low+high)/2;
            if(nums[mid]==target){

                return mid;
            }
            else if(nums[mid]<target){
                low=mid+1;
            }
            else{
                high=mid-1;
            }
        }
 return -1;
    }
}
