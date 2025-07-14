**介绍**
- LinkedHashSet是HashSet的子类
- LinkedHashSet底层是一个LinkedHashMap,底层维护了一个数组+双向链表
- LinkedHashSet根据元素的hashCode值来决定元素的存储位置，同时使用链表维护元素的次序，这使得元素看起来是以插入顺序保存的（用遍历的方式是有次序的，即加入顺序和取出元素的顺序一致）
- LinkedHashSet不允许添加重复元素

**底层机制**

1. linkedHashSet加入书序和取出元素/数据的顺序一致
2. LinkedHashSet 底层维护的是一个LinkedHashMap（是HashMap的子类）
3. LinkedHashSet 底层结构是数组table+双向链表
4. 第一次添加时，直接将数组table扩容到16，存放的结点类型是LInkedHashMap$Entry
5. 数组是 HashMao$Node[] 存放的元素/数据是LinkedHashMap￥Entry类型

![Image](img1.png)![Image](img2.png)![Image](img3.png)