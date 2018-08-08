
# Knuth-Morris-Pratt算法

> 克努斯-莫里斯-普拉特算法

Knuth-Morris-Pratt字符串查找算法（简称为KMP算法）可在一个主文本字符串 `S`内查找一个词`W`的出现位置。此算法通过运用对 这个`W`词在不匹配时,本身就包含足够的信息来确定下一个匹配将在哪里开始的发现，从而避免重新检查先前匹配的字符。

## 复杂性

-   **时间:** `O(|W| + |T|)` (比较琐碎的`O(|W| * |T|)`快得多) 
-   **空间:** `O(|W|)`

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Knuth%E2%80%93Morris%E2%80%93Pratt_algorithm)
-   [YouTube](https://www.youtube.com/watch?v=GTJr8OvyEVQ&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
