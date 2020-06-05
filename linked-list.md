 # Linked-list

+ [reorder-list](#reorder-list)

## reorder-list

 https://leetcode.com/problems/reorder-list/ 

 ```python
class Solution:
    def reorderList(self, head):
        if not head:
            return
        slow, fast = head, head
        while fast and fast.next:
            slow, fast = slow.next, fast.next.next
        pre, slow.next, slow = None, None, slow.next
        while slow:
            slow.next, pre, slow = pre, slow, slow.next
        while head and pre:
            head.next, head, pre.next, pre = pre, head.next, head.next, pre.next

 ```