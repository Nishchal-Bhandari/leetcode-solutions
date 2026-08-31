# 882. Peak Index in a Mountain Array
  
<br>**Problem:** https://leetcode.com/problems/peak-index-in-a-mountain-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search, Ternary Search<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-31 14:19 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 31.5 MB (beats 23.19549999999998%)


<!-- leetgit:submissionId=2125891165 codeHash=49d04bcb3dba0776a35324e44a5d4c53d602d13e6e159eea1e4c8b0962c8f2db notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def peakIndexInMountainArray(self, arr: List[int]) -> int:
        l=0
        r=len(arr)-1

        while l<r:
            m=(l+r)//2
            if arr[m]<arr[m+1]:
                l=m+1
            else:
                r=m

        return l
        
```
