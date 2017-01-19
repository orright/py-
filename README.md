

实时读取nginx日志（json格式），存入mysql数据库，并实现定时删除mysql过期事件

知识点：

1.掌握json格式日志读取方式，读取出来的unicode格式需要通过str()转换为字符串格式

2.指针滑动到日志底部，实时读取最新产生的日志 seek(0, 2)

3.nginx访问日志的字段切分，非正则方式，效率要高，但不具备通用性

4.实例化mysql增删改查的类，进行sql语句拼接并执行，熟悉sql语句的写法，以及mysql建库建表建字段的方法

日志测试：

测试脚本：# numbers=`wc -l < 1.log`;for((i=1;i<=$numbers;i=i+1));do sed -n "$i"p 1.log >>2.log;sleep 5;done
