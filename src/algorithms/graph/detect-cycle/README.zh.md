
# 检测 图中的环

在图论中,一个**图**是一个边和顶点的路径,其中一个顶点可以自环路. 有几种不同类型的环路,主要是**闭路**和**简单的环路**. 

## 定义

一个**闭路**由一个顶点的开始和结束 的顶点序列组成,在图中,序列中的每两个连续顶点彼此相邻. 在有向图中,

- 遍历每个边必须与其方向一致地: 边必须从两个连续顶点中较早的一个定向到后一个. 

- 起始顶点的选择并不重要: 因为从不同的起始顶点遍历相同的边序列会产生相同的闭路. 

一个**简单环路可能**

被定义为一个*不允许*重复顶点和边的闭路,除了重复起始和结束顶点,或者作为闭路的边集合. 

- 这两个定义在有向图中是等价的,其中简单环路也称为有向环路: 闭路中的顶点和边的环路序列完全由它使用的边集合确定. 

- 在无向图中,环路的边集合可以在两个方向中的任何一个方向上遍历,为每个无向环路提供两个可能的有向环路. 

电路可以是闭路,允许重复顶点而不是边;但是,它也可以是一个简单的环路,因此在使用时,建议使用明确的定义. 

## 例

![Cycles](https://upload.wikimedia.org/wikipedia/commons/e/e7/Graph_cycle.gif)

边颜色的图表说明**路径** `H-A-B` (绿色) ,或闭路**用重复的顶点走路** `B-D-E-F-D-C-B` (蓝色) 和**环路没有重复的边**的顶点`H-D-G-H` (红) 

### 在无向图中环路

![Undirected Cycle](https://www.geeksforgeeks.org/wp-content/uploads/cycleGraph.png)

### 在有向图中环路

![Directed Cycle](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/cycle.png)

## 参考

一般信息: 

-   [Wikipedia](https://en.wikipedia.org/wiki/Cycle_(graph_theory))
- [图形理论](http://www.stat.nuk.edu.tw/cbme/discrete/Graph/gch1.pdf)
无向图中的环路: 

-   [Detect Cycle in Undirected Graph on GeeksForGeeks](https://www.geeksforgeeks.org/detect-cycle-undirected-graph/)
-   [Detect Cycle in Undirected Graph Algorithm on YouTube](https://www.youtube.com/watch?v=n_t0a_8H8VY&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)

有向图中的环路: 

-   [Detect Cycle in Directed Graph on GeeksForGeeks](https://www.geeksforgeeks.org/detect-cycle-in-a-graph/)
-   [Detect Cycle in Directed Graph Algorithm on YouTube](https://www.youtube.com/watch?v=rKQaZuoUR4M&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
