# 121. Best Time to Buy and Sell Stock
  
<br>**Problem:** https://leetcode.com/problems/best-time-to-buy-and-sell-stock/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Dynamic Programming<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-14 18:09 local time

**Runtime:** 35 ms (beats 80.09830000000005%)
**Memory:** 28.7 MB (beats 43.374899999999954%)


<!-- leetgit:submissionId=2172119405 codeHash=5e9b3148c607efa98b7628da8f4a886b1e662b3e26beb5e104e04361be17177a notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def maxProfit(self, prices: list[int]) -> int:
        minp=float(inf)
        maxp=0
        for val in prices:
            if val<minp:
                minp=val
            else:
                maxp=max(maxp,val-minp)
        return maxp
        
        
```
