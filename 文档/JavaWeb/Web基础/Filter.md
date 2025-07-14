# Filter
---

## 概述

Filter,即过滤器,是JAVAEE技术规范之一,作用目标资源的请求进行过滤的一套技术规范,是Java web项目中 最为实用的技术之一

- Filter接口定义了过滤器的开发规范,所有的过滤器都要实现该接口
- Filter的工作位置是项目中所有目标资源之前,容器在创建HtpServletRequest和HttpservletResponse对象后,会先调用Filter的dofilter方法
- Filter的doFilter方法可以控制请求是否继续,如果放行,则请求继续,如果拒绝,则请求到此为止,由过滤器本身做出响应
- Filter不仅可以对请求做出过滤,也可以在目标资源做出响应前,对响应再次进行处理
- Filter是GOF中责任链模式的典型案例
- Filter的常用应用包括但不限于: 登录权限检查,解决网站乱码,过滤敏感字符,日志记录,性能分析.……


应用的场景

- 日志的记录
- 性能的分析
- 乱码的处理
- 事务的控制
- 登录的控制
- 跨域的处理
- .............

![Image](img1.png)

API

| API                                                                                         | 目标                                                         |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| default public void init(FilterConfig filterConfig)                                       | 初始化方法,由容器调用并传入初始配置信息 filterConfig 对象    |
| public void doFilter(ServletRequest request, ServletResponse response, FilterChain chain) | 过滤方法,核心方法,过滤请求,决定是否放行,响应之前的其他处理等 |
| default public void destroy()                                                             | 都在该方法中销毁方法,容器在回收过滤器对象之前调用的方法      |

## 过滤器使用


