# 898. Transpose Matrix
  
<br>**Problem:** https://leetcode.com/problems/transpose-matrix/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Matrix, Simulation<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 14:24 local time

**Runtime:** 1 ms (beats 26.3759%)
**Memory:** 19.8 MB (beats 83.3061%)


<!-- leetgit:submissionId=2155772159 codeHash=d2ad3a19fd6f80b0a749534a975338d7ec3bc3830e852806b9fae9c01791a805 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def transpose(self, m: list[list[int]]) -> list[list[int]]:
        t=[[0]*len(m) for i in range(len(m[0]))]
        for i in range(len(m)):
            for j in range(len(m[0])):
                t[j][i]=m[i][j]

        return t
        
```
