﻿**介绍**
- 允许所有的元素，包括null，ArrayList可以加入null，而且可以多个
- ArrayList是由数组来实现数据存储的
- ArrayList基本等同于Vector,除了ArrayList是线程不安全的(没有synchronized)（执行效率高），在多线程情况下，不建议使用ArrayList

**底层**

- ArrayList中维护了一个Object类型的数组elementData(transient Object[] elementData;)
- 当创建ArrayList对象时，如果使用的是无参构造器，则初始elementData容量为0，第一次添加，则扩容elementData为10，如需要再次扩容，则扩容elementData为1.5倍
- 如果使用的是指定大小的构造器，则初始elementData容量为指定大小，如果需要扩容，则直接扩容elementData为1.5倍

