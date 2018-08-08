
# 克鲁斯克尔演算法

克鲁斯克尔演算法是一种最小生成树算法,它可以找到连接森林中任意两棵树的最小权重边. 它是图论中的一种贪婪算法,因为它找到了连接加权图的最小生成树,在每一步增加了成本弧. 这意味着它找到形成包含每个顶点的树的边的子集,其中树中所有边的总权重被最小化. 如果图形并没连接,则它会找到最小生成林 (每个连接组件的最小生成树) . 

![Kruskal Algorithm](https://upload.wikimedia.org/wikipedia/commons/5/5c/MST_kruskal_en.gif)

![Kruskal Demo](https://upload.wikimedia.org/wikipedia/commons/b/bb/KruskalDemo.gif)

基于 欧几里德距离 的 克鲁斯克尔演算法演示. 

## 最小生成树

一个**最小生成树** (MST) 或 最小权重生成树 是 连接 具有边权重(非)有向图的边子集,其将所有顶点连接在一起,没有任何循环,并且具有最小可能的总边权重. 也就是说,它是一种生成树,其边权重之和尽可能小. 一般来说,任何边加权无向图 (不一定连接) 具有最小生成林,其是连接组件的最小生成树的并集. 

![Minimum Spanning Tree](https://upload.wikimedia.org/wikipedia/commons/d/d2/Minimum_spanning_tree.svg)

平面图及其最小生成树. 每个都标有其重量,这里的重量大致与其长度成正比. 

![Minimum Spanning Tree](https://upload.wikimedia.org/wikipedia/commons/c/c9/Multiple_minimum_spanning_trees.svg)

此图显示图表中可能有多个最小生成树. 在该图中,图下面的两棵树是给定图的最小生成树的两种可能性. 

## 参考

-   [Minimum Spanning Tree on Wikipedia](https://en.wikipedia.org/wiki/Minimum_spanning_tree)
-   [Kruskal's Algorithm on Wikipedia](https://en.wikipedia.org/wiki/Kruskal%27s_algorithm)
-   [Kruskal's Algorithm on YouTube by Tushar Roy](https://www.youtube.com/watch?v=fAuF0EuZVCk&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
-   [Kruskal's Algorithm on YouTube by Michael Sambol](https://www.youtube.com/watch?v=71UQH7Pr9kU&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
