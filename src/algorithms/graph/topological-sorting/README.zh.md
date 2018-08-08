
# 拓扑排序

在计算机科学领域,有向图的拓扑排序或拓扑排序是其顶点的线性排序，使得对于从顶点 `u`到顶点 `v`的每个有向边 `uv`， ` u`在排序中都在`v`之前。 例如，图形的顶点可以表示要执行的任务，并且边缘可以表示一个任务必须在另一个任务之前执行的约束; 在这个应用中，拓扑排序只是一个有效的任务顺序。

 如果且仅当图形没有定向循环，即如果它是[有向无环图（DAG）](https://zh.wikipedia.org/wiki/DAG)，则拓扑排序是可能的。 任何 DAG 具有至少一个拓扑排序，并且已知这些算法用于在线性时间内构建任何 DAG 的拓扑排序。

![Directed Acyclic Graph](https://upload.wikimedia.org/wikipedia/commons/c/c6/Topological_Ordering.svg)

有向无环图的拓扑排序: 每个边从排序中的较早 (左上) 到排序的后面 (右下) . 有向图是非循环的,当且仅当它具有拓扑排序时. 

## 例

![Topologic Sorting](https://upload.wikimedia.org/wikipedia/commons/0/03/Directed_acyclic_graph_2.svg)

上面显示的图表有许多有效的拓扑排序,包括: 

-   `5, 7, 3, 11, 8, 2, 9, 10` (视觉从左到右,从上到下) 
-   `3, 5, 7, 8, 11, 2, 9, 10` (最小编号的可用顶点首先) 
-   `5, 7, 3, 8, 11, 10, 9, 2` (最少边) 
-   `7, 5, 11, 3, 10, 8, 9, 2` (最大编号的可用顶点优先) 
-   `5, 7, 11, 2, 3, 8, 9, 10` (尝试从上到下,从左到右) 
-   `3, 7, 8, 5, 11, 10, 2, 9` (任意) 

## 应用

拓扑排序的规范应用是在 **安排一系列工作** 或 基于其依赖关系的任务. 作业由顶点表示,并且有一个边`x`到`y`,如果工作`x`必须在`y`工作前完成 (例如,洗衣服时,洗衣机必须在我们将衣服放入烘干机之前完成) . 然后,拓扑排序给出了执行作业的顺序. 

其他应用是**依赖解决**. 每个顶点都是一个包,每个边都是包的依赖`a`在包`b`上. 然后拓扑排序将提供一系列安装依赖关系,以便每个下一个依赖关系都要在之前安装其依赖包. 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Topological_sorting)
-   [Topological Sorting on YouTube by Tushar Roy](https://www.youtube.com/watch?v=ddTC4Zovtbc&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
