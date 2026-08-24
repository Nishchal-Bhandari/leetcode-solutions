# 33. Search in Rotated Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/search-in-rotated-sorted-array/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-25 00:01 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.5 MB (beats 38.875299999999996%)


<!-- leetgit:submissionId=2118852546 codeHash=67298e18d0922bddfa80839393fcf8659ace79a4e0e639ea04ae7be26b1057eb notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def search(self, a: List[int], target: int) -> int:

        l=0
        r=len(a)-1

        while l<=r:
            m=(l+r)//2
            if a[m]==target:
                return m
                break

            elif a[0]<=a[m]:
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
            return -1
        
```
