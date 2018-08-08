
# 组合求和问题

我们有一个 **组** 的候选数字 (`candidates`) **(没有重复)** 和 目标号码 (`target`) ,找到所有不相同的组合`candidates`候选数字它们的总和等于`target`. 

当然, 能允许 选择重复 **相同** 的数字`candidates`. 

**注意:**

-   所有数字 (包括`target`) 将是正整数. 
-   解决方案集 不得包含 重复的组合. 

## 例子

    Input: candidates = [2,3,6,7], target = 7,

    A solution set is:
    [
      [7],
      [2,2,3]
    ]

    Input: candidates = [2,3,5], target = 8,

    A solution set is:
    [
      [2,2,2,2],
      [2,3,3],
      [3,5]
    ]

## 说明

由于 问题是获得所有可能的结果,而不是 最佳结果或结果数,因此我们不需要考虑DP (动态规划) ,需要使用 递归的回溯方法 来处理它. 

以下是针对`candidates = [2, 3]`和`target = 6`情况的决策树示例: 

                    0
                  /   \
               +2      +3
              /   \      \
           +2       +3    +3
          /  \     /  \     \
        +2    ✘   ✘   ✘     ✓
       /  \
      ✓    ✘    

## 参考

-   [LeetCode](https://leetcode.com/problems/combination-sum/description/)
