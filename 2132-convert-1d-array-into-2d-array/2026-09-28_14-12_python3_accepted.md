# 2132. Convert 1D Array Into 2D Array
  
<br>**Problem:** https://leetcode.com/problems/convert-1d-array-into-2d-array/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Matrix, Simulation<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 14:12 local time

**Runtime:** 28 ms (beats 37.145399999999945%)
**Memory:** 25.4 MB (beats 38.18540000000001%)


<!-- leetgit:submissionId=2155760789 codeHash=a4ab36e01089aa9318674e44cdc524ab4ea4f6c8d83897feada818b56478a0ad notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def construct2DArray(self, o: list[int], m: int, n: int) -> list[list[int]]:
        if len(o)!=m*n:
            return []

        t=[[0]*n for i in range(m)]
        ind=0

        for i in range(len(t)):
            for j in range(len(t[0])):
                t[i][j]=o[ind]
                ind+=1

        return t
        
```
