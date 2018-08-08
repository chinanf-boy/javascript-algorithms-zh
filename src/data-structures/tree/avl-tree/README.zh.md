
# AVL树

在计算机科学中,AVL树 (以发明者 Adelson-Velsky 和 Landis 命名) 是一种 自平衡 二元搜索树. 这是第一个发明的数据结构. 在AVL树中,任何节点 的 两个子树的高度 最多相差一个; 如果在任何时候它们相差 多于一个,则重新平衡以恢复此属性. 查找,插入和删除 在 平均和最差情况 下  都需要`O(log n)`的时间,其中 n 是操作之前 树中节点的数量. 插入和删除 可能需要通过 一个或多个树 旋转来重新平衡树. 

动画显示将多个元素插入到 AVL树 中. 它包括左,右,左右和左右旋转. 

![AVL Tree](https://upload.wikimedia.org/wikipedia/commons/f/fd/AVL_Tree_Example.gif)

具有平衡因子的AVL树 (绿色) 

![AVL Tree](https://upload.wikimedia.org/wikipedia/commons/a/ad/AVL-tree-wBalance_K.svg)

### AVL树旋转

**左左旋转**

![Left-Left Rotation](http://btechsmartclass.com/DS/images/LL%20Rotation.png)

**右旋转**

![Right-Right Rotation](http://btechsmartclass.com/DS/images/RR%20Rotation.png)

**左右旋转**

![Left-Right Rotation](http://btechsmartclass.com/DS/images/LR%20Rotation.png)

**左右旋转**

![Right-Right Rotation](http://btechsmartclass.com/DS/images/RL%20Rotation.png)

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/AVL_tree)
-   [Tutorials Point](https://www.tutorialspoint.com/data_structures_algorithms/avl_tree_algorithm.htm)
-   [BTech](http://btechsmartclass.com/DS/U5_T2.html)
-   [AVL Tree Insertion on YouTube](https://www.youtube.com/watch?v=rbg7Qf8GkQ4&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=12&)
-   [AVL Tree Interactive Visualisations](https://www.cs.usfca.edu/~galles/visualization/AVLtree.html)
