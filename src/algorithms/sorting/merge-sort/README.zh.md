# 归并排序

在计算机科学中,归并排序 (通常拼写为 mergesort) 是一种有效的,通用的,基于比较的排序算法. 大多数实现产生稳定的排序,这意味着实现保留排序输出中 相等元素的输入顺序. Mergesort 是一种分治算法,由 John von Neumann 于 1945 年发明.

归并排序的一个例子. 首先将列表划分为最小单位 (1 个元素) ,然后将每个元素与相邻列表进行比较,以对两个相邻列表进行排序和归并. 最后,对所有元素进行 排序和合并.

![Merge Sort](https://upload.wikimedia.org/wikipedia/commons/c/cc/Merge-sort-example-300px.gif)

一种递归合并排序算法,用于对 7 个整数值的数组进行排序. 这些是人类用来模拟归并排序 (自上而下) 的步骤.

![Merge Sort](https://upload.wikimedia.org/wikipedia/commons/e/e6/Merge_sort_algorithm_diagram.svg)

## 复杂性

| 名称         |  最好   |  平均   |  最差   |  内存 | 稳定 | 注释 |
| ------------ | :-----: | :-----: | :-----: | :---: | :--: | :--- |
| **归并排序** | nlog(n) | nlog(n) | nlog(n) |   n   |  是  |      |

## 参考

- [Wikipedia](https://en.wikipedia.org/wiki/Merge_sort)
- [YouTube](https://www.youtube.com/watch?v=KF2j-9iSf4Q&index=27&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
