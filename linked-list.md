 # Linked-list

+ [palindrome-linked-list](#palindrome-linked-list)

## palindrome-linked-list

 https://leetcode.com/problems/palindrome-linked-list/ 

 ```python
class Solution:
    def isPalindrome(self, head: ListNode) -> bool:
        if head is None or head.next is None:
            return True
        list = []
        while head is not None:
            list.append(head.val)
            head = head.next
        while len(list) > 1:
            if list[0] != list[-1]:
                return False
            else:
                list.pop()
                list.pop(0)
        return True

 ```