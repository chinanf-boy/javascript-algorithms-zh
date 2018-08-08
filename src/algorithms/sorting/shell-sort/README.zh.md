# 希尔排序

希尔排序，也称递减增量排序算法，是插入排序的一种更高效的改进版本。希尔排序是非稳定排序算法。

希尔排序是基于插入排序的以下两点性质而提出改进方法的：

- 插入排序在对几乎已经排好序的数据操作时，效率高，即可以达到线性排序的效率
- 但插入排序一般来说是低效的，因为插入排序每次只能将数据移动一位

![Shellsort](https://upload.wikimedia.org/wikipedia/commons/d/d8/Sorting_shellsort_anim.gif)

## 希尔排序如何工作

对于我们的例子和易于理解,我们采取间隔为`4`. 创建位于 4 个位置间隔的所有值的虚拟子列表. 这些值是`{35, 14}`,`{33, 19}`,`{42, 27}`和`{10, 44}`

![Shellsort](https://www.tutorialspoint.com/data_structures_algorithms/images/shell_sort_gap_4.jpg)

我们比较每个子列表中的值,并在原始数组中交换它们 (如果需要) . 完成此步骤后,新数组应如下所示

![Shellsort](https://www.tutorialspoint.com/data_structures_algorithms/images/shell_sort_step_1.jpg)

然后,我们采用 `2` 的间隔,这个间隙产生两个子列表

- `{14, 27, 35, 42}`,`{19, 10, 33, 44}`

![Shellsort](https://www.tutorialspoint.com/data_structures_algorithms/images/shell_sort_gap_2.jpg)

我们比较并交换原始数组中的值 (如果需要) . 完成此步骤后,数组应如下所示

![Shellsort](https://www.tutorialspoint.com/data_structures_algorithms/images/shell_sort_step_2.jpg)

最后,我们使用值间隔为`1` 对数组的其余部分进行排序.这个 顺序列表 使用插入排序对数组进行排序.

![Shellsort](https://www.tutorialspoint.com/data_structures_algorithms/images/shell_sort.jpg)

## 复杂性

| 名称       |  最好   |      平均      |             最差             |  内存 | 稳定 | 注释 |
| ---------- | :-----: | :------------: | :--------------------------: | :---: | :--: | :--- |
| **希尔排序** | n&nbsp;log(n) | 取决于差距序列 | n(log(n))<sup>2</sup> |   1   | 没有 |      |

## 参考

- [Tutorials Point](https://www.tutorialspoint.com/data_structures_algorithms/shell_sort_algorithm.htm)
- [Wikipedia](https://en.wikipedia.org/wiki/Shellsort)
- [维基百科](https://zh.wikipedia.org/wiki/%E5%B8%8C%E5%B0%94%E6%8E%92%E5%BA%8F)
