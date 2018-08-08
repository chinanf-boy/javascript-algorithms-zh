
# 最长递增子序列

最长递增子序列问 题是 找到 给定序列的子序列,其中子序列的元素按排序顺序,从最低到最高,并且子序列尽可能长. 该子序列 不一定是连续的 或 唯一的. 

## 复杂性性

最长递增子序列问题 可以 及时解决`O(n log n)`,这里的`n`表示输入序列的长度. 

动态规划方法具有`O(n * n)`复杂性. 

## 例

在二进制 Van der Corput 序列的前16个值中

    0, 8, 4, 12, 2, 10, 6, 14, 1, 9, 5, 13, 3, 11, 7, 15

最长递增子序列是

    0, 2, 6, 9, 11, 15.

这个子序列长度为6; 输入序列没有 七个成员增加的子序列. 但此示例中 最长递增子序列不是唯一的: 例如,

    0, 4, 6, 9, 11, 15 or
    0, 2, 6, 9, 13, 15 or
    0, 4, 6, 9, 13, 15

是在相同输入序列中 等长的其他递增子序列. 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Longest_increasing_subsequence)
-   [Dynamic Programming Approach on YouTube](https://www.youtube.com/watch?v=CE2b_-XfVDk&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
