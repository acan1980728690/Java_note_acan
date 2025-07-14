**语法**
```
try {
    //可能出现异常的代码
} catch (Exception e) {
    //捕获到异常，执行此块代码
    //没有异常，则不执行此块代码
    e.printStackTrace();
} finally {
    //不管try块是否有异常，finally块都会执行
}
```

**细节**

- 如果try代码块有可能有多个异常，可以使用多个catch分别捕获不同的异常，响应处理，注意子类异常要写在前面
- 可以进行try-finally，本质没有捕获异常程序会崩溃，但是不管会不会崩溃都会执行finally
