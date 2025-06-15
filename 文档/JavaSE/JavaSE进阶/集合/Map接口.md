**Map接口实现类的特点（jdk8）**

- Map与Collection并列存在，用于保存具有映射关系的数据：Key-Value
- Map中的key河value可以是任何引用类型的数据，会封装到HashMap$Node对象中
- Map中的key不允许重复，原因和HashSet一样//当有相同的k时，就等价于替换
- Map中的value可以重复
- Map中的key可以为null,value也可以为null,注意key为null,只能有一个，value为null,可以多个
- 常用String类作为Map的key
- key和value之间存在单向一对一关系，即通过指定地key总能找到对应的value
- 一对k-v是放在一个Node中的，因为Node实现了Entry接口，有些书上也说一对k-v就是一个Entry

**常用方法**

- put添加
- remove根据键删除映射关系(用k把k-v都删掉)
- get根据键获取值
- size获取元素个数
- isEmpty判断个数是否为0
- clear：清除
- containKey查找键是否存在

**遍历方式**

containKey查找键是否存在
keySet：获取所有的键(Set)
entrySet获取所有关系k-v
values:获取所有的值（Collection）

