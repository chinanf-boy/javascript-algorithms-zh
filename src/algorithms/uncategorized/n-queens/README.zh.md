
# N-Queens问题

**八皇后问题**是：设法在国际象棋的棋盘上放置八个皇后，使得其中任何一个皇后所处的“行”、“列”以及“对角线”上都不能有其它的皇后。 八个女王之谜是一个更普遍的例子*n皇后问题*将n个非攻击女王放置在`n×n`棋盘,对于所有自然数都存在解决方案`n`除了`n=2`和`n=3`. 

例如,以下是4皇后问题的解决方案. 

![N Queens](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/N_Queen_Problem.jpg)

预期输出是二进制矩阵,对于放置皇后的块,其具有1. 例如,以下是4皇后解决方案的输出矩阵. 

    { 0,  1,  0,  0}
    { 0,  0,  0,  1}
    { 1,  0,  0,  0}
    { 0,  0,  1,  0}

## 简单算法

生成船上所有可能的皇后集合配置,并打印满足给定约束的集合配置. 

    当 还具有 配置们
    {
       生成 下一个 配置
       if 皇后们不在 配置 
       then
       {
          print 配置;
       }
    }

## 回溯算法

我们的想法是从最左边的列开始,将皇后 一​​个接一个地放在不同的列中. 当我们在一个列中放置一个女王时,我们检查已经放置的女王的冲突. 在当前列中,如果我们找到没有冲突的行,我们将 此行和列 标记为解决方案的一部分. 如果由于冲突我们没有找到这样的行,那么我们回溯并返回false. 

    1) 开始最左边的列
    2) 如果所有皇后都安置好了
        `return true`
    3) 在当前列中尝试所有行. 每个行都运行下面字母顺序操作.
        a) 如果该皇后能安全放下当前行 `then` 记下 `[row, 
            column]` 作为答案的一部分 `and` 递归检查是否在这里放置女王导致解决方案.
        b) 如果皇后放在 `[row, column]` 解决了问题 `then return 
            true`.
        c) 如果放置的皇后不能解决问题 `then` 扔掉 `[row, 
            column]` (Backtrack) `and` 去回 (a) 继续尝试其他行.
    3) 如果所有行都尝试完了,来到了这一步, `return false` 结束.

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Eight_queens_puzzle)
-   [GeeksForGeeks](https://www.geeksforgeeks.org/backtracking-set-3-n-queen-problem/)
-   [On YouTube by Abdul Bari](https://www.youtube.com/watch?v=xFv_Hl4B83A&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
-   [On YouTube by Tushar Roy](https://www.youtube.com/watch?v=xouin83ebxE&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
