 # Arrays

+ [two-sum](#two-sum)

## two-sum

 https://leetcode.com/problems/two-sum/ 

 ```python
class Solution:
    def TwoSum(self, nums, target):
        d = {}
        for i, num in enumerate(nums):
            if target - num in d:
                return [i, d[target-num]]
            else:
                d[num] = i
 ```