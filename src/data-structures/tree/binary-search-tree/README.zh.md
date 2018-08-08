# 二叉查找树

在计算机科学中, 二叉查找树（BST）, 有时称为 有序或排序的二叉树, 是一种特殊类型的容器：存储“项目”的数据结构（例如数字, 名称等）在内容中。它们允许快速查找, 添加和删除 items, 可以用来实现动态集合, 允许按 key 查找项目 或 查找表（例如, 通过姓名查找某人的电话号码）。

二叉查找树使其 key 按 顺序排列, 以便查找,还有其他操作可以使用二叉查找的原则：在树中寻找 key （或插入新 key 的地方）时, 他们从 总树干 到 树叶 , 与存储在树的节点进行 key 比较, 并在此基础上决定, 继续向左或向右查找子树。平均而言, 这意味着每次比较都跳过大约一半的树 (每下一层), 这样每个查找, 插入或删除 就是 (`logN`) 了。这是比 在（未排序）数组中 按 key 查找项目所需的线性时间要好得多, 但比对哈希表的相应操作 慢。

大小为9 且 深度为3的二叉查找树, 在根处为8。
叶子没有绘制。

> 每个点下面 右边的 比 左边的 大

![Binary Search Tree](https://upload.wikimedia.org/wikipedia/commons/d/da/Binary_search_tree.svg)

## References

- [Wikipedia](https://en.wikipedia.org/wiki/Binary_search_tree)
- [Inserting to BST on YouTube](https://www.youtube.com/watch?v=wcIRPqTR3Kc&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=9&t=0s)
- [BST Interactive Visualisations](https://www.cs.usfca.edu/~galles/visualization/BST.html)
d
