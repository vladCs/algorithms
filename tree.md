 # Tree

+ [binary-search-tree-iterator](#binary-search-tree-iterator)

## binary-search-tree-iterator

 https://leetcode.com/problems/binary-search-tree-iterator/ 

 ```python
class BSTIterator:

    def __init__(self, root):
        self.traverse = []

        def inOrderTraversal(node):
            if node is not None:
                inOrderTraversal(node.left)
                self.traverse.append(node.val)
                inOrderTraversal(node.right)
        inOrderTraversal(root)

    def next(self):
        if self.hasNext():
            return self.traverse.pop(0)

    def hasNext(self):
        if len(self.traverse) != 0:
            return True
        return False

 ```