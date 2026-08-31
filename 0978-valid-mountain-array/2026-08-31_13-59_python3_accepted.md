# 978. Valid Mountain Array
  
<br>**Problem:** https://leetcode.com/problems/valid-mountain-array/<br>

**Difficulty:** Easy<br>
**Topics:** Array<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-31 13:59 local time

**Runtime:** 174 ms (beats 5.020100000000003%)
**Memory:** 20.3 MB (beats 96.96350000000001%)


<!-- leetgit:submissionId=2125874591 codeHash=445442c5f572cec3185e60961f1814ff467dc88110272cd1d5504b4f324fb78d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def validMountainArray(self, arr: List[int]) -> bool:
        i=0

        while i<len(arr)-1 and arr[i]<arr[i+1]:
            i+=1

        if i==0 or i==len(arr)-1:
            return False
        
        while i<len(arr)-1 and arr[i]>arr[i+1]:
            i+=1

        if i==len(arr)-1:
            return True 
        else:
            return False

        
        
```
