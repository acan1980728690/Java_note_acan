**分类**

分为有序和无序，有序是List接口，无序是Set接口的

**Collection接口实现类**

- 概念
	- Collection接口实现类可以存放多个元素，每个元素可以是Object
	- 有些Collection接口实现类，可以存放重复的元素，有些不可以
	- 有些Collection接口实现类,有些是有序的（List），有些不是有序的（Set）
	- Collection接口没有直接的实现子类，是通过它的子接口Set和List来实现的

- 常用方法
	- add：添加单个元素
	- remove：查找指定元素
	- contains：查找元素是否存在
	- size：获取元素个数
	- isEmpty：判断是否为空
	- clear：清空
	- addAll：添加多个元素
	- containsAll：查找多个元素是否都存在
	- removeAll:删除多个元素

**通用遍历方式**
1. 使用Iterator（迭代器）
2. for增强循环
