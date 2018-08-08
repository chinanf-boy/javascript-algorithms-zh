
# 计数排序

计数排序（Counting sort）是一种稳定的线性时间排序算法。计数排序使用一个额外的数组 `C` ，其中第i个元素是待排序数组 `A`中值等于 `i`的元素的个数。然后根据数组 `C`来将 `A`中的元素排到正确的位置。

当输入的元素是 `n`个 **0 到 k** 之间的整数时，它的运行时间是 `O(n + k)`。计数排序不是比较排序，排序的速度快于任何比较排序算法。

由于用来计数的数组 `C` 的长度取决于待排序数组中数据的范围（等于待排序数组的最大值与最小值的差加上1），这使得计数排序对于数据范围很大的数组，需要大量时间和内存。例如：计数排序是用来排序 0到100 之间的数字的最好的算法，但是它不适合按字母顺序排序人名。但是，计数排序可以用在基数排序算法中，能够更有效的排序数据范围很大的数组。

通俗地理解，例如有10个年龄不同的人，统计出有8个人的年龄比A小，那A的年龄就排在第9位，用这个方法可以得到其他每个人的位置，也就排好了序。当然，年龄有重复时需要特殊处理（保证稳定性），这就是为什么最后要反向填充目标数组，以及将每个数字的统计减去1的原因。

## 算法

**第一步**

在第一步中,我们计算输入数组的所有元素的计数`A` (有几个). 然后将结果存储在计数数组中`C`. 我们计算的方式如下所示. 

![Counting Sort](https://3.bp.blogspot.com/-jJchly1BkTc/WLGqCFDdvCI/AAAAAAAAAHA/luljAlz2ptMndIZNH0KLTTuQMNsfzDeFQCLcB/s1600/CSortUpdatedStepI.gif)

**第二步**

在第二步中,对所有的计数累加 (从`C` 中的第一个元素开始，每一项和前一项相加）

![Counting Sort](https://1.bp.blogspot.com/-1vFu-VIRa9Y/WLHGuZkdF3I/AAAAAAAAAHs/8jKu2dbQee4ap9xlVcNsILrclqw0UxAVACLcB/s1600/Step-II.png)

**第三步**

反向填充目标数组：将每个元素 `i`放在新数组的第 `C[i]` 项，每放一个元素就将`C[i]`减去`1`

> 注意是 减掉 `1` 之后的 值才是数组的索引， 因为数组从0开始索引的嘛

![Counting Sort](https://1.bp.blogspot.com/-xPqylngqASY/WLGq3p9n9vI/AAAAAAAAAHM/JHdtXAkJY8wYzDMBXxqarjmhpPhM0u8MACLcB/s1600/ResultArrayCS.gif)

## 复杂性

| 名称      |   最好  |   平均  |   最差  |   内存  |  稳定 | 注释            |
| ------- | :---: | :---: | :---: | :---: | :-: | :------------ |
| **数排序** | n + r | n + r | n + r | n + r |  是  | r  - 数组中的最大数字 |

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Counting_sort)
-   [YouTube](https://www.youtube.com/watch?v=OKd534EWcdk&index=61&t=0s&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
-   [EfficientAlgorithms](https://efficientalgorithms.blogspot.com/2016/09/lenear-sorting-counting-sort.html)
- [维基百科](https://zh.wikipedia.org/wiki/%E8%AE%A1%E6%95%B0%E6%8E%92%E5%BA%8F)
