
# 正则表达式匹配

给定一个输入字符串`s`和一个模式`p`,实现正则表达式匹配的支持`.`和`*`. 

-   `.`匹配任何单个字符. 
-   `*`匹配前面元素的零个或多个. 

匹配应涵盖**整个**输入字符串 (不是部分) . 

**注意**

-   `s`可能是空的,只包含小写字母`a-z`. 
-   `p`可能是空的,只包含小写字母`a-z`和`.`要么`*`. 

## 例子

**示例#1**

输入: 

    s = 'aa'
    p = 'a'

输出: `false`

说明: `a`与`aa`整个字符串不匹配. 

**例#2**

输入: 

    s = 'aa'
    p = 'a*'

输出: `true`

说明: `*`表示前面元素中的零个或多个`a`. 因此,通过重复`a`一旦它变成了`aa`. 

**例#3**

输入: 

    s = 'ab'
    p = '.*'

输出: `true`

说明: `.*`意思是"零或更多(`*`) 的 任何角色 (`.`)". 

**例#4**

输入: 

    s = 'aab'
    p = 'c*a*b'

输出: `true`

说明: `c`可以重复0次,`a`可以重复1次. 因此它匹配`aab`. 

## 参考

-   [YouTube](https://www.youtube.com/watch?v=l3hda49XcDE&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=71&t=0s)
-   [LeetCode](https://leetcode.com/problems/regular-expression-matching/description/)
