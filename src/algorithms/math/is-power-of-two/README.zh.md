
# 判断2次方数

给定一个正整数,写一个函数来查找它是否为 2的幂. 

**简单解决方案**

在简单解决方案中,我们只是将 数字除以2,除非数字变为`1`,不然每次我们这样做,我们都会检查除法后的余数是为`0`. 否则数字不能是2的幂. 

**按位解决方案**

判断2次方数总是只有一位. 唯一的例外是带符号整数 (例如,值为-128的8位有符号整数如下所示: `10000000`) 

    1: 0001
    2: 0010
    4: 0100
    8: 1000

因此,在检查数字大于零之后,我们可以使用按位来测试一个,且只设置一个位. 

    number & (number - 1)

例如数字`8`操作将如下所示: 

      1000
    - 0001
      ----
      0111
      
      1000
    & 0111
      ----
      0000    

## 参考

-   [GeeksForGeeks](https://www.geeksforgeeks.org/program-to-find-whether-a-no-is-power-of-two/)
-   [Bitwise Solution on Stanford](http://www.graphics.stanford.edu/~seander/bithacks.html#DetermineIfPowerOf2)
-   [Binary number subtraction on YouTube](https://www.youtube.com/watch?v=S9LJknZTyos&t=0s&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=66)
