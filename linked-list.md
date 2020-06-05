 # Linked-list

+ [reverse-linked-list](#reverse-linked-list)

## reverse-linked-list

 https://leetcode.com/problems/reverse-linked-list/ 

 ```python
class Solution:
    def reverseList(self, head):
        prev = None
        cur_node = head
        while cur_node:
            cur_node.next, prev, cur_node = prev, cur_node, cur_node.next
        return prev

 ```