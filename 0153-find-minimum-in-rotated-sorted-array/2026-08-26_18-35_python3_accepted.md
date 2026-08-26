# 153. Find Minimum in Rotated Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-26 18:35 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.4 MB (beats 25.925499999999985%)


<!-- leetgit:submissionId=2120814229 codeHash=897aa8e2be9f980400c57278ae1de2e0a190cccd77e442163cbfc36f7c6ca9e5 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def findMin(self, nums: List[int]) -> int:
        l=0
        r=len(nums)-1
        while l<r:
            m=(l+r)//2

            if nums[m]<nums[r]:
                r=m
            else:
                l=m+1

        return nums[l]
        
```
