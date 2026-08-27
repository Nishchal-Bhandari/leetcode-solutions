# 4. Median of Two Sorted Arrays
  
<br>**Problem:** https://leetcode.com/problems/median-of-two-sorted-arrays/<br>

**Difficulty:** Hard<br>
**Topics:** Array, Binary Search, Divide and Conquer<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-08-27 23:59 local time

**Runtime:** 4 ms (beats 28.763%)
**Memory:** 19.4 MB (beats 77.97910000000003%)


<!-- leetgit:submissionId=2122261491 codeHash=013254e4e2e933c81d59bcb5c206eaa90cedaba7f6f86be459af02b116c873dc notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def findMedianSortedArrays(self, nums1: List[int], nums2: List[int]) -> float:
        nums=sorted(nums1+nums2)
        print(nums)
        if len(nums)==1:
                return nums[0]
        if nums:
                length=len(nums)
        else:
                return 0
        
        if length%2==1:
                return nums[length//2]
        else:
                return (nums[length//2-1]+nums[length//2])/2
             
             
                
                
               
```
