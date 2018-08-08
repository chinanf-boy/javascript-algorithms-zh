
# 普里姆算法

在计算机科学,**普里姆算法**是一种贪心算法,可以为加权无向图 找到最小生成树. 

意即由此算法搜索到的边子集所构成的树中，不但包括了连通图里的所有顶点，且其所有边的权值之和亦为最小. 

![Prim's Algorithm](https://upload.wikimedia.org/wikipedia/commons/f/f7/Prim%27s_algorithm.svg)

普里姆算法从顶点开始`A`. 在第三步,边`BD`和`AB`两者都有重量`2`,所以`BD`是任意选择的. 在那一步之后,`AB`不再是添加到树中的候选者,因为它链接了树中已有的两个节点. 

## 最小生成树

一个**最小生成树** (MST) 或 最小权重生成树 是 连接 具有边权重(非)有向图的边子集,其将所有顶点连接在一起,没有任何循环,并且具有最小可能的总边权重. 也就是说,它是一种生成树,其边权重之和尽可能小. 一般来说,任何边加权无向图 (不一定连接) 具有最小生成林,其是连接组件的最小生成树的并集. 

![Minimum Spanning Tree](https://upload.wikimedia.org/wikipedia/commons/d/d2/Minimum_spanning_tree.svg)

平面图及其最小生成树. 每个都标有其重量,这里的重量大致与其长度成正比. 

![Minimum Spanning Tree](https://upload.wikimedia.org/wikipedia/commons/c/c9/Multiple_minimum_spanning_trees.svg)

此图显示图表中可能有多个最小生成树. 在该图中,图下面的两棵树是给定图的最小生成树的两种可能性. 

## 参考

-   [Minimum Spanning Tree on Wikipedia](https://en.wikipedia.org/wiki/Minimum_spanning_tree)
-   [Prim's Algorithm on Wikipedia](https://en.wikipedia.org/wiki/Prim%27s_algorithm)
-   [Prim's Algorithm on YouTube by Tushar Roy](https://www.youtube.com/watch?v=oP2-8ysT3QQ&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
-   [Prim's Algorithm on YouTube by Michael Sambol](https://www.youtube.com/watch?v=cplfcGZmX7I&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
- [维基百科](https://zh.wikipedia.org/wiki/%E6%9C%80%E5%B0%8F%E7%94%9F%E6%88%90%E6%A0%91)
