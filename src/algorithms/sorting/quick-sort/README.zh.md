# 快速排序

Quicksort 是一种分而治之的算法. Quicksort 首先将一个大数组分成两个较小的子数组: 低元素和高元素. Quicksort 然后可以递归地对子数组进行排序

步骤为：

1. 从数列中挑出一个元素，称为"基准"（pivot），
2. 重新排序数列，所有比基准值小的元素摆放在基准前面，所有比基准值大的元素摆在基准后面（相同的数可以到任何一边）。在这个分区结束之后，该基准就处于数列的中间位置。这个称为分区（partition）操作。
3. 递归地（recursively）把小于基准值元素的子数列和大于基准值元素的子数列排序。

快速排序算法的动画可视化. 水平线是基准值.

![Quicksort](https://upload.wikimedia.org/wikipedia/commons/6/6a/Sorting_quicksort_anim.gif)

## 复杂性

| 名称         |  最好   |  平均   |     最差      |    内存    | 稳定 | 注释                                             |
| ------------ | :-----: | :-----: | :-----------: | :--------: | :--: | :----------------------------------------------- |
| **快速排序** | nlog(n) | nlog(n) | n<sup>2</sup> | log(n) | 没有 | Quicksort 通常使用 O(log(n))的堆栈空间 ,也就是原地（in-place）分区的版本 |

## 参考

- [Wikipedia](https://en.wikipedia.org/wiki/Quicksort)
- [YouTube](https://www.youtube.com/watch?v=SLauY6PpjW4&index=28&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
- [维基百科](https://zh.wikipedia.org/wiki/快速排序)
