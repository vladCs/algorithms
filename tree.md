 # Tree

+ [binary-tree-inorder-traversal](#binary-tree-inorder-traversal)

## binary-tree-inorder-traversal

 https://leetcode.com/problems/binary-tree-inorder-traversal/ 

 ```python
class Solution:
    def help(self, root, l):
        if root:
            self.help(root.left, l)
            l.append(root.val)
            self.help(root.right, l)
            return l

    def inorderTraversal(self, root):
        l = []
        return self.help(root, l)

 ```