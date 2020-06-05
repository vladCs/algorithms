 # Intervals

+ [insert-interval](#insert-interval)

## insert-interval

 https://leetcode.com/problems/insert-interval/ 

 ```python
class Solution:
    def insert(self, intervals):
        intervals.append(newInterval)
        intervals.sort(key=lambda x: x[0])
        result = []
        for interval in intervals:
            if not result or result[-1][1] < interval[0]:
                result.append(interval)
            else:
                result[-1][1] = max(result[-1][1], interval[1])
        return result
 ```