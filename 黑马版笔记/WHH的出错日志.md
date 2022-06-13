# **WHH的出错日志**

# 1.判断数组是否为空

![判断数组是否为空](.\Bugimg\判断数组是否为空.png)

直接写数组名会获得数组的地址，比较地址是否为空即可

# 2.线程

当线程在睡眠时，也代表该线程正在占用

![线程](.\Bugimg\线程.png)

# 3.mybatis连接时，要设置字符集，不然容易出错

![字符集问题](.\Bugimg\字符集问题.png)

# 4.mapper大小写一致

![mapper大小写](.\Bugimg\mapper大小写.png)

# 5.jsp获取不了后端数据

我忘记在jsp中忘了加 <%page isELIgnored="false"%>,**isELIgnored的默认值为true,导致了在jsp页面会把${xxx}解析成正常的文本。**

![jsp文本解析](.\Bugimg\jsp文本解析.png)

