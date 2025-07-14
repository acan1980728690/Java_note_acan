**构造器**

- new FileOutputStream(filePath)用这种方法创建会清空原内容
- new FileOutputStream(filePath,true)不清空内容，而是在原内容上追加


**常用方法**

- close()关闭流
- write(int b)将制定的字节写入此文件输出流
- write(byte[] b, int off,int len)将从off开始len个字节写入此文件输出流//可以用str.getBytes()来把字符串变成字节数组
- write(byte[] b)
