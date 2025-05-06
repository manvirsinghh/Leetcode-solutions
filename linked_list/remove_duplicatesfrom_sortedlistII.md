# 📌 LeetCode Problem 82. Remove Duplicates from Sorted List II
[LeetCode Problem 82 ,Remove duplicates from sorted list II](https://leetcode.com/problems/remove-duplicates-from-sorted-list-ii/description/?envType=problem-list-v2&envId=linked-list)

# **Problem statement:-Given the head of a sorted linked list, delete all nodes that have duplicate numbers, leaving only distinct numbers from the original list. Return the linked list sorted as well.**

.
---
### Solution:-

```java

/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode deleteDuplicates(ListNode head) {
        if (head == null) return null;
        if (head.next == null) return head;

        // Step 1: Count frequency using a HashMap
        HashMap<Integer, Integer> map = new HashMap<>();
        ListNode temp = head;

        while (temp != null) {
            if (map.containsKey(temp.val)) {
                map.put(temp.val, map.get(temp.val) + 1);
            } else {
                map.put(temp.val, 1);
            }
            temp = temp.next;
        }

        // Step 2: Rebuild list with only unique values
        ListNode dummy = new ListNode(0);
        ListNode curr = dummy;
        temp = head;

        while (temp != null) {
            if (map.get(temp.val) == 1) {
                curr.next = new ListNode(temp.val);
                curr = curr.next;
            }
            temp = temp.next;
        }

        return dummy.next;
    }
}







```
