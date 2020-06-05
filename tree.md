 # Tree

+ [symmetric-tree](#symmetric-tree)

## symmetric-tree

 https://leetcode.com/problems/symmetric-tree/ 

 ```python
class Solution:
    def isSymmetric(self, root):
        path = []

        def euler(node):
            if not node:
                path.append(None)
                return
            path.append(node.val)
            euler(node.left)
            path.append(node.val)
            euler(node.right)
            path.append(node.val)
        euler(root)
        return path == path[::-1]

 ```