
# 红黑树

红黑树 是 计算机科学中 的 一种自平衡 二叉搜索树. 二叉树的每个节点都有一个额外的位,该位通常表示为节点的颜色 (红色或黑色) . 这些颜色位用于确保 树在插入和删除期间 保持近似平衡. 

通过满足某些属性的方式,用两种颜色之一 绘制树的每个节点 来保留平衡,这些属性共同限制 树 在最坏情况下 的不平衡程度. 修改树时,随后重新排列新树,并重新绘制 以恢复着色属性. 这些属性的设计使得可以有效地执行这种重新排列和重新着色. 

树的平衡并不完美,但它足以让它保证`O(log n)`的搜索时间,`n`是树中元素的总数. 插入和删除操作 以及 树重新排列和重新着色 执行时间也是`O(log n)`. 

红黑树的一个例​​子: 

![red-black tree](https://upload.wikimedia.org/wikipedia/commons/6/66/Red-black_tree_example.svg)

## 属性

除了 对二叉搜索树施加的要求 之外,红黑树还必须满足以下要求: 

-   每个节点都是红色或黑色. 
-   根是黑色的. 有时会省略此规则. 由于根始终可以 从红色变为黑色,但不一定相反,因此该规则对分析几乎没有影响. 
-   所有 叶子 (NIL) 都是黑色的. 
-   如果节点为红色,则其子节点 均为黑色. 
-   从 给定节点 到 其任何后代NIL节点 的 每条路径 都包含 相同数量 的黑色节点. 

一些定义: 从 根到节点的黑节点数 是 节点的 **黑色深度**;从 根到叶子的所有路径中的黑色节点 的 统一数量称为 **黑色高度** 红黑树. 

这些约束 强制执行 红黑树的关键属性: *从根到最远叶子的路径 不超过 从根到最近叶子的路径 的两倍*. 结果是 树 大致高度平衡. 由于诸如 插入,删除和查找值之类的操作 需要 最坏情况的时间来使 树的高度成比例,因此与 最普通的二叉搜索树不同,这种高度的理论上限,允许红黑树在最坏的情况下都是有效的. 

## 在插入期间平衡

### 如果叔叔是红的

![Red Black Tree Balancing](https://www.geeksforgeeks.org/wp-content/uploads/redBlackCase2.png)

### 如果叔叔是黑的

-   左左案 (`p`是`g`左边的孩子 和 `x`是`p`左边的孩子) 

-   左右案 (`p`是`g`左边的孩子 和 `x`是`p`右边的孩子) 

-   右右案 (`p`是`g`右边的孩子 和 `x`是`p`右边的孩子) 

-   右左案 (`p`是`g`右边的孩子 和 `x`是`p`左边的孩子) 

#### 左左案例 (见g,p和x) 

![Red Black Tree Balancing](https://www.geeksforgeeks.org/wp-content/uploads/redBlackCase3a1.png)

#### 左右案例 (见g,p和x) 

![Red Black Tree Balancing](https://www.geeksforgeeks.org/wp-content/uploads/redBlackCase3d.png)

#### 右右案例 (见g,p和x) 

![Red Black Tree Balancing](https://www.geeksforgeeks.org/wp-content/uploads/redBlackCase3c.png)

#### 右左案 (见g,p和x) 

![Red Black Tree Balancing](https://www.geeksforgeeks.org/wp-content/uploads/redBlackCase3c.png)

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Red%E2%80%93black_tree)
-   [Red Black Tree Insertion by Tushar Roy (YouTube)](https://www.youtube.com/watch?v=UaLIHuR1t8Q&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=63)
-   [Red Black Tree Deletion by Tushar Roy (YouTube)](https://www.youtube.com/watch?v=CTvfzU_uNKE&t=0s&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=64)
-   [Red Black Tree Insertion on GeeksForGeeks](https://www.geeksforgeeks.org/red-black-tree-set-2-insert/)
-   [Red Black Tree Interactive Visualisations](https://www.cs.usfca.edu/~galles/visualization/RedBlack.html)
