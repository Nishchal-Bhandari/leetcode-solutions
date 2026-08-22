# 3918. Check Divisibility by Digit Sum and Product
  
<br>**Problem:** https://leetcode.com/problems/check-divisibility-by-digit-sum-and-product/<br>

**Difficulty:** Easy<br>
**Topics:** Math<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-22 22:07 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.2 MB (beats 58.35189999999999%)


<!-- leetgit:submissionId=2116374159 codeHash=0a7c7a274a06ff21ebfb8be5ae3eb0368fb695755cd19ace9052d4dd87f22600 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def checkDivisibility(self, n: int) -> bool:
        d_sum=sum(int(x) for x in str(n))
        d_prod=1
        for dig in str(n):
            d_prod*=int(dig)

        return n%(d_sum+d_prod)==0

```
