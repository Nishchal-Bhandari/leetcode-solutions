# 162. Find Peak Element
  
<br>**Problem:** https://leetcode.com/problems/find-peak-element/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-31 14:28 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.3 MB (beats 79.9704%)


<!-- leetgit:submissionId=2125898960 codeHash=748bc832a75c6d79dcf5dbf16d7fff1e4ba1f4e9e22b5d37a1f7853f03e2fee7 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def findPeakElement(self, nums: List[int]) -> int:
        l=0
        r=len(nums)-1

        while l<r:
            m=(l+r)//2

            if nums[m]<nums[m+1]:
                l=m+1

            else:
                r=m

        return l

            
        
```
