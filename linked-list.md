 # Linked-list

+ [linked-list-cycle-ii](#linked-list-cycle-ii)

## linked-list-cycle-ii

 https://leetcode.com/problems/linked-list-cycle-ii/

 ```python
class Solution:
    def detectCycle(self, head):
        if head is None or head.next is None:
            return None
        else:
            dic = {}
            current = head
            while current.next is not None:
                if current in dic:
                    return current
                else:
                    dic[current] = 1
                current = current.next
            return None

 ```