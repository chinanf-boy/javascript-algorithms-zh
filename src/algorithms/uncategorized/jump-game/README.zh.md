# 跳跃游戏

## 问题

给出一个非负整数数组，你最初定位在数组的第一个位置。　　　

数组中的每个元素代表你在那个位置可以跳跃的最大长度。　　　　

判断你是否能到达数组的最后一个位置。

**示例#1**

    Input: [2,3,1,1,4]
    Output: true
    Explanation: 从索引0 跳转1步 到索引1，然后跳3步到最后一个索引.

**例#2**

    Input: [3,2,1,0,4]
    Output: false
    Explanation: 无论如何，你总是会到达索引3。 它的最大值
                  跳转长度为0，这使得无法到达最后一个索引.

## 命名

我们在数组中一个**"好的索引"是可以**从该位置开始,到达最后一个索引. 否则,该索引称为 **"坏索引"**. 这样问题就减少到 索引0 是否是"好的索引".

## 解决方案

### 方法 1: 回溯

这是一个低效的解决方案，我们尝试每一个跳跃模式
把我们从第一个位置带到最后一个位置。 我们从第一个位置开始
并跳转到可到达的每个索引。 我们重复这个过程直到最后
达到指数。 卡住时，回溯。

> 看到[backtrackingJumpGame.js](backtrackingJumpGame.js)文件

**时间复杂度:**: `O(2^n)`. 有 2<sup>n</sup> (上限) 从第一个位置跳到最后一个位置的方式,其中`n`是数组的长度`nums`.

**辅助空间复杂性**: `O(n)`. 递归需要额外的内存用于堆栈帧.

### 方法 2: 动态规划自上而下

自上而下的动态规划可以被认为是优化的回溯. 它依赖于观察,一旦我们确定某个指标是好/坏,这个结果永远不会改变. 这意味着我们可以存储结果,而不是每次都需要重新计算.

因此,对于数组中的每个位置,我们都记住索引是好还是坏. 让我们调用这个数组备忘录,让它的值为以下之一: GOOD,BAD,UNKNOWN. 这种技术称为 memoization.

> 看到[dpTopDownJumpGame.js](dpTopDownJumpGame.js)文件

**时间复杂度:**: `O(n^2)`. 对于数组中的每个元素,比如说`i`,我们正在关注下一个`nums[i]`旨在找到 GOOD 索引的元素. `nums[i]`最多可以`n`,这里`n`是数组的长度`nums`.

**辅助空间复杂性**: `O(2 * n) = O(n)`. 第一`n`起源于递归. 第二`n`来自`备忘录表-memo table`的使用.

### 方法 3: 动态规划自下而上

自上而下 到 自下而上的转换是通过 消除递归 来完成的. 实际上,这可以实现更好的性能,因为我们不再有堆栈开销的方法,甚至可能从一些缓存中受益. 更重要的是,这一步为未来的优化开辟了可能性. 通常通过尝试 从自上而下的方法 逆转步骤的顺序来消除递归.

这里的观察是我们只跳到右边. 这意味着如果我们从数组的右侧开始,每次我们将向右侧查询位置时,该位置已被确定为 GOOD 或 BAD. 这意味着我们不再需要递归,因为我们备忘录表中已有了结果.

> 看到[dpBottomUpJumpGame.js](dpBottomUpJumpGame.js)文件

**时间复杂度:**: `O(n^2)`. 对于数组中的每个元素,比如说`i`,我们正在关注下一个`nums[i]`旨在找到 GOOD 索引的元素. `nums[i]`最多可以`n`,这里`n`是数组的长度`nums`.

**辅助空间复杂性**: `O(n)`. 这来自备忘录表的使用.

### 方法 4: 贪心

一旦我们将代码置于 自下而上 状态,我们就可以做出最后一个重要的观察. 从给定的位置,当我们试图看看我们是否可以跳到一个好位置时,我们只使用第一个. 换句话说,最左边的一个. 如果我们将这个最左边的 GOOD 位置跟踪为一个单独的变量,我们可以避免在数组中搜索它. 不仅如此,我们可以完全停止使用数组.

> 从 结尾 开始 遍历数组, 比较 每个索引 的 `值 +索引` 能否到 结尾, 能-> 保存好索引值成为新的`结尾`,一直到遍历结束, 保存下来的索引值如果为`0`?**能跳:不能**

> 看到[greedyJumpGame.js](greedyJumpGame.js)文件

**时间复杂度:**: `O(n)`. 我们正在做一次通过`nums`数组,因此`n`步骤,这`n`是数组的长度`nums`.

**辅助空间复杂性**: `O(1)`. 我们没有使用任何额外的内存.

## 参考

- [Jump Game Fully Explained on LeetCode](https://leetcode.com/articles/jump-game/)
- [Dynamic Programming vs Divide and Conquer](https://itnext.io/dynamic-programming-vs-divide-and-conquer-2fea680becbe)
- [Dynamic Programming](https://en.wikipedia.org/wiki/Dynamic_programming)
- [Memoization on Wikipedia](https://en.wikipedia.org/wiki/Memoization)
- [Top-Down and Bottom-Up Design on Wikipedia](https://en.wikipedia.org/wiki/Top-down_and_bottom-up_design)
