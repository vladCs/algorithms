 # Arrays

+ [subarray-sum-equals-k](#subarray-sum-equals-k)

## subarray-sum-equals-k

 https://leetcode.com/problems/subarray-sum-equals-k/ 

 ```python
class Solution:
    def SubarraySum(self, nums, k):
        d = defaultdict(int)
        d[0] += 1
        temp = 0
        res = 0
        for i, num in enumerate(nums):
            temp += num
            res += d[temp - k]
            d[temp] += 1
        return res

 ```