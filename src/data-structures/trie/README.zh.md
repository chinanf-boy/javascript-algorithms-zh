# 字典树

是一种哈希树的变种。典型应用是用于统计，排序和保存大量的字符串（但不仅限于字符串），所以经常被搜索引擎系统用于文本词频统计。它的优点是：利用字符串的公共前缀来减少查询时间，最大限度地减少无谓的字符串比较，查询效率比哈希树高。

它有3个基本性质：
根节点不包含字符，除根节点外每一个节点都只包含一个字符； 从根节点到某一节点，路径上经过的字符连接起来，为该节点对应的字符串； 每个节点的所有子节点包含的字符都不相同。

> 我觉得 百度百科里面的 说明更 中国

有关 前缀树的空间优化 ，请参阅 compact
前缀树. 

![Trie](https://upload.wikimedia.org/wikipedia/commons/b/be/Trie_example.svg)

## References

- [Wikipedia](https://en.wikipedia.org/wiki/Trie)
- [YouTube](https://www.youtube.com/watch?v=zIjfhVPRZCg&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=7&t=0s)
