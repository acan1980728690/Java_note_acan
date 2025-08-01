# Spring FrameWork
---

## 系统架构图以及学习路线图

![Image](img1.png) 

![Image](img2.png)

## 基本的一些概念

**三层架构**
- Controller：控制层。接收前端发送的请求，对请求进行处理，并响应数据。
- Service：业务逻辑层。处理具体的业务逻辑。
- Dao(mapper)：数据访问层(Data Access Object)，也称为持久层。负责数据访问操作，包括数据的增、删、改、查。

**分层解耦**
- 内聚：软件中各个功能模块内部的功能联系。
- 耦合：衡量软件中各个层/模块之间的依赖、关联的程度。
- 软件设计原则：高内聚低耦合。
- 高内聚：指的是一个模块中各个元素之间的联系的紧密程度，如果各个元素(语句、程序段)之间的联系程度越高，则内聚性越高，即 "高内聚"。
- 低耦合：指的是软件中各个层、模块之间的依赖关联程序越低越好。



## 核心容器

### 核心概念

#### IOC/DI

##### 概念

IOC是为了低耦合高内聚

**控制反转**： Inversion Of Control，简称IOC。对象的创建控制权由程序自身转移到外部（容器），这种思想称为控制反转。
    - 对象的创建权由程序员主动创建转移到容器(由容器创建、管理对象)。这个容器称为：IOC容器或Spring容器。

**依赖注入**： Dependency Injection，简称DI。容器为应用程序提供运行时，所依赖的资源，称之为依赖注入。
    - 程序运行时需要某个资源，此时容器就为其提供这个资源。
    - 例：EmpController程序运行时需要EmpService对象，Spring容器就为其提供并注入EmpService对象。

**bean对象**：IOC容器中创建、管理的对象，称之为：bean对象。


##### 使用方式

###### 通过配置方式

1. 在spring配置文件内配置对应的类作为Spring管理的bean

```
<bean id="bookDao" class="全类名"></bean>
<bean id="bookService" class="全类名"></bean>
```

2. 初始化容器，通过容器获取bean
```

//加载配置文件得到上下文对象，也就是容器对象
AppliacationContext ctx = new ClassPathXmlApplicationContext("applicationContext.xml")
//获取资源
BookService bookservice = ctx.getBean("ID");
```

3. 配置文件内配置依赖关系（依赖对象需要提供对应的setter方法）

```
<bean id="bookService" class="全类名">
//name为属性名，ref为bean的名字
	<property name="bookDao" ref="bookDao"/>
</bean>
```
**bean的一些属性**

name设置别名，但是不建议这么做

scope设置作用域，值为prototype或者singleton（默认），prototype不是单例singleton是单例

#### IoC容器

#### Bean

### 容器基本操作

## 整合

整合数据层技术mybatis

## AOP

### 核心概念

### aop基础操作

### aop实用开发

## 事务

### 事务实用开发