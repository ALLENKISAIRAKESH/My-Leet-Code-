# Two Sum

| Field | Value |
|---|---|
| Platform | LeetCode |
| Difficulty | Easy |
| Language | python3 |
| URL | [https://leetcode.com/problems/two-sum/](https://leetcode.com/problems/two-sum/) |

## Problem Statement

Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`.

## Solution

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        seen = {}
        for i, num in enumerate(nums):
            diff = target - num
            if diff in seen:
                return [seen[diff], i]
            seen[num] = i
        return []
```
