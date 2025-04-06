# 📌 LeetCode Problem 876. Middle of the Linked List
](https://leetcode.com/problems/middle-of-the-linked-list/description/?envType=problem-list-v2&envId=linked-list)

# **Problem statement:-Given the head of a singly linked list, return the middle node of the linked list.

If there are two middle nodes, return the second middle node..**

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
    public ListNode middleNode(ListNode head) {
        ListNode temp=head;
     int length=0;
     while(temp!=null){
        length++;
        temp=temp.next;
     }
   
       temp=head;
       int mid=length/2;
       for(int i=0;i<mid;i++){
        temp=temp.next;
       }
   return temp;
     }
}

//2nd way:
// ListNode slow=head;
// ListNode fast=head;

//   while (fast != null && fast.next != null) {
//             slow = slow.next;
//             fast = fast.next.next;
//         }
//  return slow;
//     }
// }
