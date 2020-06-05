 # Tree

+ [subtree-of-another-tree](#subtree-of-another-tree)

## subtree-of-another-tree

 https://leetcode.com/problems/subtree-of-another-tree/ 

 ```python
class Solution:
    def isSubtree(self, s, t):
        if not s:
            return False
        if self.isSameTree(s, t):
            return True
        return self.isSubtree(s.left, t) or self.isSubtree(s.right, t)

    def isSameTree(self, p, q):
        if p and q:
            rez1 = self.isSameTree(p.left, q.left)
            rez2 = self.isSameTree(p.right, q.right)
            return p.val == q.val and rez1 and rez2
        return p is q

 ```