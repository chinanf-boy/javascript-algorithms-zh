
# Eratosthenes的筛子

Eratosthenes的Sieve 是一种用于查找 用来找出一定范围`n`内所有的素数。. 

它归功于古希腊数学家 Cyrene 的 Eratosthenes. 

## 怎么运行的

1.  创建一个`n + 1`大小的布尔数组 (代表`0`到`n`) 
2.  设位置`0`和`1`为`false`,其余的`true`
3.  从位置开始`p = 2` (第一个素数) 
4.  标记为`false`所有`p`的倍数 (即位置`2 * p`,`3 * p`,`4 * p`... 直到你到达阵列的末尾) 
5.  在数组中 找到大于`p`的第一个位置且是`true`. 如果没有这样的位置,请停止. 否则,让`p`等于这个新数字 (这是下一个素数) ,并从第4步重复

算法终止时,数组中剩余还是`true`都是`n`下面的所有素数. 

在步骤4中,该算法的改进 是开始标记的倍数 `p`从`p * p`而不是来自 `2 * p`. 之所以能起作用是因为,在那时,`p`的较小倍数早被标记上`false`了. 

## 例

![Sieve](https://upload.wikimedia.org/wikipedia/commons/b/b9/Sieve_of_Eratosthenes_animation.gif)

## 复杂性

该算法具有复杂性`O(n log(log n))`. 

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes)
