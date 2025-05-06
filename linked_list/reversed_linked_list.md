# 📌 LeetCode Problem 206. Reverse Linked List
[LeetCode Problem 206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/description/?envType=problem-list-v2&envId=linked-list)

# **Problem statement:-Given the head of a singly linked list, reverse the list, and return the reversed list**

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
    public ListNode reverseList(ListNode head) {
        if(head==null) return null;
        if(head.next==null) return head;
        ListNode curr=head;
        ListNode prev=null;
        ListNode next=null;

        while(curr!=null){
            next=curr.next;
            curr.next=prev;
            prev=curr;
            curr=next;
        } 
        return prev;
    }
}
---

//2nd approach is to use stack for reversing the linked list
//  if(head==null) return null;
//         if(head.next==null) return head;
// Stack<Integer>st=new Stack<>();
// ListNode temp=head;
// while(temp!=null){
//     st.push(temp.val);
//     temp=temp.next;
// }
// ListNode dummy=new ListNode(0);
// ListNode curr=dummy;


//  while(!st.isEmpty()){
//    curr.next=new ListNode (st.pop());
//    curr=curr.next;
//  }

// return dummy.next;
//     }
// }



```
