 # Linked-list

+ [intersection-of-two-linked-lists](#intersection-of-two-linked-lists)

## intersection-of-two-linked-lists

 https://leetcode.com/problems/intersection-of-two-linked-lists/ 

 ```python
class Solution:
    def getIntersectionNode(self, headA, headB):
        if not headA or not headB:
            return None
        key = headA
        while headA:
            headA.val = -1 * headA.val
            headA = headA.next
        while headB and headB.val >= 0:
            headB = headB.next
        while key:
            key.val = -1 * key.val
            key = key.next
        return headB

 ```