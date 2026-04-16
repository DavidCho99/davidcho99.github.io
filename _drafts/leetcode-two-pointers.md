---
layout: post
title: Two Pointer
category: Computer Science
---


```python
class Solution:
    def isPalindrome(self, s: str) -> bool:
        s = s.lower()
        isPal = ""
        for i in s:
            if (i.isalpha() or i.isdigit()):
                isPal = isPal + i

        for i in range(len(isPal)):
            if (i == len(isPal) - 1 - i):
                return True
            if isPal[i] == isPal[len(isPal) - 1 - i]:
                continue
            else:
                return False
        return True


s = "A man, a plan, a canal: Panama"


solution = Solution()
print(solution.isPalindrome(s))
```


```python
class Solution(object):
    def twoSum(self, numbers, target):
        """
        :type numbers: List[int]
        :type target: int
        :rtype: List[int]
        """
        i, j = 0, (len(numbers) - 1)

        while i < j:
            curSum = numbers[i] + numbers[j]

            if curSum < target:
                i += 1
            elif curSum > target:
                j -= 1
            else:
                return [i+1, j+1]


numbers = [2, 3, 4]
target = 7

solution = Solution()
print(solution.twoSum(numbers, target))
```


```python
class Solution(object):
    def threeSum(self, nums):
        """
        :type nums: List[int]
        :rtype: List[List[int]]
        """
        nums.sort()
        res = []

        for index, num in enumerate(nums):
            if num > 0:
                break
            if index > 0 and num == nums[index -1]:
                continue

            l ,r = index + 1, len(nums) - 1
            
            while l < r:
                threeSum = num + nums[l] + nums[r]

                if threeSum > 0:
                    r -= 1
                elif threeSum < 0:
                    l += 1
                else:
                    res.append([num,nums[l], nums[r]])
                    l += 1
                    r -= 1
                    while nums[l] == nums[l - 1] and l < r:
                        l += 1
        return res

nums = [-3,-1,0,2,4,5]

solution = Solution()
print(solution.threeSum(nums))      

```


```python
# Hint 1
# If you simulate the problem, it will be O(n^2) which is not efficient.
# Hint 2
# Try to use two-pointers. Set one pointer to the left and one to the right of the array. Always move the pointer that points to the lower line.
# Hint 3
# How can you calculate the amount of water at each step?


class Solution(object):
    def maxArea(self, height):
        """
        :type height: List[int]
        :rtype: int
        """
        
        res = 0
        last = len(height)-1

        h, l, r= 0, 0, last

        while l < r:
            
            if height[l] < height[r]:
                h = height[l]
                temp = (r-l)*h
                l += 1
            else:
                h = height[r]
                temp = (r-l)*h
                r -= 1
            if res < temp:
                res = temp
            else:
                continue
            
        
        return res
    
height = [1,8,6,2,5,4,8,3,7]

solution = Solution()
print(solution.maxArea(height))    
```
