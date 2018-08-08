
# 哈密顿回路

**哈密顿图**（哈密尔顿图）（英语：Hamiltonian path，或Traceable path）是一个无向图，由天文学家哈密顿提出，由指定的起点前往指定的终点，途中经过所有其他节点且只经过一次。在图论中是指含有哈密顿回路的图，闭合的哈密顿路径称作哈密顿回路（Hamiltonian cycle），含有图中所有顶点的路径称作哈密顿路径。

![Hamiltonian cycle](https://upload.wikimedia.org/wikipedia/commons/6/6c/Hamiltonian_path_3d.svg)

通过十二面体的每个顶点的一个可能的哈密顿循环以红色显示 - 像所有柏拉图固体一样,十二面体是哈密顿. 

## 简单算法

生成所有可能的顶点集合并打印满足给定约束的集合. 将有`n!` (n阶乘) 集合. 

    当没有找到 哈密顿 环
    {
       寻找下一个顶点集合
       if ( 两个顶点相连, 并且从最开始顶点 到 最后顶点 是一条边 ).
       {
          print 集合;
          break;
       }
    }

## 回溯算法

创建一个空路径数组并添加 顶点`0` 给它. 从顶点开始添加其他顶点`1`. 在添加顶点之前,请检查它是否与先前添加的顶点相邻且尚未添加. 如果我们找到这样一个顶点,我们将顶点添加为解决方案的一部分. 如果我们找不到顶点,那么我们返回false. 

## 参考

-   [Hamiltonian path on Wikipedia](https://en.wikipedia.org/wiki/Hamiltonian_path)
-   [Hamiltonian path on YouTube](https://www.youtube.com/watch?v=dQr4wZCiJJ4&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
-   [Hamiltonian cycle on GeeksForGeeks](https://www.geeksforgeeks.org/backtracking-set-7-hamiltonian-cycle/)
- [百度百科](https://baike.baidu.com/item/%E5%93%88%E5%AF%86%E9%A1%BF%E5%9B%9E%E8%B7%AF)