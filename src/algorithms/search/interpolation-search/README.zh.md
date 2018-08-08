
# 插值搜索

**插值搜索**是一种搜索 数组中的key 的算法,该数组已按照 分配给 key 的数值 ( key 值) 排序. 

例如,我们有一个`n`大小的 均匀分布排序数组`arr[]`,我们需要编写一个函数来搜索特 定元素`x`在数组中. 

**线性搜索**找到元素`O(n)`时间,**跳转搜索**需要`O(√ n)`时间和 **二叉查找**采取`O(Log n)`时间. 

该**插值搜索**是二叉查找实例的改进,其中排序数组中的值是*均匀*分散式. 二叉查找总是转到中间元素进行检查. 另一方面,插值搜索 可以根据 被搜索的 key 的值 去往不同的位置. 例如,如果 key 的值更接近最后一个元素,则 插值搜索可能开始向结束侧搜索. 


要查找要搜索的位置,请使用以下公式: 

    // 公式的想法是返回更高的pos值
    // 想要更高就是,当要搜索的元素更接近 arr[hi] 或
    // 更接近 arr[lo] 
    pos = lo + ((x - arr[lo]) * (hi - lo) / (arr[hi] - arr[Lo]))

    arr[] - 需要搜索元素的数组
    x - 要搜索的元素
    lo - arr []中的起始索引
    hi - arr []中的结束索引

## 复杂性

**时间复杂**: `O(log(log(n))`

## 参考

-   [GeeksForGeeks](https://www.geeksforgeeks.org/interpolation-search/)
-   [Wikipedia](https://en.wikipedia.org/wiki/Interpolation_search)
