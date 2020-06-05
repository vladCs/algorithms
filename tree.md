 # Tree

+ [same-tree](#same-tree)

## same-tree

 https://leetcode.com/problems/same-tree/ 

 ```python
class Solution:
    def maxDepth(self, root):

        def helper(node, s):
            if not node:
                return 0
            if not node.right and not node.left:
                return s
            return max(helper(node.left, s + 1), helper(node.right, s + 1))
        return helper(root, 1)

 ```