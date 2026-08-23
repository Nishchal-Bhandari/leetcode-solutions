# 322. Coin Change
  
<br>**Problem:** https://leetcode.com/problems/coin-change/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Breadth-First Search, Knapsack Problem, Complete Knapsack<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-24 00:18 local time

**Runtime:** 455 ms (beats 79.48959999999974%)
**Memory:** 19.4 MB (beats 98.84429999999999%)


<!-- leetgit:submissionId=2117734474 codeHash=babd24f014c54f349dc38f6294c55b0e5da0b879b0dfbe900fa31bb452f6be75 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def coinChange(self, c: List[int], amount: int) -> int:
        
        c.sort()
        d=[amount+1 for i in range(amount+1)] 
        d[0]=0
        for i in c:
            for j in range(i,len(d)):
                rem=j-i
                d[j]=min(d[rem]+1,d[j])
        print(d[-1])
        return -1 if d[-1]>amount else d[-1]
        





        
```
