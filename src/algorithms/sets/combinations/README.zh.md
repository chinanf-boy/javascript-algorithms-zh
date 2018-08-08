
# 组合

当顺序 无关紧要时,它就是一个 **组合**. 

当顺序 **是**个问题,它就是一个 **排列**. 

**"我的水果沙拉是苹果,葡萄和香蕉的组合"** 我们不关心水果的顺序,它们也可以是"香蕉,葡萄和苹果"或"葡萄,苹果和香蕉",它是相同的水果沙拉. 

## 组合不重复

这就是彩票的工作方式. 这些数字是一次一个,如果我们有幸运数字 (无论什么顺序) 我们赢了!

没有重复: 比如彩票号码`(2,14,15,27,30,33)`

**组合数量**

![Formula](https://www.mathsisfun.com/combinatorics/images/combinations-no-repeat.png)

上面的`n`是可供选择的事物的数量,我们在其中选择`r`个,没有重复,顺序无关紧要. 

它通常被称为"n中选择r个" (例如"16中选3个") . 并且也称为二项式系数. 

## 重复的组合

允许重复: 例如口袋里的硬币`(5,5,5,10,10)`

或者 让我们说 有五种口味的冰淇淋: `banana`,`chocolate`,`lemon`,`strawberry`和`vanilla`. 

我们可以有三个勺子. 有多少种变化?

让我们使用字母表示口味: `{b, c, l, s, v}`. 示例选择包括: 

-   `{c, c, c}` (3勺巧克力) 
-   `{b, l, v}` (香蕉,柠檬和香草各一个) 
-   `{b, v, v}` (香蕉之一,香草之一) 

**组合数量**

![Formula](https://www.mathsisfun.com/combinatorics/images/combinations-repeat.gif)

`n`是可供选择的事物的数量,我们选择`r`个, 允许他们重复,顺序无所谓. 

## 备忘单

排列备忘单

![Permutations Cheat Sheet](https://cdn-images-1.medium.com/max/2000/1*JNK-n0Pt0Vbxk0lxVpgT5A.png)

组合备忘单

![Combinations Cheat Sheet](https://cdn-images-1.medium.com/max/2000/1*7cFRn8jW4g_91YgDAbmxRQ.png)

排列/组合算法的想法. 

![Algorithms Idea](https://cdn-images-1.medium.com/max/2000/1*vLsSsZMnesCFPCYTYMbxrQ.png)

## 参考

-   [Math Is Fun](https://www.mathsisfun.com/combinatorics/combinations-permutations.html)
-   [Permutations/combinations cheat sheets](https://medium.com/@trekhleb/permutations-combinations-algorithms-cheat-sheet-68c14879aba5)
