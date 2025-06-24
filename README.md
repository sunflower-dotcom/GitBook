---
description: HashTable
---

# HashTable

1. hash table struct
   1. cells : hash 槽, 上面有节点和冲突计数
   2. ctl数组: 用于在控制cell, 一个cell控制一定数量(n\_cell\_per\_ctl, 2的n\_powen\_power次幂)的cells
2. hash insert
   1. 计算hash值,  (key ^ 165389371) % n\_cells, 为cell序号; 计算出序号后, 记录原本cell上登记的内容, 将新内容登记在cell上, 原本内容登记在新内容的hash\_node上
3. hash search
   1. 计算hash值, 在对应cell上一次查找符合需求的数据
4.  hash delete

    1. 计算hash值, 在对应cell上找到对应数据, 链表删除元素操作



本质上是个链表操作

其上存在的ctl之类信息, 特殊场景排序优化等使用
