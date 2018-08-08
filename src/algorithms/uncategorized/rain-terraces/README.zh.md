
# 雨梯 (雨水收集) 问题

给定一组非负整数,表示困水的柱子,每个绿矩形条的量为`1`,计算下雨后它能捕获多少水. 

![Rain Terraces](https://www.geeksforgeeks.org/wp-content/uploads/watertrap.png)

> 注意: 绿色的是柱子, 不是容器, 被它们困在中间的额蓝色才是计算的水量

## 例子

**示例#1**

    Input: arr[] = [2, 0, 2]
    Output: 2
    Structure is like below:

    | |
    |_|

    我们可以在中间间隙捕获2个单位的水。

**例#2**

    Input: arr[] = [3, 0, 0, 2, 0, 4]
    Output: 10
    Structure is like below:

         |
    |    |
    |  | |
    |__|_| 

    We can trap "3*2 units" of water between 3 an 2,
    "1 unit" on top of bar 2 and "3 units" between 2 
    and 4. See below diagram also.

**例#3**

    Input: arr[] = [0, 1, 0, 2, 1, 0, 1, 3, 2, 1, 2, 1]
    Output: 6
    Structure is like below:

           | 
       |   || |
    _|_||_||||||

    Trap "1 unit" between first 1 and 2, "4 units" between
    first 2 and 3 and "1 unit" between second last 1 and last 2.

## 算法

如果左右两侧有较高的条形,则数组元素可以存储水. 我们可以通过找到 左侧和右侧的条形高度 来找到存储在每个元素中的水量. 想法是计算可以存储在阵列的每个元素中的水量. 例如,考虑数组`[3, 0, 0, 2, 0, 4]`,我们可以 在3和2 之间捕获"3 * 2单位"的水,在条2的顶部捕获"1个单位",在2和4之间捕获"3个单位". 往下看. 

### 方法1: 蛮力

**直观来看**

对于阵列中的每个元素,我们发现它在雨后可以捕获的最大水位,这等于两侧柱中最大高度 减去 最小值.

**步骤**

- 初始化`answer = 0`
- 从左到右迭代数组：
   - 初始化`max_left = 0`和`max_right = 0`
   - 从当前元素迭代到数组更新的开头：`max_left = max(max_left, height [j])`
   - 从当前元素迭代到数组更新结束：`max_right = max(max_right, height [j])`
   - 将`min(max_left, max_right) - height[i]`添加到`answer`

**复杂度分析**

时间复杂度: `O(n^2)`对于数组的每个元素,我们迭代左右部分. 

辅助空间复杂性: `O(1)`额外的空间

### 方法2: 动态规划 


**直观来看**

左右两侧，能够装水的体积只与较低的一侧相关，某种意义上，我们只需要从一侧进行遍历便可以求出最大装水量。但是，无论我们从哪一侧遍历，另一侧的不确定性都会增加求取装水体积的难度，需要细分求解，因此，我们采用两侧逼近的方法更为妥当，无论中间数据为何种形态，两侧逼近都能较为简洁的求解：

概念如图所示: 

![DP Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/Figures/42/trapping_rain_water.png)

**步骤**

-   找到从左端 到 索引的最大条形高度`i`, 放到`left_max`数组中. 
-   找到从右端 到 索引的最大条形高度`i`, 放到`right_max数组中`. 
-   迭代了`height`数组和更新`answer`: 
    -   加`min(max_left[i], max_right[i]) − height[i]`至`answer`. 

**复杂性分析**

时间复杂度: `O(n)`. 我们使用2次迭代`O(n)`将最大高度存储到一个点. 我们最后更新了`answer`使用存储的值在`O(n)`内. 

辅助空间复杂性: 额外的空间`O(n)`. 额外多了`left_max`和`right_max`数组空间 比 方法1. 

## 参考

-   [GeeksForGeeks](https://www.geeksforgeeks.org/trapping-rain-water/)
-   [LeetCode](https://leetcode.com/problems/trapping-rain-water/solution/)
