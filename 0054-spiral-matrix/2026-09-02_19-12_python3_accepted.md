# 54. Spiral Matrix
  
<br>**Problem:** https://leetcode.com/problems/spiral-matrix/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Matrix, Simulation<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-09-02 19:12 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.3 MB (beats 34.415300000000016%)


<!-- leetgit:submissionId=2128487229 codeHash=2fbf45aeeced35b09e8da76f53103356236ac617ebcf2f742a3718205c95fdae notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def spiralOrder(self, mat: List[List[int]]) -> List[int]:
        t=0
        e=len(mat)-1
       
        l=0
        r=len(mat[0])-1
        ans=[]
        while t<=e and l<=r:
            lt=l
            while t<=e and lt<=r:
                ans.append(mat[t][lt])
                
                lt+=1
            t+=1
            tt=t
            while tt<=e and l<=r:
                ans.append(mat[tt][r])
                
                tt+=1
            r-=1 
            rt=r
            while t<=e and l<=rt:
                ans.append(mat[e][rt])
                print(mat[e][rt])
                rt-=1
            e-=1
            et=e
            while t<=et and l<=r:
                
                ans.append(mat[et][l])
                et-=1

            l+=1

        return ans
            
        
```
