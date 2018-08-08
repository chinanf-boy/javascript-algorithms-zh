
# 线段树

在计算机科学中,也称为统计树的线段树 是用于存储关于 间隔或分段的信息的树数据结构. 它允许查询哪些存储的段包含给定的点. 原则上,它是静态结构; 也就是说,它是一个一旦构建就无法修改的结构. 类似的数据结构是 间隔树. 

线段树是二叉树. 树的根代表整个数组. 根的两个子节点代表数组的上一段与下一段数组. 类似地,每个节点的子节点都有父/母的一半. 

我们自下而上 构建树,每个节点的值是 其子节点值之间的"最小值" (或任何其他函数) . 这将需要`O(n log n)`时间. 完成的操作数 是 树的高度,即`O(log n)`. 要进行范围查询,每个节点将查询分为两部分,每次查询一个子查询. 如果查询包含节点的整个子数组,我们可以在节点处使用 预先计算的值. 使用此优化,我们只能证明`O(log n)`最快的完成时间. 

![Min Segment Tree](https://www.geeksforgeeks.org/wp-content/uploads/RangeMinimumQuery.png)

![Sum Segment Tree](https://www.geeksforgeeks.org/wp-content/uploads/segment-tree1.png)

## 应用

线段树是一种数据结构,旨在有效地执行某些阵列操作 - 尤其是涉及 范围查询的那些操作. 

分段树的应用在计算 几何和地理信息 系统领域. 

线段树的当前实现意味着您可以将 任何二进制 (具有两个输入参数) 函数传递给它,因此您可以对各种函数进行范围查询. 在测试中,你可以尝试做`min`,`max`和`sam`的例子,在线段树的范围查询上. 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Segment_tree)
-   [YouTube](https://www.youtube.com/watch?v=ZBHKZF5w4YU&index=65&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
-   [GeeksForGeeks](https://www.geeksforgeeks.org/segment-tree-set-1-sum-of-given-range/)
