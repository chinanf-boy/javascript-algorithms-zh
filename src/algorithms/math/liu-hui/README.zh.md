
# 刘辉的π算法

刘徽是中国数学史上最先创造了一个从数学上计算圆周率到任意精确度的迭代程序。他自己通过分割圆为192边形，计算出圆周率在·`.141024 与 3.142704`之间，取其近似，并以 `157/50` 表示。这个数值准确到三位数字，比前人的圆周率数值都准，但他自己次承认这个数值偏小。后来刘徽发明一种快捷算法，可以只用 96边形 得到和 1536边形 同等的精确度，从而得令他自己满意的 π = 3.1416。

## 圆的面积

刘辉说: 

将6边形一边的长度乘以圆半径，再乘3，得12边形的面积。将12边形的一边长乘半径，再乘6，得24边形面积。越割越细，多边形和圆面积的差越小。如此割了再割，最后终于和圆合为一体，毫无差别了

- 6边形的面积显然和圆面积相差很多。
- 内接正12边形面积 = 6边形面积+6个蓝色三角形面积，向圆面积趋近了一步。
- 正24边形面积=6边形面积+6个蓝色三角形面积+12个黄色三角形面积，更加接近圆面积了。

![Liu Hui](https://upload.wikimedia.org/wikipedia/commons/6/69/Cutcircle2.svg)

刘辉计算圆的面积的方法. 

下面是证明过程: 

关于多边形的面积，刘徽有如下公式：

2 N边形的面积= N边形的半周长×R = `L * N/2 *R`

其中 `L` 为  `N`边形的单边长，`R` 为圆半径。

此公式可用刘徽出入相补原理证明: 将内接2N边形，分割，然后重新排列成宽为 `L x N/2, 高为R`的长方形；

显然 2N边形的面积=长方形面积= `N/2 * L * R` = N边形的半周长 * R

![Liu Hui](https://upload.wikimedia.org/wikipedia/commons/9/95/Cutcircle.svg)

- 当 N -> `∞ `时
- N边形的半周长 -> 圆的半周长
- 2N边形面积 = N边形的半周长 * R => 圆面积
- 所以
- 圆的半周长 * R = 圆面积
- 因此
- 圆周 = 2* 圆面积/R
- 圆周率 = 圆周/直径 = 2* 圆面积/(R*2R)= 圆面积/R<sup>2</sup> = 2N边形的面积/R<sup>2</sup> (N -> `∞`)

圆内的面积等于半径乘以圆周的一半,或`A = r x C/2 = r x r x π`. 

## 迭代算法

刘辉从一个刻有六边形的开始. 让`M`是是`AB`边的一半,`r`是圆的半径. 

![Liu Hui](https://upload.wikimedia.org/wikipedia/commons/4/46/Liuhui_geyuanshu.svg)

可以看出, `m`会成为 12边形的 边长, 那么如何求出

因为`AOP`,`APC`是两个直角三角形. 刘辉用了[Gou Gu](https://en.wikipedia.org/wiki/Pythagorean_theorem) (毕达哥拉斯定理) 定理重复: 

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/dbfc192c78539c3901c7bad470302ededb76f813)

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/ccd12a402367c2d6614c88e75006d50bfc3a9929)

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/65d77869fc02c302d2d46d45f75ad7e79ae524fb)

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/a7a0d0d7f505a0f434e5dd80c2fef6d2b30d6100)

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/c31b9acf38f9d1a248d4023c3bf286bd03007f37)

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/0dee798efb0b1e3e64d6b3542106cb3ecaa4a383)

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/3ffeafe88d2983b364ad3442746063e3207fe842)

刘徽从半径1尺圆的内接正6边形开始，逐次分割为12边形，24边形，48边形，96边形。反复使用勾股定理求得各多边形的边长，又用刘氏多边形面积公式求多边形面积。

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Liu_Hui%27s_%CF%80_algorithm)
-   [维基百科][zh]

[zh]: https://zh.wikipedia.org/wiki/%E5%89%B2%E5%9C%86%E6%9C%AF_(%E5%88%98%E5%BE%BD)
