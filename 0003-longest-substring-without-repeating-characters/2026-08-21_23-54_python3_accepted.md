# 3. Longest Substring Without Repeating Characters
  
<br>**Problem:** https://leetcode.com/problems/longest-substring-without-repeating-characters/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Sliding Window<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-21 23:54 local time

**Runtime:** 217 ms (beats 20.589299999999998%)
**Memory:** 19.9 MB (beats 15.1935%)


<!-- leetgit:submissionId=2115409222 codeHash=6ec8a7387cef36c587ea025d1755fc2b3f44db10e6163c2f37a5aa34b7d8b578 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
                mv=max((right-left)+1,mv)
                right+=1
                
            else:
                
                left=max(h[s[i]]+1,left)
                mv=max((right-left)+1,mv)

                h[s[i]]=i
                right+=1
                
                

        return mv

            
```
