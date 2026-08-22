# 3. Longest Substring Without Repeating Characters
  
<br>**Problem:** https://leetcode.com/problems/longest-substring-without-repeating-characters/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Sliding Window<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-21 23:54 local time

**Runtime:** 208 ms (beats 28.3615%)
**Memory:** 19.8 MB (beats 30.9009%)


<!-- leetgit:submissionId=2115409692 codeHash=a282e90ca46638c92c2633c6df9cebde43f9082dbd8c1fa5310b6a9447ca8eb9 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def lengthOfLongestSubstring(self, s: str) -> int:
        if not s:
            return 0
        mv=1
        h={s[0]:0}
        left=0
        right=1
        
        for i in range(1,len(s)):
            if s[i] not in h :
                h[s[i]]=i
                mv=(right-left)+1 if mv<(right-left)+1 else mv
                right+=1
                
            else:
                
                left=max(h[s[i]]+1,left)
                mv=(right-left)+1 if mv<(right-left)+1 else mv

                h[s[i]]=i
                right+=1
                
                

        return mv

            
```
