 # Tree

+ [kth-smallest-element-in-a-bst](#kth-smallest-element-in-a-bst)

## subtree-of-another-tree

 https://leetcode.com/problems/kth-smallest-element-in-a-bst/ 

 ```python
class Solution:
    def kthSmallest(self, root, k):
        was = set()
        stack = [root]
        while(stack):
            currNode = stack.pop()
            if((not currNode.left and not currNode.right) or currNode in was):
                k -= 1
                if(k == 0):
                    return currNode.val
            else:
                was.add(currNode)
                if(currNode.right):
                    stack.append(currNode.right)
                stack.append(currNode)
                if(currNode.left):
                    stack.append(currNode.left)

 ```