
# 独特路径问题

机器人位于`m x n`网格左上角 (在下图中标记为"start") . 

机器人只能一时间 向下 或 向右 移动. 机器人正试图到达网格的右下角 (在下图中标记为"Finish") . 

有多少可能的独特路径?

![Unique Paths](https://leetcode.com/static/images/problemset/robot_maze.png)

## 例子

**示例#1**

> 注意: 不是小猪猪的大小哦

    Input: m = 3, n = 2
    Output: 3
    Explanation:
    从 左上角出发, 有三种路径到达右下角:
    1. Right -> Right -> Down
    2. Right -> Down -> Right
    3. Down -> Right -> Right

**例#2**

    Input: m = 7, n = 3
    Output: 28

## 算法

### 回溯

首先想到的可能是我们需要建立一个决策树

- `D`意味着向下移动 
- `R`意味着向右移动. 

例如,小猪猪在`width = 3`和`height = 2`出发的情况下我们将有以下决策树: 

                    START
                    /   \
                   D     R
                 /     /   \
               R      D      R
             /      /         \
            R      R            D

           END    END          END

我们可以在这里看到三个独特的分支,这是我们问题的答案. 

**时间复杂性**: `O(2 ^ n)`- 使用方形板`n`,最坏的情况下

**辅助空间复杂性**: `O(m + n)`- 因为我们需要存储具有位置的当前路径. 

### 动态规划

让我们来对待`BOARD[i][j]`

因为要走最短路径，每一步只能向右方或者下方走。所以经过每一个格子路径数只可能源自左方或上方，这就得到了动态规划的递推式，我们用一个二维数组储存每个格子的路径数

    BOARD[i][j] = BOARD[i - 1][j] + BOARD[i][j - 1]; // 只能向右方或者下方走

基本情况是: 

    BOARD[0][any] = 1; // only one way to reach any top slot.
    BOARD[any][0] = 1; // only one way to reach any slot in the leftmost column.

> 最左边和最上边的路径数都固定为1，代表一直沿着最边缘走的路径。

对于`3 x 2`实例我们的动态规划矩阵如下所示: 

|       |  0  |  1  |  1  |
| :---: | :-: | :-: | :-: |
| **0** |  0  |  1  |  1  |
| **1** |  1  |  2  |  3  |

每个单元格包含其唯一路径的数量. 我们需要右下角的数字`3`. 

> `DP` 二维数组

**时间复杂性**: `O(m * n)`- 因为我们正在浏览DP矩阵的每个单元格. 

**辅助空间复杂性**: `O(m * n)`- 因为我们需要有DP矩阵. 

### 杨辉三角形基础

这个问题实际上是杨辉三角形的另一种形式. 

这个矩形的角落是`m + n - 2`线,和`min(m, n) - 1`三角形的位置. 

## 参考

-   [LeetCode](https://leetcode.com/problems/unique-paths/description/)
- [[Leetcode] Unique Paths 唯一路径](https://segmentfault.com/a/1190000003502805)