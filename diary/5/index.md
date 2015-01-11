#Oracle日志
######2015年1月10日 16:59:53 
------
>1. 今天学到了什么
2. 遇到的问题
3. 怎么解决的
--------

####今天学到了什么
+ `java7`自动关闭连接
```java
Class.forname("jdbc");
try(Connection con = DriverManager.getConnection( "jdbc:mysql://zyl-me.xicp.net:10000/graduationsystem", "root", ""))
{
    ...
}catch(SQLException e)
{
    ...
}
```
+ 构造函数的`访问修饰符 `
```
 构造函数`访问修饰符`与`类`的`访问修饰符`相同
```
+ 获得32位 `uuid`
```
public static String getId()
    {
        UUID uuid = UUID.randomUUID();
        return uuid.toString();
    }  
```

####遇到的问题&怎么解决的
>+ __MYSQL Error Code: 1146. Table 'ask.ask_user' doesn't exist__ : 删除掉 drop index uq_email on ask_user;
>+ __MYSQL Error Code: 1215. Cannot add foreign key constraint__ : 外键是varchar(32),引用的主键是int,将int改回varchar(32)
>+ __JSTL 的添加 问题__ : 安装了MYECLIPSE 10, 添加了JSTL库
>+ __MYECLIPSE 10 内容助手不工作__ : 卸载掉了MyEclipse 10 安装了MyEclipse2015

