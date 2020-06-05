 # Arrays

+ [3sum](#3sum)

## 3sum

 https://leetcode.com/problems/3sum/ 

 ```python
class Solution:
    def threeSum(self, nums):
        nums.sort()
        ans = set()
        for i, v in enumerate(nums):
            self.twoSum(nums[i+1:], -v, ans)
        return ans

    def twoSum(self, nums, target, ans):
        d = {}
        for i, v in enumerate(nums):
            if target - v in d:
                ans.add((v, target - v, -target))
            d[v] = i

 ```