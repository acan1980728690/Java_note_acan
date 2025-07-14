**概念**

当程序中出现了某些“错误”，但该错误信息并没有在Throwable子类中描述处理，这个时候可以自己设计异常类，用于描述该错误信息

**自定义异常的步骤**

1. 定义类：自定义异常类名（程序员自己写）继承Exception或RuntimeException
2. 如果继承Exception，属于编译异常
3. 如果继承RuntimeException，属于运行异常

**throw和throws**

- throws是异常处理的一种方式，在方法声明处，后面跟的是异常类型
- throw是手动生成异常对象的关键字，在方法体中，后面跟的是异常对象
