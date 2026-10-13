# 80. Remove Duplicates from Sorted Array II
  
<br>**Problem:** https://leetcode.com/problems/remove-duplicates-from-sorted-array-ii/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-13 22:48 local time

**Runtime:** 19 ms (beats 61.93430000000001%)
**Memory:** 21.1 MB (beats 69.40639999999999%)


<!-- leetgit:submissionId=2171428283 codeHash=a60c13ad8bcdc2f76ec1ba3aedefe97de24b98c85571f53df4f7568aa155e831 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def removeDuplicates(self, nums: list[int]) -> int:
        def remove(arr):
            prev=arr[0]
            count=-1
            i=0

            while i<(len(arr)):
                
                
                if i==0 or arr[i]==prev:
                    count+=1
                    
                    if count>=2:
                        
                        arr.pop(i)
                    else:
                        i+=1
                else:
                    count=0
                    prev=arr[i]
                    i+=1


            return i-1

        remove(nums)




        
        
```
