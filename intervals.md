 # Intervals

+ [merge-intervals](#merge-intervals)

## merge-intervals

 https://leetcode.com/problems/merge-intervals/ 

 ```python
class Solution:
    def merge(self, intervals: List[List[int]]) -> List[List[int]]:
        intervals.sort()
        i = 0
        n = len(intervals)
        results = []
        while(i < n):
            start = intervals[i][0]
            end = intervals[i][1]
            while(i < n-1 and intervals[i+1][0] <= end):
                end = max(end, intervals[i+1][1])
                i += 1
            results.append([start, end])
            i += 1

        return results
 ```