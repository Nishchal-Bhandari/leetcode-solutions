# 122. Best Time to Buy and Sell Stock II
  
<br>**Problem:** https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-15 19:29 local time

**Runtime:** 1 ms (beats 72.219%)
**Memory:** 20.3 MB (beats 54.702500000000015%)


<!-- leetgit:submissionId=2173065852 codeHash=465001f560b36f42aadece68ead8c2f198c90374752786c1f0afc1c6d78fb34f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def maxProfit(self, prices: list[int]) -> int:
        profit=0
        for i in range(1,len(prices)):
            if prices[i]>prices[i-1]:
                profit+=prices[i]-prices[i-1]
                
        return profit
```
