
# 戴克斯特拉算法

戴克斯特拉算法是用于 在图中的节点之间 找到最短路径的算法,其可以表示例如 道路网络. 

该算法存在许多变体;戴克斯特拉的原始版本找到两个顶点之间的最短路径，但是更常见的变体固定了一个顶点作为源节点然后找到该顶点到图中所有其它节点的最短路径，产生一个最短路径树

![Dijkstra](https://upload.wikimedia.org/wikipedia/commons/5/57/Dijkstra_Animation.gif)

戴克斯特拉算法找到 `a`和`b`之间的最短路径. 它选择具有最低距离的未访问顶点,计算通过它到每个未访问的邻居的距离,并且如果更小则更新邻居的距离. 当与邻居完成时,马克笔标记已访问 (设置为红色) . 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)
-   [On YouTube by Nathaniel Fan](https://www.youtube.com/watch?v=gdmfOwyQlcI&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
-   [On YouTube by Tushar Roy](https://www.youtube.com/watch?v=lAXZGERcDf4&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
