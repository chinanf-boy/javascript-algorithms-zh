# JavaScript 算法与数据结构 [![translate-svg]][translate-list]

[![build status](https://travis-ci.org/trekhleb/javascript-algorithms.svg?branch=master)](https://travis-ci.org/trekhleb/javascript-algorithms)
[![codecov](https://codecov.io/gh/trekhleb/javascript-algorithms/branch/master/graph/badge.svg)](https://codecov.io/gh/trekhleb/javascript-algorithms)

[translate-svg]: http://llever.com/translate.svg
[translate-list]: https://github.com/chinanf-boy/chinese-translate-list


---

## 校对✔

> 进入到 每个算法中 还是 英文, 搞搞

<!-- doc-templite START generated -->
<!-- time = '2018 7.27' -->
<!-- repo = 'trekhleb/javascript-algorithms' -->
<!-- commit = 'f32172e3db50a73b2c4b09c4363d1fdc40ce2ef6' -->
翻译的原文 | 与日期 | 最新更新 | 更多
---|---|---|---
[commit] | ⏰ 2018 7.27 | ![last] | [中文翻译][translate-list]

[last]: https://img.shields.io/github/last-commit/trekhleb/javascript-algorithms.svg
[commit]: https://github.com/trekhleb/javascript-algorithms/tree/f32172e3db50a73b2c4b09c4363d1fdc40ce2ef6

<!-- doc-templite END generated -->

> **提示**: 其实对应, 每个算法里面多数是维基百科, 的内容, 可能自我查找一些中文材料,理解会好一点 ❤

### 贡献

欢迎 👏 勘误/校对/更新贡献 😊 [具体贡献请看](https://github.com/chinanf-boy/chinese-translate-list#贡献)


## 生活

[help me live , live need money 💰](https://github.com/chinanf-boy/live-need-money)


---

本仓库包含了多种基于 JavaScript 的算法与数据结构。

每种算法和数据结构都有自己的 README 并提供相关说明以及进一步阅读和 YouTube 视频。

> 我们正在编写一本书, 详细解释主要算法。
如果您希望在“JavaScript算法”一书中收到通知
发布会, [订阅 这里](https://upscri.be/402324/).

## 数据结构

数据结构是在计算机中 组织和存储数 据的一种特殊方式, 它可以高效地 访问和修改 数据。更确切地说, 数据结构是数据值的集合, 它们之间的关系、函数或操作可以应用于数据。

`B` - 初学者, `A` - 进阶

* `B` [链表](src/data-structures/linked-list/README.zh.md)
* `B` [双向链表](src/data-structures/doubly-linked-list/README.zh.md)
* `B` [队列](src/data-structures/queue/README.zh.md)
* `B` [栈](src/data-structures/stack/README.zh.md)
* `B` [哈希表](src/data-structures/hash-table/README.zh.md)
* `B` [堆](src/data-structures/heap/README.zh.md)
* `B` [优先队列](src/data-structures/priority-queue/README.zh.md)
* `A` [字典树](src/data-structures/trie/README.zh.md)
* `A` [树](src/data-structures/tree/README.zh.md)
    * `A` [二叉查找树](src/data-structures/tree/binary-search-tree/README.zh.md)
    * `A` [AVL 树](src/data-structures/tree/avl-tree/README.zh.md)
    * `A` [红黑树](src/data-structures/tree/red-black-tree/README.zh.md)
    * `A` [线段树](src/data-structures/tree/segment-tree/README.zh.md) - 使用 最小/最大/总和 范围查询示例
    * `A` [树状数组](src/data-structures/tree/fenwick-tree/README.zh.md) (二叉索引树)
* `A` [图](src/data-structures/graph/README.zh.md) (有向图与无向图)
* `A` [并查集](src/data-structures/disjoint-set/README.zh.md)
* `A` [布隆过滤器](src/data-structures/bloom-filter/README.zh.md)

## 算法

算法是如何解决一类问题的明确规范。 算法是一组精确定义操作序列的规则。

### 算法主题

*  **数学**
  * `B` [Bit 操控](src/algorithms/math/bits/README.zh.md) - set/get/update/clear 位, 乘以/除以 二进制位, 变负 等.
  * `B` [阶乘](src/algorithms/math/factorial/README.zh.md)
  * `B` [斐波那契数](src/algorithms/math/fibonacci/README.zh.md)
  * `B` [素数检测](src/algorithms/math/primality-test/README.zh.md) (排除法)
  * `B` [欧几里得算法](src/algorithms/math/euclidean-algorithm/README.zh.md) - 计算最大公约数 (GCD) 
  * `B` [最小公倍数](src/algorithms/math/least-common-multiple/README.zh.md) (LCM)
  * `B` [素数筛](src/algorithms/math/sieve-of-eratosthenes/README.zh.md) - 查找所有素数达到任何给定限制
  * `B` [判断2次方数](src/algorithms/math/is-power-of-two/README.zh.md) - 检查数字是否为2的幂 (原生和按位算法) 
  * `B` [杨辉三角形](src/algorithms/math/pascal-triangle/README.zh.md)
  * `A` [整数拆分](src/algorithms/math/integer-partition/README.zh.md)
  * `A` [割圆术](src/algorithms/math/liu-hui/README.zh.md) - 基于N-gons的近似π计算
* **集合**
  * `B` [笛卡尔积](src/algorithms/sets/cartesian-product/README.zh.md) - 多集合结果
  * `A` [幂集](src/algorithms/sets/power-set/README.zh.md) - 该集合的所有子集
  * `A` [排列](src/algorithms/sets/permutations/README.zh.md) (有/无重复)
  * `A` [组合](src/algorithms/sets/combinations/README.zh.md) (有/无重复)
  * `A` [洗牌算法](src/algorithms/sets/fisher-yates/README.zh.md) - 随机置换有限序列
  * `A` [最长公共子序列](src/algorithms/sets/longest-common-subsequence/README.zh.md) (LCS)
  * `A` [最长递增子序列](src/algorithms/sets/longest-increasing-subsequence/README.zh.md)
  * `A` [最短公共父序列](src/algorithms/sets/shortest-common-supersequence/README.zh.md) (SCS)
  * `A` [背包问题](src/algorithms/sets/knapsack-problem/README.zh.md) - "0/1" and "Unbound" ones
  * `A` [最大子数列问题](src/algorithms/sets/maximum-subarray/README.zh.md) - BF算法 与 动态规划
  * `A` [组合求和](src/algorithms/sets/combination-sum/README.zh.md) - 查找形成特定总和的所有组合
* **字符串**
  * `A` [莱温斯坦距离](src/algorithms/string/levenshtein-distance/README.zh.md) - 两个序列之间的最小编辑距离
  * `B` [汉明距离](src/algorithms/string/hamming-distance/README.zh.md) - 符号不同的位置数
  * `A` [克努斯-莫里斯-普拉特算法](src/algorithms/string/knuth-morris-pratt/README.zh.md) - 子串搜索
  * `A` [字符串快速查找](src/algorithms/string/rabin-karp/README.zh.md) - 子串搜索
  * `A` [最长公共子串](src/algorithms/string/longest-common-substring/README.zh.md)
  * `A` [正则表达式匹配](src/algorithms/string/regular-expression-matching/README.zh.md)
* **搜索**
  * `B` [线性搜索](src/algorithms/search/linear-search/README.zh.md)
  * `B` [跳转搜索](src/algorithms/search/jump-search/README.zh.md)  (或块搜索)  - 搜索排序数组
  * `B` [二分查找](src/algorithms/search/binary-search/README.zh.md)
  * `B` [插值搜索](src/algorithms/search/interpolation-search/README.zh.md) - 搜索均匀分布的排序数组
* **排序**
  * `B` [冒泡排序](src/algorithms/sorting/bubble-sort/README.zh.md)
  * `B` [选择排序](src/algorithms/sorting/selection-sort/README.zh.md)
  * `B` [插入排序](src/algorithms/sorting/insertion-sort/README.zh.md)
  * `B` [堆排序](src/algorithms/sorting/heap-sort/README.zh.md)
  * `B` [归并排序](src/algorithms/sorting/merge-sort/README.zh.md)
  * `B` [快速排序](src/algorithms/sorting/quick-sort/README.zh.md)
  * `B` [希尔排序](src/algorithms/sorting/shell-sort/README.zh.md)
  * `B` [计数排序](src/algorithms/sorting/counting-sort/README.zh.md)
  * `B` [基数排序](src/algorithms/sorting/radix-sort/README.zh.md)
* **树**
  * `B` [深度优先搜索](src/algorithms/tree/depth-first-search/README.zh.md) (DFS)
  * `B` [广度优先搜索](src/algorithms/tree/breadth-first-search/README.zh.md) (BFS)
* **图**
  * `B` [深度优先搜索](src/algorithms/graph/depth-first-search/README.zh.md) (DFS)
  * `B` [广度优先搜索](src/algorithms/graph/breadth-first-search/README.zh.md) (BFS)
  * `A` [戴克斯特拉算法](src/algorithms/graph/dijkstra/README.zh.md) - 找到图中所有顶点的最短路径
  * `A` [贝尔曼-福特算法](src/algorithms/graph/bellman-ford/README.zh.md) - 找到图中所有顶点的最短路径
  * `A` [弗洛伊德算法](src/algorithms/graph/floyd-warshall/README.zh.md) - 找到所有顶点对 之间的最短路径
  * `A` [判圈算法](src/algorithms/graph/detect-cycle/README.zh.md) - 对于有向图和无向图 (基于DFS和不相交集的版本) 
  * `A` [普林演算法](src/algorithms/graph/prim/README.zh.md) - 寻找加权无向图的最小生成树 (MST) 
  * `B` [克鲁斯克尔演算法](src/algorithms/graph/kruskal/README.zh.md) - 寻找加权无向图的最小生成树 (MST) 
  * `A` [拓扑排序](src/algorithms/graph/topological-sorting/README.zh.md) - DFS 方法
  * `A` [关节点](src/algorithms/graph/articulation-points/README.zh.md) - Tarjan算法 (基于DFS) 
  * `A` [桥](src/algorithms/graph/bridges/README.zh.md) - 基于DFS的算法
  * `A` [欧拉回径与一笔画问题](src/algorithms/graph/eulerian-path/README.zh.md) - Fleury的算法 - 一次访问每个边
  * `A` [哈密顿图](src/algorithms/graph/hamiltonian-cycle/README.zh.md) - 恰好访问每个顶点一次
  * `A` [强连通分量](src/algorithms/graph/strongly-connected-components/README.zh.md) - Kosaraju算法
  * `A` [旅行推销员问题](src/algorithms/graph/travelling-salesman/README.zh.md) - 尽可能以最短的路线访问每个城市并返回原始城市
* **未分类**
  * `B` [汉诺塔](src/algorithms/uncategorized/hanoi-tower/README.zh.md)
  * `B` [旋转矩阵](src/algorithms/uncategorized/square-matrix-rotation/README.zh.md) - 原地算法
  * `B` [跳跃 游戏](src/algorithms/uncategorized/jump-game/README.zh.md) - 回溯, 动态编程 (自上而下+自下而上) 和贪婪的例子
  * `B` [独特(唯一) 路径](src/algorithms/uncategorized/unique-paths/README.zh.md) - 回溯, 动态编程和基于Pascal三角形的例子
  * `B` [雨水收集](src/algorithms/uncategorized/rain-terraces/README.zh.md) - 诱捕雨水问题 (动态编程和暴力版本) 
  * `A` [八皇后问题](src/algorithms/uncategorized/n-queens/README.zh.md)
  * `A` [骑士巡逻](src/algorithms/uncategorized/knight-tour/README.zh.md)

### 算法范式

算法范式是基于类的设计的通用方法或方法的算法。 这是一个比算法概念更高的抽象, 就像一个
算法是比计算机程序更高的抽象。

* **BF算法** - 查找/搜索 所有可能性并选择最佳解决方案
  *  `B` [线性搜索](src/algorithms/search/linear-search)
  *  `B` [雨水收集](src/algorithms/uncategorized/rain-terraces) - 诱导雨水问题
  *  `A` [最大子数列](src/algorithms/sets/maximum-subarray)
  *  `A` [旅行推销员问题](src/algorithms/graph/travelling-salesman) - 尽可能以最短的路线访问每个城市并返回原始城市

* **贪心法** - 在当前选择最佳选项, 不考虑以后情况
  *  `B` [跳跃游戏](src/algorithms/uncategorized/jump-game)
  *  `A` [背包问题](src/algorithms/sets/knapsack-problem)
  *  `A` [戴克斯特拉算法](src/algorithms/graph/dijkstra) - 找到所有图顶点的最短路径
  *  `A` [普里姆算法](src/algorithms/graph/prim) - 寻找加权无向图的最小生成树 (MST)
  *  `A` [克鲁斯卡尔算法](src/algorithms/graph/kruskal) - 寻找加权无向图的最小生成树 (MST)
* **分治法** - 将问题分成较小的部分, 然后解决这些部分
  *  `B` [二分查找](src/algorithms/search/binary-search)
  *  `B` [汉诺塔](src/algorithms/uncategorized/hanoi-tower)
  *  `B` [杨辉三角形](src/algorithms/math/pascal-triangle)
  *  [欧几里得算法](src/algorithms/math/euclidean-algorithm) - 计算最大公约数 (GCD)
  *  `A` [排列](src/algorithms/sets/permutations) (有/无重复)
  *  `A` [组合](src/algorithms/sets/combinations) (有/无重复)
  *  `B` [跳跃游戏](src/algorithms/uncategorized/jump-game)
  *  `B` [归并排序](src/algorithms/sorting/merge-sort)
  *  `B` [快速排序](src/algorithms/sorting/quick-sort)
  *  `B` [树深度优先搜索](src/algorithms/tree/depth-first-search) (DFS)
  *  `B` [图深度优先搜索](src/algorithms/graph/depth-first-search) (DFS)
*  **动态编程** - 使用以前找到的子解决方案构建解决方案
  *  `B` [斐波那契数](src/algorithms/math/fibonacci)
  *  `B` [跳跃游戏](src/algorithms/uncategorized/jump-game)
  *  `B` [独特路径](src/algorithms/uncategorized/unique-paths)
  *  `B` [雨水收集](src/algorithms/uncategorized/rain-terraces) - 疏导雨水问题
  *  `A` [莱温斯坦距离](src/algorithms/string/levenshtein-distance) - 两个序列之间的最小编辑距离
  *  `A` [最长公共子序列](src/algorithms/sets/longest-common-subsequence) (LCS)
  *  `A` [最长公共子串](src/algorithms/string/longest-common-substring)
  *  `A` [最长递增子序列](src/algorithms/sets/longest-increasing-subsequence)
  *  `A` [最短公共子序列](src/algorithms/sets/shortest-common-supersequence)
  *  `A` [0-1背包问题](src/algorithms/sets/knapsack-problem)
  *  `A` [整数拆分](src/algorithms/math/integer-partition)
  *  `A` [最大子数列](src/algorithms/sets/maximum-subarray)
  *  `A` [弗洛伊德算法](src/algorithms/graph/floyd-warshall) - 找到所有顶点对之间的最短路径
  *  `A` [贝尔曼-福特算法](src/algorithms/graph/bellman-ford) - 找到所有图顶点的最短路径
* **回溯法** - 类似于 BF算法 试图产生所有可能的解决方案, 但每次生成解决方案测试如果它满足所有条件, 那么只有继续生成后续解决方案。 否则回溯并继续寻找不同路径的解决方案。
  *  `B` [跳跃游戏](src/algorithms/uncategorized/jump-game)
  *  `B` [独特路径](src/algorithms/uncategorized/unique-paths)
  *  `A` [哈密顿图](src/algorithms/graph/hamiltonian-cycle) - 恰好访问每个顶点一次
  *  `A` [八皇后问题](src/algorithms/uncategorized/n-queens)
  *  `A` [骑士巡逻](src/algorithms/uncategorized/knight-tour)
  * `A` [组合求和](src/algorithms/sets/combination-sum) - 从规定的总和中找出所有的组合
* **B & B**

## 如何使用本仓库

**安装依赖**
```
npm install
```

**执行测试**
```
npm test
```

**按照名称执行测试**
```
npm test -- 'LinkedList'
```

**Playground**

你可以在`./src/playground/playground.js`文件中操作数据结构与算法, 并在`./src/playground/__test__/playground.test.js`中编写测试。

然后, 只需运行以下命令来测试你的 Playground 是否按无误:

```
npm test -- 'playground'
```

## 有用的信息

### 引用

[▶ YouTube](https://www.youtube.com/playlist?list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)

### 大O符号

大O符号中指定的算法的增长顺序。

![Big O graphs](./assets/big-o-graph.png)

源: [Big O Cheat Sheet](http://bigocheatsheet.com/).

以下是一些最常用的 大O标记法 列表以及它们与不同大小输入数据的性能比较。

| 大O标记法 | 计算10个元素 | 计算100个元素 | 计算1000个元素  |
| -------------- | ---------------------------- | ----------------------------- | ------------------------------- |
| **O(1)**       | 1                            | 1                             | 1                               |
| **O(log N)**   | 3                            | 6                             | 9                               |
| **O(N)**       | 10                           | 100                           | 1000                            |
| **O(N log N)** | 30                           | 600                            | 9000                            |
| **O(N^2)**     | 100                          | 10000                         | 1000000                         |
| **O(2^N)**     | 1024                         | 1.26e+29                      | 1.07e+301                       |
| **O(N!)**      | 3628800                      | 9.3e+157                      | 4.02e+2567                      |

### 数据结构操作的复杂性

| 数据结构          | 连接    | 查找    | 插入 | 删除  |
| ----------------------- | :-------: | :-------: | :-------: | :-------: |
| **数组**               | 1         | n         | n         | n         |
| **栈**               | n         | n         | 1         | 1         |
| **队列**               | n         | n         | 1         | 1         |
| **链表**         | n         | n         | 1         | 1         |
| **哈希表**          | -         | n         | n         | n         |
| **二分查找树**  | n         | n         | n         | n         |
| **B树**              | log(n)    | log(n)    | log(n)    | log(n)    |
| **红黑树**      | log(n)    | log(n)    | log(n)    | log(n)    |
| **AVL树**            | log(n)    | log(n)    | log(n)    | log(n)    |

### 数组排序算法的复杂性

| 名称                  | 最优      | 平均   | 最坏         | 内存    | 稳定    |
| --------------------- | :-------: | :-------: | :-----------: | :-------: | :-------: |
| **冒泡排序**       | n         | n^2       | n^2           | 1         | Yes       |
| **插入排序**    | n         | n^2       | n^2           | 1         | Yes       |
| **选择排序**    | n^2       | n^2       | n^2           | 1         | No        |
| **堆排序**         | n log(n)  | n log(n)  | n log(n)      | 1         | No        |
| **归并排序**        | n log(n)  | n log(n)  | n log(n)      | n         | Yes       |
| **快速排序**        | n log(n)  | n log(n)  | n^2           | log(n)    | No        |
| **希尔排序**        | n log(n)  | 取决于差距序列   | n (log(n))^2  | 1         | No        |
