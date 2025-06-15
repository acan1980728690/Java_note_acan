**介绍**

- HashMao是以key-val的方式来存储数据
- key不能重复，value可以，允许使用null键和null值
- 如果添加相同的key，会覆盖之前原来的key-val，等同于修改
- 和HashSet一样不保存映射的顺序，因为底层是以hash 表的方式来存储的（jdk8的hashMap底层 数组+链表j+红黑树）
- HashMap没有实现同步，因此是线程不安全的

**底层**

数据结构是数组+链表，数组里的每一个元素都是一个链表，在java8中，如果一条链表的元素个数到达TREEIFY_THRESHOLD(默认8)，并且table的大小>=MIN_TREEIFY_CAPACITY(默认64)，就会进行树化（红黑树），否则依然采用数组扩容机制（在扩容过程中会改变原来链表的存放位置）

add添加底层

![Image](img1.png)

底层扩容机制

- 往里面加东西的时候，不管是加到数组或者链表，只要加入了一个新的结点，就算大小变大，就可能会触发扩容机制
- HashSet底层是HashMap,第一次添加时，table扩容到16，临界值(threshold)是16*加载因子(loadFactor)0.75 = 12
- 如果table数组使用到了临界值12，就会扩容到16*2 = 32,新的临界值就是32*0.75 =24，依次类推
- 在java8中，如果一条链表的元素个数到达TREEIFY_THRESHOLD(默认8)，并且table的大小>=MIN_TREEIFY_CAPACITY(默认64)，就会进行树化（红黑树），否则依然采用数组扩容机制（在扩容过程中会改变原来链表的存放位置）

k-v

- k-v最后是HashMap$Node node = newNode(hash,key,value,null)
- k-v为了方便程序员的遍历，还会创建EntrySet集合，该集合存放的元素类型Entry,而一个Entry对象就有k,v EntrySet<Entry<k,v>> 即transient Set<Map.Entry<K,V>> entrySet;
- EntrySet里存放的只是k-v的引用,并没有新建一个值存储
- entrySet中，定义的类型是Map.Entry,但是实际上存放的还是HashMap$Node,这时因为HashMap$Node implements Map.Entry<K,V>
- 当把HashMap$Node对象存放到entrySet就方便我们的遍历，因为Map.Entry提供了重要方法K getKey()和V getValue( );
![Image](img2.png)