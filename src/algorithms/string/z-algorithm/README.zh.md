
# Z算法

Z算法找到"单词"的出现`W`在主"文本字符串"中`T`在线性时间`O(|W| + |T|)`. 

给定一个字符串`S`长度`n`,算法产生一个数组,`Z`哪里`Z[i]`表示从最长的子串开始`S[i]`这也是一个前缀`S`. 查找`Z`对于通过连接单词获得的字符串,`W`有一个nonce字符,比方说`$`然后是文字,`T`,有助于模式匹配,如果有一些索引`i`这样的`Z[i]`等于模式长度,那么模式必须存在于该点. 

虽然`Z`数组可以用两个嵌套循环来计算`O(|W| * |T|)`时间,以下策略显示如何在线性时间内获得它,基于我们迭代字符串中的字母 (index) 的想法`i`从`1`至`n - 1`) ,我们保持间隔`[L, R]`这是最大的间隔`R`这样的`1 ≤ L ≤ i ≤ R`和`S[L...R]`是一个前缀也是一个子字符串 (如果不存在这样的间隔,请让它`L = R =  - 1`) . 对于`i = 1`,我们可以简单地计算`L`和`R`通过比较`S[0...]`至`S[1...]`. 

**Z数组的示例**

    Index            0   1   2   3   4   5   6   7   8   9  10  11 
    Text             a   a   b   c   a   a   b   x   a   a   a   z
    Z values         X   1   0   0   3   1   0   0   2   2   1   0 

其他例子

    str =  a a a a a a
    Z[] =  x 5 4 3 2 1

    str =  a a b a a c d
    Z[] =  x 1 0 2 1 0 0

    str =  a b a b a b a b
    Z[] =  x 0 6 0 4 0 2 0

**Z盒的例子**

![z-box](https://ivanyu.me/wp-content/uploads/2014/09/zalg1.png)

## 复杂性

-   **时间: ** `O(|W| + |T|)`
-   **空间: ** `O(|W|)`

## 参考

-   [GeeksForGeeks](https://www.geeksforgeeks.org/z-algorithm-linear-time-pattern-searching-algorithm/)
-   [YouTube](https://www.youtube.com/watch?v=CpZh4eF8QBw&t=0s&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=70)
-   [Z Algorithm by Ivan Yurchenko](https://ivanyu.me/blog/2013/10/15/z-algorithm/)
