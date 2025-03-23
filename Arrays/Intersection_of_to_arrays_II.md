# 📌 LeetCode Problem 350. Intersection of Two Arrays II
](https://leetcode.com/problems/intersection-of-two-arrays-ii/description/)

# **Problem statement:-Given two integer arrays nums1 and nums2, return an array of their intersection. Each element in the result must appear as many times as it shows in both arrays and you may return the result in any order..**

.

### Solution:-

``` java



class Solution {
    public int[] intersect(int[] nums1, int[] nums2) {
    // Step 1: Sort both arrays
        Arrays.sort(nums1);
        Arrays.sort(nums2);

        // Step 2: Use two pointers to find common elements
        List<Integer> result = new ArrayList<>();
        int i = 0, j = 0;

        while (i < nums1.length && j < nums2.length) {
            if (nums1[i] == nums2[j]) {
                // Common element found, add to result
                result.add(nums1[i]);
                i++;
                j++;
            } else if (nums1[i] < nums2[j]) {
                // Move pointer for nums1 forward
                i++;
            } else {
                // Move pointer for nums2 forward
                j++;
            }
        }

        // Step 3: Convert result list to array
        int[] intersection = new int[result.size()];
        for (int k = 0; k < result.size(); k++) {
            intersection[k] = result.get(k);
        }

        return intersection;
    }
}
