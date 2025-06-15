**介绍**

- HashSet实际上是HashMap
- 可以存放null,但是只能有一个null
- HashSet不保证元素使有序的，取决于hash后，再确定索引的结果
- 不能有重复元素/对象，在前面Set接口使用已经讲过

**底层机制**

HashSet底层是HashMap，HashMap底层是数组+链表+红黑树，具体看HashMap