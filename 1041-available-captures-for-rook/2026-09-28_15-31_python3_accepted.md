# 1041. Available Captures for Rook
  
<br>**Problem:** https://leetcode.com/problems/available-captures-for-rook/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Matrix, Simulation<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-28 15:31 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.3 MB (beats 73.72399999999999%)


<!-- leetgit:submissionId=2155834856 codeHash=ea5ed0ffecd661da7ddc0f12c24c33a53b0ebfa65e9628c5ce75d70e5af3103d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def numRookCaptures(self, board: list[list[str]]) -> int:
        for i in range(len(board)):
            for j in range(len(board[0])):
                if board[i][j]=="R":
                    row=i
                    col=j
                    break
        r1=row-1
        c=0
        while r1>-1 and board[r1][col]!="B":
            if board[r1][col]=="p":
                c+=1
                break
            r1-=1
        r2=row+1
        while r2<len(board) and board[r2][col]!="B":
            if board[r2][col]=="p":
                c+=1
                break
            r2+=1
        c1=col-1
        while c1>-1 and board[row][c1]!="B":
            if board[row][c1]=="p":
                c+=1
                break
            c1-=1
        c2=col+1
        while c2<len(board) and board[row][c2]!="B":
            if board[row][c2]=="p":
                c+=1
                break
            c2+=1
        return c
        

```
