# 📌 LeetCode Problem 61. Rotate List
[LeetCode 61. Rotate List](https://leetcode.com/problems/rotate-list/description/?envType=problem-list-v2&envId=linked-list)

# **Problem statement:-Given the head of a linked list, rotate the list to the right by k places.**

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
    public ListNode rotateRight(ListNode head, int k) {
        if(head==null) return null;
        if(head.next==null) return head;
         // Step 1: Find the length of the linked list and the last node
        int length=1;
       ListNode temp=head;
        while(temp.next!=null){
            length++;
 temp=temp.next;
        }
        //special case if k>n
        k%=length;
        if(k==0) return head;  // If k is a multiple of length, no rotation needed
//   Make the list circular by connecting the last node to the head
        temp.next=head;
        //  Find the new tail and the new head after rotation
      
        int newtailpos=length-k; 
        ListNode newtail=head;
        for(int i=1;i<newtailpos;i++){
               newtail=newtail.next;
                 
        }
        // Break the circle to get the rotated list
        ListNode newhead = newtail.next;
        newtail.next = null; // Break the circular link
        return newhead;

    }
}
