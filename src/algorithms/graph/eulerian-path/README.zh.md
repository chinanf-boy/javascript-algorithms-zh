
# 欧拉回路与一笔画

在图论中,一个**欧拉路路径**是有限图中的轨迹,它只访问每个边一次. 同样,一个**欧拉回路**是一条欧拉轨迹,它在相同的顶点开始和结束. 

- 连通的无向图`G` 有欧拉路径的充要条件是：`G`中奇顶点（连接的边数量为奇数的顶点）的数目等于0或者2。

- 连通的无向图`G` 是欧拉环（存在欧拉回路）的充要条件是：`G`中每个顶点的度都是偶数。

![Eulerian Circuit](https://upload.wikimedia.org/wikipedia/commons/7/72/Labelled_Eulergraph.svg)

该图的每个顶点都具有偶数度. 因此,这是欧拉图. 按字母顺序排列边缘后,给出欧拉回路/环. 

对于欧拉轨迹的存在,零或两个顶点必须具有奇数度; 这意味着Königsberg图不是欧拉图. 如果没有奇数度的顶点,则所有欧拉轨迹都是回路. 如果恰好有两个奇数度的顶点,则所有欧拉航迹都从其中一个开始,到另一个结束. 具有欧拉轨迹但不是欧拉回路的图形称为半欧拉. 

![Königsberg graph](https://upload.wikimedia.org/wikipedia/commons/9/96/K%C3%B6nigsberg_graph.svg)

Königsberg 桥多图. 这个多图不是欧拉,因此,不存在解决方案. 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Eulerian_path)
-   [YouTube](https://www.youtube.com/watch?v=vvP4Fg4r-Ns&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
- [维基百科](https://zh.wikipedia.org/wiki/%E4%B8%80%E7%AC%94%E7%94%BB%E9%97%AE%E9%A2%98)
