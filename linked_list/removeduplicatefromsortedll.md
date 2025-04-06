# 📌 LeetCode Problem 83. Remove Duplicates from Sorted List
](https://leetcode.com/problems/remove-duplicates-from-sorted-list/description/?envType=problem-list-v2&envId=linked-list)

# **Problem statement:-Given the head of a sorted linked list, delete all duplicates such that each element appears only once. Return the linked list sorted as well...**

.

### Solution:-

``` java

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
        ListNode temp=head;
        if(temp==null){
            return temp;
        }
        while(temp!=null && temp.next!=null){
            if(temp.val==temp.next.val){
                temp.next=temp.next.next;
            }
            else{
                temp=temp.next;
            }

        }
     return head;
    }
}
