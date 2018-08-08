# 堆排序

Heapsort 是一种基于比较的排序算法. Heapsort 可以被认为是一种改进的选择排序: 像该算法一样,它将其输入分为 排序(大/小顺序的)区域和未排序区域,并通过提取最大元素,并将其移动到排序区域来迭代缩小未排序区域. 改进包括使用堆数据结构 而不是 线性结构 来搜索找到最大值.

![Algorithm Visualization](https://upload.wikimedia.org/wikipedia/commons/1/1b/Sorting_heapsort_anim.gif)

![Algorithm Visualization](https://upload.wikimedia.org/wikipedia/commons/4/4d/Heapsort-example.gif)

## 复杂性

| 名称       |     最好      |     平均      |     最差      | 内存 | 稳定 | 注释 |
| ---------- | :-----------: | :-----------: | :-----------: | :--: | :--: | :--- |
| **堆排序** | nlog(n) | nlog(n) | nlog(n) |  1   | 没有 |      |

## 参考

[Wikipedia](https://en.wikipedia.org/wiki/Heapsort)
