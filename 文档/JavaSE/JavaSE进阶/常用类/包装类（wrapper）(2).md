**包装类的分类**

针对八种数据类型相应的引用类型——包装类

有了类的特点，就可以调用类中的方法

**包装类和基本数据的转换（装箱和拆箱）**

装箱：基本数据类型->包装类型，拆箱就是反过来

jdk5以前为手动装箱和拆箱，之后为自动装箱和拆箱

自动装箱底层调用的是valueOf方法，比如Interger.valueOf()

**一些常用方法**

- Interger.MIN_VALUE返回最小值
- Interger.MAX_VALUE返回最大值
- Character.isDigit()判断是不是数字
- Character.isLetter()判断是不是字母
- Character.isUpperCase()判断是不是大写
- Character.isLowerCase()判断是不是小写
- Character.isWhiteSpace()判断是不是空格
- Character.toUpperCase()转成大写
- Character.toLowerCase()转成小写


**面试题，底层**

Integer底层创建机制

-128 -127的时候是直接返回同一个对象的引用，类似Sstring，超出这个范围是新建一个对象