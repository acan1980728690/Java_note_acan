**介绍**

- 存放的元素是键值对，即k-v
- hashtable的键和值都不能为null
- hashtable使用方法基本上和hashmap一样
- hashTable是线程安全的（synchronized），hashMap是线程不安全的

**底层**
底层有数组`Hashtable$Entry[] `初始化大小为11，临界值`threshold 8 = 11 * 0.75`

扩容：按照自己的扩容机制来进行,执行方法addEntry(hash,key,value,index)；

1. 添加K-V封装到Entry

2. 当if(count >= threshold)满足时，就进行扩容

3. 按照int newCapacity = (oldCapacity << 1) + 1的大小进行扩容（大小为原来x2 +1）

