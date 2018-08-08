
# 位操作

#### 得到位

该方法将 相关位 移动到 第零位置. 然后我们执行`AND`具有位模式的操作`0001`. 这将清除原始数字中的所有位,但 相关位(这里就是那么`1`的位置) 除外. 如果相关位为1,则结果为`1`,否则结果是`0`. 

> 看到`getBit`函数更多细节. 

#### 设置位

这种方法改为`1`到一个`bitPosition`位,创建一个看起来像`00100`的值. 然后我们执行`OR`将特定位设置为`1`,但它不影响数字的其他位. 

> 看到`setBit`函数更多细节. 

#### 清除位

这种方法改为`1`到一个`bitPosition`位,创建一个看起来像`00100`的值. 反转这个掩码,以获得看起来像`11011`的数字. 然后`AND`操作正在应用于 数字和掩码. 这个操作 清除了这一位. 

> 看到`clearBit`函数更多细节. 

#### 更新位

此方法是"清除位"和"设置位"方法的组合. 

> 看到`updateBit`函数更多细节. 

#### 乘以二

该方法将 原始数字向左移一位. 因此,所有二进制数分量 (2的幂) 乘以2,因此数字本身乘以2. 

    移动之前
    Number: 0b0101 = 5
    Powers of two: 0 + 2^2 + 0 + 2^0 

    移动之后
    Number: 0b1010 = 10
    Powers of two: 2^3 + 0 + 2^1 + 0 

> 看到`multiplyByTwo`函数更多细节. 

#### 除以二

此方法将 原始数字向右移动一位. 因此,所有二进制数分量 (2的幂) 被除以2,因此数字本身被除以2而没有余数. 

    移动之前
    Number: 0b0101 = 5
    Powers of two: 0 + 2^2 + 0 + 2^0 

    移动之后
    Number: 0b0010 = 2
    Powers of two: 0 + 0 + 2^1 + 0 

> 看到`divideByTwo`函数更多细节. 

#### 切换标志

这种方法使 正数 为 负数和反向数. 为此,它使用"二进制 补充"方法,通过反转数字的所有位,并向其 添加1 来实现它. 

    1101 -3
    1110 -2
    1111 -1
    0000  0
    0001  1
    0010  2
    0011  3

> 看到`switchSign`函数更多细节. 

## 参考

-   [Bit Manipulation on YouTube](https://www.youtube.com/watch?v=NLKQEOgBAnw&t=0s&index=28&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
-   [Negative Numbers in binary on YouTube](https://www.youtube.com/watch?v=4qH4unVtJkE&t=0s&index=30&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
-   [Bit Hacks on stanford.edu](https://graphics.stanford.edu/~seander/bithacks.html)
