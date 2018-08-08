
# 拉宾卡普算法

在计算机科学中,Rabin-Karp算法是由 Richard M.Karp 和 Michael O.Rabin (1987) 创建的字符串搜索算法,其使用哈希来查找文本中的 一组模式字符串中的任何一个. 

## 复杂性性

对于长度为`n`和`p`模式的组合文本
长度为`m`，其平均和最佳案例运行时间为
`O(n + m)`和空间`O(p)`，但其最坏情况时间是`O(n * m)`。

## 应用

该算法的实际应用是检测抄袭. 
在给定源材料的情况下,该算法可以快速在纸张中搜索来自 源材料的句子实例,忽略诸如 大小写和标点符号 之类的细节. 

由于所搜索的字符串丰富,单字符串搜索算法是不切实际的. 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Rabin%E2%80%93Karp_algorithm)
-   [YouTube](https://www.youtube.com/watch?v=H4VrKHVG5qI&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
