**基本介绍**
- Properties类继承自HashTable类并且实现了Map接口，使用键值对的形式来保存数据
- 使用特点和HashTable类似
- 专门用于读写配置文件的集合类

**常见方法**

- load:加载配置文件的键值对到Properties对象
- list:将数据显示到指定设备
- getProperty(key):根据键获取值
- setProperty(key,Value):设置键值对到Properties对象
- store：将Properties中的键值对存储到配置文件，在idea中，保存信息到配置文件，如果含有中文，会存储为unicode吗
