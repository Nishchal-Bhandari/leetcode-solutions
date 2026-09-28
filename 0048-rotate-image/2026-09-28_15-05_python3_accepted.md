# 48. Rotate Image
  
<br>**Problem:** https://leetcode.com/problems/rotate-image/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Math, Matrix<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 15:05 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.3 MB (beats 30.151499999999984%)


<!-- leetgit:submissionId=2155810201 codeHash=e71b6dc4550add07670f2542bc180abc49b0efe01069e267e9faa98645ab1c25 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def rotate(self, matrix: list[list[int]]) -> None:
        """
        Do not return anything, modify matrix in-place instead.
        """

        for i in range(len(matrix)):
            for j in range(i,len(matrix)):
                matrix[i][j],matrix[j][i]=matrix[j][i],matrix[i][j]

        for i in range(len(matrix)):
            matrix[i]=matrix[i][::-1]

        return matrix

        
```
