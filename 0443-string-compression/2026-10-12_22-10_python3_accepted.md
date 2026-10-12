# 443. String Compression
  
<br>**Problem:** https://leetcode.com/problems/string-compression/<br>

**Difficulty:** Medium<br>
**Topics:** Two Pointers, String<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-12 22:10 local time

**Runtime:** 3 ms (beats 44.5261%)
**Memory:** 19.5 MB (beats 20.06670000000001%)


<!-- leetgit:submissionId=2170390788 codeHash=928498668452fe2dc3c85ba3d70bf21a462850fbb39884f5efbde1dc0092c4e9 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def compress(self, chars: list[str]) -> int:
        h=[]
        prev=""
        c=0
        for i in chars:
            
            if not prev or i!=prev:
                if c!=0 and c!=1:
                    h.extend(str(j) for j in str(c))
                if c!=0:
                    c=0
                
                h.append(i)
                c+=1
                prev=i
            else:
                c+=1   
                prev=i
        if c!=1 and c!=0:
            h.extend(str(j) for j in str(c))          
                       
        chars.clear()
        chars.extend(h)
        return len(h)

        
```
