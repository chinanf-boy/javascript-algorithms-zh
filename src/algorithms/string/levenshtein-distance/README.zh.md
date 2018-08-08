
# Levenshtein 距离

Levenshtein距离 是用于测量两个序列之间差异的字符串度量. 一般来说,两个单词之间的 Levenshtein距离 是将 一个单词 更改为 另一个单词 所需的单字符编辑 (插入,删除或替换) 的最小数量. 

## 定义

数学上，我们定义两个字符串A和B间的 Levenshtein距离 为levA, B(a, b)，其中a、b分别为字符串A、B的长度， ![Levenshtein](https://wikimedia.org/api/rest_v1/media/math/render/svg/4cf357d8f2135035207088d2c7b890fb4b64e410)

![Levenshtein](https://wikimedia.org/api/rest_v1/media/math/render/svg/f0a48ecfc9852c042382fdc33c19e11a16948e85)

这个![Levenshtein](https://wikimedia.org/api/rest_v1/media/math/render/svg/52512ede08444b13838c570ba4a3fc71d54dbce9)是![Levenshtein](https://wikimedia.org/api/rest_v1/media/math/render/svg/231fda9ee578f0328c5ca28088d01928bb0aaaec)相等时为 0,否则为1的示性行数,还有就是![Levenshtein](https://wikimedia.org/api/rest_v1/media/math/render/svg/bdc0315678caad28648aafedb6ebafb16bd1655c)是`a`的前`i`个字符和`b`的前`j`个字符之间的距离。

注意在*min大括号*内的三种情况: 第一部分对应删除操作(从a到))、第二部分对应插入操作、第三部分对应替换操作,这取决于 a,b 对应的各个字符 是否相同. 

## 例

例如,`kitten`和`sitting`的Levenshtein距离是`3`,因为以下三个编辑将 一个更改为另一个,并且没有办法 以少于三个编辑执行此操作: 

1. **k**itten → **s**itten (用"s"代替"k") 
2. sitt**e**n → sitt**i**n (用"i"代替"e") 
3. sittin → sittin**g** (在末尾插入"g") . 

## 应用

在字符串近似匹配中，目标是从很多长的的文本中发现短文本的匹配，在这种情况下，较少差别的匹配是期望得到的。例如，短文本可以来自字典，这里，通常其中一个字符串是短的，另一个字符串是任意长的。莱文斯坦距离有着广泛的应用，例如，拼写检查、光学字符的校正系统、基于翻译内存库的自然语言翻译的辅助软件。

## 动态规划方法解释

我们来看一个简单的例子,找出字符串`ME`和`MY`之间的最小编辑距离. 直观地说,你已经知道这里的最小编辑距离是只有`1`个步骤. 它就是用`E`取代`Y`. 但是,让我们尝试以算法的形式将其形式化,以便能够执行更复杂的示例,如转换`Saturday`成`Sunday`. 

应用上面提到的数学公式`ME → MY`转换,我们需要知道`ME → M`,`M → MY`和`M → M`转变的最小编辑距离. 然后我们需要选择最小的一个,并添加*一个*操作去转换最后一个字母的操作`E → Y`. 所以最小编辑距离`ME → MY`基于三个先前可能的变换来计算变换. 

为了进一步解释,让我们绘制以下矩阵: 

![Levenshtein Matrix](https://cdn-images-1.medium.com/max/1600/1*2d46ug_PL5LfeqztckoYGw.jpeg)

- 格子`(0: 1)`包含红色数字1.这意味着我们需要1次操作
将`M`转换为空字符串。 它是删除`M`。 这就是为什么这个数字是红色的。

- 格子`(0: 2)`包含红色数字2.这意味着我们需要2次操作
将`ME`转换为空字符串。 它是删除`E`和'M`。

- 格子`(1: 0)`包含绿色数字1.这意味着我们需要1次操作
将空字符串转换为“M`。 它是通过插入`M`。 这就是为什么这个数字是绿色的。

- 格子`(2: 0)`包含绿色数字2.这意味着我们需要2个操作
将空字符串转换为“MY`。 它是通过插入“Y`和“M`。

- 格子`(1: 1)`包含数字0.这意味着它不需要任何费用
把`M`变成'M`。

- 格子`(1: 2)`包含红色数字1.这意味着我们需要1次操作
将“ME`转换为“M`。 它正在删除`E`。

- 等等...

对于像我们这样的小矩阵来说，它看起来很容易(它只有`3x3`)。 但在这里
可以找到可用于计算所有这些数字的基本概念
更大的矩阵(自己试试`9x7`一，`Saturday → Sunday`变换)。

根据公式，你只需要三个相邻的单元格`(i-1:j)`，`(i-1:j-1)`和`(i:j-1)`
计算当前单元格的编号`(i:j)`。 我们所要做的就是找到
那三个中最小的单元格然后添加`1`,
如果`i`行和`j`列中的字母不同的话。

您可以清楚地看到问题的递归性质。

![Levenshtein Matrix](https://cdn-images-1.medium.com/max/2000/1*JdHQ5TeKiDlE-iKK1s_2vw.jpeg)

让我们为这个问题绘制一个决策图. 

![Minimum Edit Distance Decision Graph](https://cdn-images-1.medium.com/max/1600/1*SGwYUpXH9H1xUeTvJk0e7Q.jpeg)

您可能会在图片上看到许多重叠的子问题
用红色。 此外，没有办法减少操作数量并使其成功,也就是
少于那三个相邻细胞的最小值。

您还可能会注意到计算矩阵中的每个单元格数字
是基于前一个。 因此制表技术（填写缓存）
自下而上的方向）正在这里应用。

进一步应用这个原则,我们可以解决更复杂的情况,如`Saturday → Sunday`转换. 

![Levenshtein distance](https://cdn-images-1.medium.com/max/1600/1*fPEHiImYLKxSTUhrGbYq3g.jpeg)

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Levenshtein_distance)
-   [YouTube](https://www.youtube.com/watch?v=We3YDTzNXEk&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
-   [ITNext](https://itnext.io/dynamic-programming-vs-divide-and-conquer-2fea680becbe)
