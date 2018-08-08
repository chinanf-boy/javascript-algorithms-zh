
# 哈希表

在计算中,哈希表 (哈希映射) 是实现 关联数组 抽象 数据类型 的数据结构,该结构可以将 key 映射到值. 哈希表使用 哈希函数 来计算 buckets 或 slots 的索引,从中可以找到所需的值

理想情况下,哈希函数会将每个key 分配给一个唯一的 bucket ,但 大多数哈希表设计 采用不完美的哈希函数,这可能导致哈希冲突,其中哈希函数为 多个key  生成相同的索引. 必须以某种方式适应这种碰撞. 

![Hash Table](https://upload.wikimedia.org/wikipedia/commons/7/7d/Hash_table_3_1_1_0_1_0_0_SP.svg)

通过 单独的链接 解决了哈希冲突. 

![Hash Collision](https://upload.wikimedia.org/wikipedia/commons/d/d0/Hash_table_5_0_1_1_1_1_1_LL.svg)

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Hash_table)
-   [YouTube](https://www.youtube.com/watch?v=shs0KM3wKv8&index=4&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
