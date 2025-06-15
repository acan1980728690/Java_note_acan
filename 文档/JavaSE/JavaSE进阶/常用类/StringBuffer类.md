**介绍**

- StringBuffer代表可变的字符序列，可以对字符串内容进行增删，很多方法和String一样，但是StringBuffer是可变长度的
- StringBuffer的直接父类是AbstractStringBuilder
- StringBuffer实现了Serializable，即StringBuffer的对象可以串行化
- 在父类中AbstractStringBuilder有属性char[] value,不是final 
- StringBuffer是一个final类，不能被继承
- 因为StringBuffer字符内容是存在char[] value,所以值是可以变化的，不用和String一样每次都更换地址（即不是每次都创建新对象）

**String vs StringBuffer**

- String保存的是字符串常量，里面的值不能更改，每次String类的更新实际上是更改地址，效率较低
- StringBuffer保存的是字符串变量，里面的值可以更改，每次StringBuffer的更新实际上可以更新内容，不用每次更新地址，效率较高

**构造器**

- ():创建一个大小为16的char[],用于存放字符内容
- (int capacity)：通过构造器指定char[]大小
- (String str):给一个String创建StringBuffer,char[]大小就是str.length() + 16

**常用方法**

- 增append
- 删delete
- 改replace
- 查IndexOf
- 插insert
- 获取长度length
