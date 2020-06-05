 # Linked-list

+ [linked-list-cycle](#linked-list-cycle)

## linked-list-cycle

 https://leetcode.com/problems/linked-list-cycle/

 ```python
class Solution:
    def hasCycle(self, head):
        s = head
        f = head
        while f and f.next:
            s = s.next
            f = f.next.next
            if s == f:
                return True
        return False

 ```