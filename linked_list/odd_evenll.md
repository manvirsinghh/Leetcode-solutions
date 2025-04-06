# 📌 LeetCode Problem 328. Odd Even Linked List
](https://leetcode.com/problems/odd-even-linked-list/description/?envType=problem-list-v2&envId=linked-list)

# **Problem statement:-Given the head of a singly linked list, group all the nodes with odd indices together followed by the nodes with even indices, and return the reordered list.

The first node is considered odd, and the second node is even, and so on.

Note that the relative order inside both the even and odd groups should remain as it was in the input.

You must solve the problem in O(1) extra space complexity and O(n) time complexity.**

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
    public ListNode oddEvenList(ListNode head) {
          
    if (head == null || head.next == null) return head;

        ListNode odd = head;
        ListNode even = head.next;
        ListNode evenHead = even; // To connect at the end of odd list

        while (even != null && even.next != null) {
            odd.next = even.next;    // link odd to next odd
            odd = odd.next;          // move odd pointer
            even.next = odd.next;    // link even to next even
            even = even.next;        // move even pointer
        }

        odd.next = evenHead; // finally connect odd list to even list
        return head;
    }
}
