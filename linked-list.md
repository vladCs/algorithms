 # Linked-list

+ [remove-nth-node-from-end-of-list](#remove-nth-node-from-end-of-list)

## two-sum

 https://leetcode.com/problems/remove-nth-node-from-end-of-list/

 ```python
class Solution:
    def removeNthFromEnd(self, head, n):
        a1 = head
        prev = current = nafter = a1
        if a1.next is None:
            return None
        for i in range(1, n):
            nafter = nafter.next
        # print(nafter.val)
        while(True):
            if nafter.next is None:
                if prev == current:
                    return current.next
                prev.next = current.next
                break
            prev = current
            current = current.next
            nafter = nafter.next
        return a1

 ```