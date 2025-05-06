# 📌 LeetCode Problem 2 Add Two Numbers
[LeetCode Problem 2. Add Two Numbers](https://leetcode.com/problems/add-two-numbers/description/?envType=problem-list-v2&envId=linked-list)

# **Problem statement:-You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order, and each of their nodes contains a single digit. Add the two numbers and return the sum as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.**

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
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
       ListNode dummy=new ListNode(0);
       ListNode curr=dummy;
       int carry=0; //variable for storing carry
//store the corresponding values of nodes of oth linked list
while(l1!=null || l2!=null){
int p1=(l1!=null)?l1.val :0;
int p2=(l2!=null)?l2.val :0;

int sum=p1+p2+carry;
carry=sum/10;

curr.next=new ListNode(sum%10);
curr=curr.next;
// Move to next nodes in the lists if they exist
            if (l1 != null) l1 = l1.next;
            if (l2 != null) l2 = l2.next;


}

//check if there is carry left
if(carry>0){
    curr.next=new ListNode(carry);
}
return dummy.next;

 
    }
}



```
