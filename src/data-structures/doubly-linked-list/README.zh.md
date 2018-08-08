# 双重链表

在计算机科学中, **双向链表**是一种链接数据结构
由一组称为节点的顺序链接记录组成.  每个节点包含
两个字段, 其中称为链接, 是对 节点序列中的 前一个和下一个节点的引用
.  而 开始和结束节点 的 上一个和下一个节点
链接 分别指向某种终结者, 通常是 标记
节点 或 null, 以方便遍历列表.  如果只有一个
标记 节点, 然后列表通过 标记节点 循环链接.  它可以
被概念化为 由 相同数据项 形成的两个单链表, 
但是在相反的顺序中. 

> 如果只有一个标记节点, 具有 开始节点与结束节点 的 引用, 可以让 闭合链表

![Doubly Linked List](https://upload.wikimedia.org/wikipedia/commons/5/5e/Doubly-linked-list.svg)

两个节点链接 允许 在任一方向上 遍历列表.  在添加
或者删除双向链表中的节点时 需要更改比 单链表 更多的链接. 
如果在单链表上进行相同的操作, 操作更简单
可能更有效（对于除第一个节点以外的节点）, 因为
在遍历期间, 不需要跟踪前一个节点或者无需
遍历列表以查找上一个节点, 以便可以修改其链接. 

## References

- [Wikipedia](https://en.wikipedia.org/wiki/Doubly_linked_list)
- [YouTube](https://www.youtube.com/watch?v=JdQeNxWCguQ&t=7s&index=72&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8)
