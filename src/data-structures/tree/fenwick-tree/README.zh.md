
# Fenwick树/二叉查找树

一个 **芬威克树** 要么**二叉查找树**是一种数据结构,可以有效地更新元素,并计算数字表中的前缀和. 

与 平坦的数字数组 相比,Fenwick树 在两个操作之间 实现了更好的平衡: 元素更新和前缀和的计算. 

在平面阵列`n`中,您可以存储元素,或 前缀总和. 在第一种情况下,计算前缀和需要线性时间;

在第二种情况下,更新数组元素需要 线性时间 (在两种情况下,其他操作可以在恒定时间内执行) . Fenwick树执行两个操作是 `O(log n)`时间. 这是通过将 数字表示为树 来实现的, 其中每个节点的值是该子树中数字的总和. 树结构允许仅操作`O(log n)`节点的访问. 

## 实现说明

二叉查找树表示为数组. 二叉查找树的每个节点 存储 给定数组的一些元素的总和. 二叉查找树的大小等于`n`,`n`是输入数组的大小. 在当前的实现中,我们使用 size 作为`n+1`为了便于实现. 所有索引都是 基于1 的. 

![Binary Indexed Tree](https://www.geeksforgeeks.org/wp-content/uploads/BITSum.png)

在下图中,您可以看到为 数组`[1, 2, 3, 4, 5]` 创建二叉查找树的动画示例,通过逐个插入. 

![Fenwick Tree](https://upload.wikimedia.org/wikipedia/commons/d/dc/BITDemo.gif)

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Fenwick_tree)
-   [GeeksForGeeks](https://www.geeksforgeeks.org/binary-indexed-tree-or-fenwick-tree-2/)
-   [YouTube](https://www.youtube.com/watch?v=CWDQJGaN1gY&index=18&t=0s&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
