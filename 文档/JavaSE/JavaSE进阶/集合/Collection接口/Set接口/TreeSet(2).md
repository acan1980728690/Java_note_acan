当我们使用无参构造器创建TreeSet时，仍然是无序的

有参构造器：传入一个比较器，指定排序规则，构造器把传入的比较器对象，赋给了一个TreeSet底层的TreeMap的属性`this.comparator`


