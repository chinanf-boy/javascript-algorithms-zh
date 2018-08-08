
# 汉诺塔

汉诺塔（又称河内塔）问题是源于印度一个古老传说的益智玩具。大梵天创造世界的时候做了三根金刚石柱子，在一根柱子上从下往上按照大小顺序摞着64片黄金圆盘。大梵天命令婆罗门把圆盘从下面开始按大小顺序重新摆放在另一根柱子上。并且规定，在小圆盘上不能放大圆盘，在三根柱子之间一次只能移动一个圆盘。

也就是这个难题的目的是将 整个堆栈 移动到 另一个杆,遵循以下简单规则: 

-   一次只能移动一个磁盘. 
-   每次移动包括从其中一个堆叠中取出上部磁盘并将其放置在另一个堆叠的顶部或空杆上. 
-   没有磁盘可以放在较小的磁盘上. 

![Hanoi Tower](https://upload.wikimedia.org/wikipedia/commons/8/8d/Iterative_algorithm_solving_a_6_disks_Tower_of_Hanoi.gif)

解决6磁盘问题的迭代算法的动画

同`3`磁盘,拼图可以解决`7`移动. 解决河内之塔拼图所需的最少次数是`2^n − 1`,哪里`n`是磁盘的数量. 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Tower_of_Hanoi)
-   [HackerEarth](https://www.hackerearth.com/blog/algorithms/tower-hanoi-recursion-game-algorithm-explained/)
- [百度百科](https://baike.baidu.com/item/%E6%B1%89%E8%AF%BA%E5%A1%94)