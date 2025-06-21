**介绍**

- String对象用于保存字符串，也就是一组字符序列
- 字符串常量对象是用双引号括起的字符序列，比如“你好”
- 字符串的字符使用Unicode字符编码，一个字符（不区分字母还是汉字）占两个字节
- String实现的接口
    - Serializable(String 可以串行化：可以在网络传输)
    - Compareable(String对象可以比较大小)

- String 是final类，不能继承
- String 有属性 private final char value[];用于存放字符串内容
- 一定要注意：value是一个final类型，不可以修改（不可以修改指针本身，可以修改指针所指向的值）

**创建String对象的两种方式**

- String s = "a"（直接赋值）
	- 先从常量池查看是否有a数据空间，如果有则直接指向a，如果没有则重新创建，然后指向，s最终指向的是常量池的空间地址
![Image](img1.png)
- String s2 = new String("a")
	- 先在堆中创建空间，里面维护了value属性，指向常量池的a空间，如果有，直接通过value指向，没有则重新创建然后指向。最后指向的是堆中的空间地址
![Image](img2.png)

**底层+的优化**

//此处为jdk8，jdk9之后优化方式不同，但逻辑上是差不多的

1. 先创建一个StringBuilder对象(sb)
2. sb.append(a)
3. sb.append(b)
4. return sb.toString

- 例题

	`String a = "hello" + "abc";`//底层会直接拼好，只有一个对象

	//如果是两个对象相加那么就是三个对象

**常用方法**

length()：返回字符串的长度
charAt(int index)：返回字符串指定索引位置的字符
substring(int beginIndex, int endIndex)：返回字符串指定索引范围的子串
toUpperCase()：将字符串转换为大写。
toLowerCase()：将字符串转换为小写
trim()：去除字符串两端的空格
replace(char oldChar, char newChar)：将字符串中所有的旧字符替换为新字符
split(String regex)：将字符串按指定的正则表达式分割成字符串数组
