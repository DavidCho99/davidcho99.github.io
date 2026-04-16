---
layout: post
title: Array and Hashing
category: Computer Science
selected_page: true
---


```python
class Solution(object):
    def groupAnagrams(self, strs):
        """
        :type strs: List[str]
        :rtype: List[List[str]]
        """
        mySet = set()
        grouplist = []
        print(mySet)

        for _str in strs:
            res = ''.join(sorted(_str))
            if res in mySet:
                mySet.add([res])
            else:
                continue

        print(mySet)



strs = ["eat","tea","tan","ate","nat","bat"]

solution = Solution()
print(solution.groupAnagrams(strs))      
        
```


```python
#https://leetcode.com/problems/top-k-frequent-elements/description/
# 347. Top K Frequent Elements

class Solution(object):
    def topKFrequent(self, nums, k):
        """
        :type nums: List[int]
        :type k: int
        :rtype: List[int]
        """
        count = {}
        freq = [[] for i in range(len(nums) + 1)]

        for n in nums:
            count[n] = 1 + count.get(n,0)
        for n,c in count.items():
            freq[c].append(n)

        res = []

        for i in reversed(range(len(freq))):
            for n in freq[i]:
                res.append(n)
            if k == len(res):
                return res 
```


```python
#https://leetcode.com/problems/product-of-array-except-self/
#238. Product of Array Except Self
class Solution(object):
    def productExceptSelf(self, nums):
        """
        :type nums: List[int]
        :rtype: List[int]
        """
        
        res = [1] * len(nums)

        prefix = 1
    
        for i in range(len(nums)):
            res[i] *= prefix 
            prefix *= res[i]

        postfix = 1
        for i in reversed(range(len(nums))):
            res[i] *= postfix
            postfix *= res[i]

        return res
```


```python
from collections import defaultdict

class Solution(object):
    def isValidSudoku(self, board):
        """
        :type board: List[List[str]]
        :rtype: bool
        """

        cols = defaultdict(set)
        rows = defaultdict(set)
        squares = defaultdict(set)

        for r in range(9):
            for c in range(9):
                if board[r][c] == '.':
                    continue
                if (board[r][c] in rows[r] or 
                    board[r][c] in cols[c] or
                    board[r][c] in squares[(r//3, c//3)]):
                    return False
                rows[r].add(board[r][c])
                cols[r].add(board[r][c])
                squares[r].add(board[r][c])
        return True
          


# Example usage:
sudoku_board = [["5","3",".",".","7",".",".",".","."],
                ["6",".",".","1","9","5",".",".","."],
                [".","9","8",".",".",".",".","6","."],
                ["8",".",".",".","6",".",".",".","3"],
                ["4",".",".","8",".","3",".",".","1"],
                ["7",".",".",".","2",".",".",".","6"],
                [".","6",".",".",".",".","2","8","."],
                [".",".",".","4","1","9",".",".","5"],
                [".",".",".",".","8",".",".","7","9"]]


solution = Solution()
print(solution.isValidSudoku(sudoku_board))  # Should return True for a valid Sudoku board.

```

    False



```python
from collections import defaultdict

# Create a defaultdict of sets
rows = defaultdict(set)

# Example 1: Using rows[r].add(board[r][c])

# Adding elements to sets associated with keys
rows[0].add(1)
rows[1].add(2)
rows[0].add(3)

print(rows)
# Output:
# defaultdict(<class 'set'>, {0: {1, 3}, 1: {2}})

# Example 2: Using rows[r] = board[r][c]

# Assigning values directly to keys
rows[0] = 4
rows[1] = 5

print(rows)
# Output:
# defaultdict(<class 'set'>, {0: 4, 1: 5})

# Example 3: Combining both methods

# Adding elements to sets and assigning values
rows[1] = 7

print(rows)
# Output:
# defaultdict(<class 'set'>, {0: {4, 6}, 1: 7})

```

    defaultdict(<class 'set'>, {0: {1, 3}, 1: {2}})
    defaultdict(<class 'set'>, {0: 4, 1: 5})
    defaultdict(<class 'set'>, {0: 4, 1: 7})



```python
class Solution:
    def maxProfit(self, prices) -> int:
        min_price = prices[0]
        max_profit = 0
        
        for price in prices[1:]:
            max_profit = max(max_profit, price - min_price)
            min_price = min(min_price, price)
        return max_profit

      



prices = [7,1,5,3,6,4]

solution = Solution()
print(solution.maxProfit(prices))
            
```

    5



```python
class Solution(object):
    def numIdenticalPairs(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        #how to make the pairs?
        #how to store the pairs?
        #how to find the pairs?
        #iterate the number and compare the elements of list if they are same then increase the value of identical_pairs 
        gp = 0
        # for loop in [0,len(nums))
        for i in range(len(nums)):
            # for loop in [i+1,len(nums))
            for j in range(i+1,len(nums)):
                # if condition fines the same number then update a good pair by increasing one.
                if nums[i] == nums[j]:
                    gp += 1
        # return gp
        return gp

                    


nums = [1,2,3,1,1,3]

solution = Solution()
print(solution.numIdenticalPairs(nums))
```

    4



```python
class Solution(object):
    def longestConsecutive(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        numSet = set(nums)
        longest = 0

        for num in nums:
            #check whether num is the first of a sequence.
            if num - 1 not in numSet:
                # if num is the first of a sequence set the length = 1
                length = 1
                # loop while num + length is not in numSet
                while (num + length) in numSet:
                    # increment the length until find the end of a sequence.
                    length += 1
                # 1. set the longestConsecutive using max function. 
                # 2. if a length of other sequence is bigger than current, then change the longest
                longest = max(longest, length)
        # return longest
        return longest




nums = [100,4,200,1,3,2]

solution = Solution()
print(solution.longestConsecutive(nums))
```


```python
#2023 Oct 10
class Solution(object):
    def merge(self, nums1, m, nums2, n):
        """
        :type nums1: List[int]
        :type m: int
        :type nums2: List[int]
        :type n: int
        :rtype: None Do not return anything, modify nums1 in-place instead.
        """
        nums = []
        # for loop while the nums1 
        for i in range(len(nums2)):
            nums1[m+i] = nums2[i]

        return nums1.sort() 
    
nums1 = [1,2,3,0,0,0]
m = 3
nums2 = [2,5,6]
n = 3

solution = Solution()
print(solution.merge(nums1, m, nums2, n))
```

    [1, 2, 2, 3, 5, 6]


#### 27. Remove Element
level: Easy

Given an integer array nums and an integer val, remove all occurrences of val in nums in-place. The order of the elements may be changed. Then return the number of elements in nums which are not equal to val.

Consider the number of elements in nums which are not equal to val be k, to get accepted, you need to do the following things:

* Change the array nums such that the first k elements of nums contain the elements which are not equal to val. The remaining elements of nums are not important as well as the size of nums.
* Return k.


```python
#2023 Oct 10

class Solution(object):
    def removeElement(self, nums, val):
        """
        :type nums: List[int]
        :type val: int
        :rtype: int
        """
        # set a index val to 0
        i = 0
        # for loop for len(nums)
        for j in range(len(nums)):
            # if nums[j] != val
            if nums[j] != val:
                # store the value in nums list to first element and increasing the value
                nums[i] = nums[j]
                i += 1
        return i


nums = [3,3,2,3,2]
val = 2  

solution = Solution()
print(solution.removeElement(nums, val))
```

    3

