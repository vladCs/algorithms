 # Tree

+ [invert-binary-tree](#invert-binary-tree)

## invert-binary-tree

 https://leetcode.com/problems/invert-binary-tree/ 

 ```python
class Solution(object):
    def invertTree(self, root):
        if root is None:
            return None
        left = self.invertTree(root.left)
        right = self.invertTree(root.right)
        root.right = left
        root.left = right
        return root

 ```