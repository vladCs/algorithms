 # Linked-list

+ [sort-list](#sort-list)

## sort-list

 https://leetcode.com/problems/sort-list/ 

 ```python
class Solution:
    def sortList(self, head):
        def helper(head, dummy):
            if head.next is None:
                return head
            fast = head
            slow = head
            while fast and fast.next:
                prev = slow
                slow = slow.next
                fast = fast.next.next
            prev.next = None
            list0 = helper(head, dummy)
            list1 = helper(slow, dummy)
            node = dummy
            while list0 is not None or list1 is not None:
                if list0 is not None and list1 is not None:
                    if list0.val < list1.val:
                        node.next = list0
                        list0 = list0.next
                    else:
                        node.next = list1
                        list1 = list1.next
                    node = node.next
                elif list0 is None:
                    node.next = list1
                    break
                elif list1 is None:
                    node.next = list0
                    break
            return dummy.next
        if head is None:
            return head
        return helper(head, ListNode(-1))

 ```