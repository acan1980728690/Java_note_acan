Collections是一个操作Set，List和Map等集合的工具类

Collections中提供了一系列静态的方法对集合元素进行排序，查询和修改等操作

排序操作

- reverse(List):反转List中元素的顺序
- shuffle:对LIst集合元素进行随机排序
- sort(List，Comparator):根据元素的自然顺序对指定LIst集合元素按升序排序
- swap(List,int,int)将指定list集合中的第i处元素和第j处元素进行交换

查找，替换

- Object max(Collection)根据元素的自然顺序，返回给定集合中的最大元素
- Object max(Collection Comparator)根据Comparator制定的顺序，返回给定集合中的最大元素
- Object min(Collection)
- Object min(Collectioin Comparator)
- int frequency(Collection Object)返回指定集合中指定元素的出现次数
- void copy(List dest,List src):将src中的内容赋值到dest中
- boolean replaceAll(List list,Object oldVal,Object newVal)使用新值替换List对象的所有旧值
