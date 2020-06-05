 # Linked-list

+ [middle-of-the-linked-list](#middle-of-the-linked-list)

## middle-of-the-linked-list

 https://leetcode.com/problems/middle-of-the-linked-list/ 

 ```python
class Solution:
    def middleNode(self, head):
        marker1 = head
        marker2 = head
        while marker2 and marker2.next is not None:
            marker1 = marker1.next
            marker2 = marker2.next.next
        return marker1

 ```