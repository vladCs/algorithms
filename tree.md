 # Tree

+ [validate-binary-search-tree](#validate-binary-search-tree)

## subtree-of-another-tree

 https://leetcode.com/problems/validate-binary-search-tree/ 

 ```python
class Solution:
    def isValidBST(self, root):
        if(not root):
            return True
        arr = []
        arr = self.inOrder(root, arr)
        if(len(set(arr)) != len(arr)):
            return False
        copy_arr = arr[:]
        copy_arr.sort()
        return copy_arr == arr

    def inOrder(self, root, arr):
        if not root:
            return
        self.inOrder(root.left, arr)
        arr.append(root.val)
        self.inOrder(root.right, arr)
        return arr

 ```