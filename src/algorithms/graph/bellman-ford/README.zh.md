
# 贝尔曼-福特算法

贝尔曼-福特算法是一种算法,用于计算从 单个源顶点 到 加权有向图中所有其他顶点的最短路径. 对于相同的问题,它比 戴克斯特拉算法慢,但是更通用,因为它能够处理其中一些边权重是负数的图. 

![Bellman-Ford](https://upload.wikimedia.org/wikipedia/commons/2/2e/Shortest_path_Dijkstra_vs_BellmanFord.gif)

## 复杂性

>给定图G(V, E)（其中V、E分别为图G的顶点集与边集），源点s，

- 最坏的表现`O(|V||E|)`
- 最佳表现`O(|E|)`
- 最糟糕的空间复杂性`O(|V|)`

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Bellman%E2%80%93Ford_algorithm)
-   [On YouTube by Michael Sambol](https://www.youtube.com/watch?v=obWXjtg0L64&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
