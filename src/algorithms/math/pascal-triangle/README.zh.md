
# 杨辉三角形

在数学中,**杨辉三角形**是一个三角形的阵列[binomial coefficients](https://en.wikipedia.org/wiki/Binomial_coefficient). 


要想画杨辉三角，先把 "1" 方在顶点，然后连续在下面按三角形的模式放上数字。

每个数是它上面两个数的和。

![Pascal's Triangle](https://upload.wikimedia.org/wikipedia/commons/0/0d/PascalTriangleAnimated2.gif)

## 公式

> `n` 是 排 , `k`是 行内的第几个

进入`nth`排和`kth`列的杨辉三角形表示![Formula](https://wikimedia.org/api/rest_v1/media/math/render/svg/206415d3742167e319b2e52c2ca7563b799abad7). 例如,最上面一行中的唯一非零条目是![Formula example](https://wikimedia.org/api/rest_v1/media/math/render/svg/b7e35f86368d5978b46c07fd6dddca86bd6e635c). 

使用这种表示法,前一段的结构可写如下: 

![Formula](https://wikimedia.org/api/rest_v1/media/math/render/svg/203b128a098e18cbb8cf36d004bd7282b28461bf)

对于任何非负整数`n`和任何在`0`和`n`之间的整数`k`, 概括. 

![Binomial Coefficient](https://wikimedia.org/api/rest_v1/media/math/render/svg/a2457a7ef3c77831e34e06a1fe17a80b84a03181)

## 在O (n) 时间内计算三角形条目

我们知道

第`i`个-和第`lineNumber`行 组合为 `C(lineNumber, i)`二项式系数
并且所有行都以`1`值开头. 

想法是计算`C(lineNumber, i)`通过`C(lineNumber, i-1)`. 下面内容,只需要 `O(1)`时间: 

    C(lineNumber, i)   = lineNumber! / ((lineNumber - i)! * i!)
    C(lineNumber, i - 1) = lineNumber! / ((lineNumber - i + 1)! * (i - 1)!)

我们可以从以上两个表达式中得出以下表达式: 

    C(lineNumber, i) = C(lineNumber, i - 1) * (lineNumber - i + 1) / i

所以`C(lineNumber, i)`算出`C(lineNumber, i - 1)`是在`O(1)`时间. 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Pascal%27s_triangle)
-   [GeeksForGeeks](https://www.geeksforgeeks.org/pascal-triangle/)
-   [数学乐](https://www.shuxuele.com/pascals-triangle.html)
