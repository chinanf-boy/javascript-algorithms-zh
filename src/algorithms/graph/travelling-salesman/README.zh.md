
# 旅行推销员问题

旅行商问题 (TSP) 提出以下问题: "给定一系列城市和每对城市之间的距离，求解访问每一座城市一次并回到起始城市的最短回路?"

![Travelling Salesman](https://upload.wikimedia.org/wikipedia/commons/1/11/GLPK_solution_of_a_travelling_salesman_problem.svg)

旅行商问题的解决方案: 黑线表示连接每个红点的最短循环. 

![Travelling Salesman Graph](https://upload.wikimedia.org/wikipedia/commons/3/30/Weighted_K4.svg)

可以将TSP建模为无向加权图,使得城市是图的顶点,路径是图的边,路径的距离是边的权重. 它是在完全访问每个其他顶点**一次**后(`在指定顶点开始和结束`)最小化问题. 通常,模型是完整的图形 (即,每对顶点通过边连接) . 如果两个城市之间不存在路径,则添加任意长边将完成图形而不会影响最佳巡视. 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Travelling_salesman_problem)
