 # Tree

+ [path-sum](#path-sum)

## path-sum

 https://leetcode.com/problems/path-sum/ 

 ```python
class Solution:
    def hasPathSum(self, root, sum):
        if not root:
            return False
        if not (root.left or root.right) and root.val == sum:
            return True
        sum -= root.val
        r = self.hasPathSum(root.left, sum) or self.hasPathSum(root.right, sum)
        return r

 ```