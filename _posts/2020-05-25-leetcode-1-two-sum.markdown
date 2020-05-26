---
layout: post
title:  "[LeetCode] 1. Two Sum"
date:   2020-05-26 15:52:35 -0400
categories: Algorithm Leetcode Easy
excerpt: This is the first problem on Leetcode. Given an array and a target, find two numbers in the array so that their sum is equal to the target, and return the subscript of the two numbers ...... 
---

## Description

Given an array of integers, return **indices** of the two numbers such that they add up to a specific target.

You may assume that each input would have **exactly** one solution, and you may not use the same element twice.

Example:

```
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```

## Solution

### Approach 1: Brute Force

The easiest way is to use brute force to traverse all the elements in the array to get the solution.

```Java
public int[] twoSum(int[] nums, int target) {
    for (int i = 0; i < nums.length; i++) {
        for (int j = i + 1; j < nums.length; j++) {
            if (nums[j] + nums[i] == target) {
                return new int[] { i, j };
            }
        }
    }
}
```

The brute force method can solve this problem, but its time complexity is O(n<sup>2</sup>).

### Approach 2: Hash Table

A better solution is to use Hash Table to solve this problem, only need to traverse the array once, so its complexity is O (n).

```Java
public int[] twoSum(int[] nums, int target) {
    int[] ret = new int[2];
    var map = new HashMap<Integer, Integer>();
    int remainder;
    for (int i = 0; i < nums.length; i++) {
        remainder = target - nums[i];
        if (map.containsKey(remainder)) {
            ret[0] = map.get(remainder);
            ret[1] = i;
            break;
        }
        map.put(nums[i], i);
    }
    return ret;
}
```

## Reference

[Two Sum](https://leetcode.com/problems/two-sum/)