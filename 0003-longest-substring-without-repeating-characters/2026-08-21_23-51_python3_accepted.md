# 3. Longest Substring Without Repeating Characters
  
<br>**Problem:** https://leetcode.com/problems/longest-substring-without-repeating-characters/<br>

**Difficulty:** Medium<br>
**Topics:** Hash Table, String, Sliding Window<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-21 23:51 local time

**Runtime:** 738 ms (beats 5.005599999999991%)
**Memory:** 20.4 MB (beats 5.073500000000001%)


<!-- leetgit:submissionId=2115405556 codeHash=afad2c9d5efd919ef085b9251473d6a05572253e46640ea47d1a3561fc4ad4ab notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

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
                print(s[i],h,left,right)
                h[s[i]]=i
                mv=(right-left)+1 if mv<(right-left)+1 else mv
                right+=1
                
            else:
                print("l",left)
                left=max(h[s[i]]+1,left)
                mv=(right-left)+1 if mv<(right-left)+1 else mv
                
                
                h[s[i]]=i
                right+=1
                
                

        return mv

            
```
