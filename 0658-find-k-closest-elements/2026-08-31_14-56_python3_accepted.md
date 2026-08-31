# 658. Find K Closest Elements
  
<br>**Problem:** https://leetcode.com/problems/find-k-closest-elements/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Binary Search, Sliding Window, Sorting, Heap (Priority Queue)<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-31 14:56 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 20.6 MB (beats 85.7431%)


<!-- leetgit:submissionId=2125925345 codeHash=8883d7b7b65a0671e674b43a98aaaf059462289586df0b360f3caf97c7e7f569 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def findClosestElements(self, arr: List[int], k: int, x: int) -> List[int]:
        l=0
        r=len(arr)-k

        while l<r:
            m=(l+r)//2

            if x-arr[m] >arr[m+k]-x:
                l=m+1
            else:
                r=m
                
        return arr[l:l+k]
        
```
