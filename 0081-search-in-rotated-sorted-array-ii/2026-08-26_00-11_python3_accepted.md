# 81. Search in Rotated Sorted Array II
  
<br>**Problem:** https://leetcode.com/problems/search-in-rotated-sorted-array-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-26 00:11 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.5 MB (beats 68.83070000000001%)


<!-- leetgit:submissionId=2120067142 codeHash=08b85218d9c965018e0db5372505352fd51d3f7664141f731fb54e7fc72682a8 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def search(self, a: List[int], target: int) -> int:

        l=0
        r=len(a)-1

        while l<=r:
            m=(l+r)//2
            if a[m]==target:
                return True
                break
            if a[l]==a[m]==a[r]:
                l+=1
                r-=1
                continue

            if a[l]<=a[m]:
                if a[l]<=target<a[m]:
                    r=m-1
                else:
                    l=m+1

            else:
                if a[m]<target<=a[r]:
                    l=m+1
                else:
                    r=m-1


        else:
            return False
        
```
