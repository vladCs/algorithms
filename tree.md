 # Tree

+ [same-tree](#same-tree)

## same-tree

 https://leetcode.com/problems/same-tree/ 

 ```python
class Solution:
    def isSameTree(self, p, q):
        return isSameNode(p, q)


def isSameNode(p, q):
    if not (p and q):
        return not (p or q)
    check = isSameNode(p.left, q.left) and isSameNode(p.right, q.right)
    if p.val == q.val and check:
        return True
    else:
        return False

 ```