
# 背包问题

背包问题 是 组合优化中 的问题: 给定一组项目,每个项目具有 重量 和值,确定要包括在集合中的每个项目的数量. 

使总重量 小于或等于 给定极限,总值尽可能大. 

它的名字来源于  受到固定尺寸背包约束的人 所面临的问题,并且必须 用最有价值的物品填充它. 

> 背包就那么大, 到底怎么选择装什么东西, 价值才最大.

一维 (约束) 背包问题的示例: 应选择 哪些方框以最大化金额,同时仍保持 总重量 低于或等于15公斤?

![knapsack problem](https://upload.wikimedia.org/wikipedia/commons/f/fd/Knapsack.svg)

## 定义

### 0/1背包问题

最常见的问题是**0/1背包问题**,这限制了每种物品`xi`的数量为 0 或者 1 份. 

给定n个项目编号为`1`到`n`作一组,每个都有一个重量`wi`和一个价值`vi`,剩下最大的重量容量`W`,

最大化价值![0/1 knapsack](https://wikimedia.org/api/rest_v1/media/math/render/svg/85620037d368d2136fb3361702df6a489416931b)

受制于![0/1 knapsack](https://wikimedia.org/api/rest_v1/media/math/render/svg/dd6e7c9bca4397980976ea6d19237500ce3b8176) 不能大于最大容量和![0/1 knapsack](https://wikimedia.org/api/rest_v1/media/math/render/svg/07dda71da2a630762c7b21b51ea54f86f422f951)每种选择只能小于或等于1

这里`xi`表示在背包里 第i个项目. 普遍来说,问题是 最大化背包物品价值的总和,且使得 重量的总和 小于或等于 背包的容量. 

### 有界背包问题 (BKP) 

该 **有界背包问题 (BKP)** 消除了每个项目只有一个的限制,但限制了`xi`的数量为 最大非负整数值`c`: 

最大化![bounded knapsack](https://wikimedia.org/api/rest_v1/media/math/render/svg/85620037d368d2136fb3361702df6a489416931b)

受制于![bounded knapsack](https://wikimedia.org/api/rest_v1/media/math/render/svg/dd6e7c9bca4397980976ea6d19237500ce3b8176)和![bounded knapsack](https://wikimedia.org/api/rest_v1/media/math/render/svg/6c8c5ac4f8247b3b8e01e89de76a1df0ea969821)

### 无界背包问题 (UKP) 

该 **无界背包问题 (UKP)** 每种物品的副本数量没有上限,除上述限制外,`xi`是一个非负整数. 

最大化![unbounded knapsack](https://wikimedia.org/api/rest_v1/media/math/render/svg/85620037d368d2136fb3361702df6a489416931b)

受制于![unbounded knapsack](https://wikimedia.org/api/rest_v1/media/math/render/svg/dd6e7c9bca4397980976ea6d19237500ce3b8176)和![unbounded knapsack](https://wikimedia.org/api/rest_v1/media/math/render/svg/90a99710f61d5dea19e49ae5b31164d2b56b07e3)

## 参考

-   [Wikipedia](https://en.wikipedia.org/wiki/Knapsack_problem)
-   [0/1 Knapsack Problem on YouTube](https://www.youtube.com/watch?v=8LusJS5-AGo&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
