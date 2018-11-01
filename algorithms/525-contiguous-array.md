## [Description](https://leetcode.com/problems/contiguous-array/description/)
## Topic: [HashTable](../topics/HashTable.md)
## Solution 
Python3
```python3
class Solution:
    def findMaxLength(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        # if nums == None: return 0
        
        acc = 0
        dict = {0:-1}
        # !! the 0:-1 is necessary
        max_len = 0
        
        for i in range(len(nums)):
        # !! "for i in range(len(nums)):" !!
        # !! easily written as: "for i in nums:"
            # print(i)
            temp = 1 if nums[i] == 1 else -1
            acc += temp
            if acc in dict:
                max_len = max(max_len, i - dict[acc])
                # !! dict[acc] not dict{acc} 
            else:
                dict[acc] = i
        return max_len

```
## Complexity: O(n)
## Points
* the 0:-1 is necessary
* ...
