
# 二叉查找

在计算机科学中,二叉查找 (也称为半间隔查找,对数查找或二叉查找) 是一种查找算法,用于查找 已排序数组中 目标值的位置. 二叉查找将 目标值与数组的中间元素进行比较; 如果它们不相等,则目标不能说谎(类似 大于或小于)的一半被消除,并且继续查找剩下的一半直到它成功. 如果查找以剩余的一半为空结束,则目标不在数组中. 

![Binary Search](https://upload.wikimedia.org/wikipedia/commons/8/83/Binary_Search_Depiction.svg)

## 复杂性

**时间复杂性**: `O(log(n))`- 因为我们在每次下一次迭代时将查找区域分成两部分. 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Binary_search_algorithm)
-   [YouTube](https://www.youtube.com/watch?v=P3YID7liBug&index=29&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
