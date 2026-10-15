# 122. Best Time to Buy and Sell Stock II
  
<br>**Problem:** https://leetcode.com/problems/best-time-to-buy-and-sell-stock-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Dynamic Programming, Greedy<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-15 19:29 local time

**Runtime:** 2 ms (beats 67.2122%)
**Memory:** 19.9 MB (beats 99.98060000000001%)


<!-- leetgit:submissionId=2173065405 codeHash=1c51f653a269802b52b17d1c992581f68e5f4c8c6dca5722876455f46b85c39d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
