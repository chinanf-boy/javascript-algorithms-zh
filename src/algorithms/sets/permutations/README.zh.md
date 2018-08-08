
# 排列

当 顺序 无关紧要时,它就是一个 **组合**. 

当 顺序 **是**个问题,它是个 **排列**. 

**"保险箱的组合是472"**. 我们关心顺序. `724`不会工作,也不会`247`. 它必须完全正确`4-7-2`. 

## 排列没有重复

排列,也称为"排列号"或"顺序",是 有序列表元素

下面是字符串的`ABC`排列. 

`ABC ACB BAC BCA CBA CAB`

或者例如 跑步比赛中的第三名: 你不可能是第一个和第二个. 

**组合数量**

    n * (n-1) * (n -2) * ... * 1 = n!

## 重复的排列

当允许重复时,我们有重复的排列. 例如下面的锁: 它可能是`333`. 

![Permutation Lock](https://www.mathsisfun.com/combinatorics/images/combination-lock.jpg)

**组合数量**

    n * n * n ... (r times) = n^r

## 备忘单

排列备忘单

![Permutations Cheat Sheet](https://cdn-images-1.medium.com/max/2000/1*JNK-n0Pt0Vbxk0lxVpgT5A.png)

组合备忘单

![Combinations Cheat Sheet](https://cdn-images-1.medium.com/max/2000/1*7cFRn8jW4g_91YgDAbmxRQ.png)

排列/组合算法 的想法. 

![Algorithms Idea](https://cdn-images-1.medium.com/max/2000/1*vLsSsZMnesCFPCYTYMbxrQ.png)

## 参考

-   [Math Is Fun](https://www.mathsisfun.com/combinatorics/combinations-permutations.html)
-   [Permutations/combinations cheat sheets](https://medium.com/@trekhleb/permutations-combinations-algorithms-cheat-sheet-68c14879aba5)
