#  1.数据库相关概念

![数据库相关概念](.\MySQLimg\数据库相关概念.png)

# 2.关系型数据库

![关系型数据库](.\MySQLimg\关系型数据库.png)

# 3.MySQL存储模式

![MySQL存储模式](.\MySQLimg\MySQL存储模式.png)

# 4.SQL简介

![SQL简介](.\MySQLimg\SQL简介.png)

# 5.SQL的通用语法

![SQL通用语法](.\MySQLimg\SQL通用语法.png)

```
-- 这是注释

#这是注释（mysql独有）

/*这是注释*/
```

# 6.SQL的分类

![SQL的分类](.\MySQLimg\SQL的分类.png)

![SQL的分类2](.\MySQLimg\SQL的分类2.png)

## 1.DDL

### 1.DDL操作数据库

#### 1.查询

查询数据库

show databases

#### 2.创建

创建数据库

当创建的数据库已经存在，那么会报错，此时建议加上判断语句 if not exists 数据库名

```
create database db //创建数据库

create database db if not exists db;
```



#### 3.删除

删除数据库

当删除的数据库不存在，那么会报错，此时建议加上判断语句 if exists 数据库名

```
drop database db //删除数据库

create database if exists db;
```

####  4.使用数据库

查看当前数据库

```
select database();
```

使用数据库

```
use 数据库名称;
```

#### 5.数据库小结

![DDL小结](.\MySQLimg\DDL小结.png)

### 2.DDL操作表

#### 1.查询(Retrieve)

##### 1.查询当前表下的名称

```
show tables;
```

##### 2.查询表结构

```
desc 表名称;
```

#### 2.创建(Create)

```
create table 表名(
	字段名1 数据类型1,
	字段名2 数据类型2,
	字段名3 数据类型3,
	...
	字段名n 数据类型n
);
```

**最后一行末尾，不能添加逗号（，）**

#### 3.修改(Update)

##### 1.修改表

alter table 表名 rename to 新的表名;

##### 2.添加一列

alter table 表名 add 列名 数据类型;

##### 3.修改表的数据类型

alter table 表名 modify 列名 新的数据类型;

##### 4.修改列名和数据类型

alter table 表名 change 列名 新列名 新数据类型;

##### 5.删除列

alter table 表名 drop 列名;

#### 4.删除(Delete)

drop table 表名;

drop table 表名 if exists 表名;

## 2.DML

### 1.添加（insert）

#### 1.给指定列添加数据

insert into 表名(列名1,列名2....) values(值1,值2..);

#### 2.给全部列添加数据

insert into 表名 values (值1,值2...);

#### 3.批量添加数据

insert into 表名(列名1,列名2..)  values (值1,值2...),(值1,值2...),(值1,值2...)...;

insert into 表名 values (值1,值2...),(值1,值2...),(值1,值2...)...;

### 2.修改（update）

update 表名 set 列名1 = 值 [where 条件];

**如果不添加条件，则将所有数据都修改**

### 3.删除（delete）

#### 1.删除数据

delete form 表名 [where 条件]; 

**如果不添加条件，则将所有数据都删除**

## 3.DQL

**条件查询（where）**

**分组查询（group by）**

**排序查询（order by）**

**分页查询（limit）**

### 1.基础查询

#### 1.查询多个字段

```
select 字段列表 from 表名;
select * from 表名; //查询所有数据
```

#### 2.去除重复记录

```
select distinct 字段列表 from 表名;
```

#### 3.起别名

```
as: //as可以省略
```

### 2.条件查询（where）

```
在..之间
列名 betweent ... and ...
===>
... and ...

不等号
!= ===> <>

关系运算符
&& ==> and
|| ==> or


包含关系
条件1 or 条件2 or 条件3
==>
列名 in(值1,值2..)

null值比较不能使用= != 
需要使用is | is not
```

![条件查询](.\MySQLimg\条件查询.png)

### 3.排序查询（order by）

#### 1.排序查询的语法

```
select 字段列表 from 表名 order by 排序字段1 [排序方式],排序字段2 [排序方式],...;
```

ASC :升序（默认值）

DESC:降序

注意：如果有多个排序条件，**当前边的条件值一样**，才会根据**第二条件进行排序**。

### 4.分组查询（group by）

#### 1.聚合函数

![聚合函数](.\MySQLimg\聚合函数.png)

```
count(参数):
*：统计所有信息，如果一行中，有一个数据不为空，则会统计
列名：统计所有不为空的信息
```

#### 2.分组查询

```
select 字段列表 from 表名 [where 分组查询限定条件] group by 分组字段名 [having 分组后条件过滤];
```

![分组查询](.\MySQLimg\分组查询.png)

### 5.分页查询（limit）

![分页查询](.\MySQLimg\分页查询.png)

# 7.MySQL数据类型

![MySQL数据类型](.\MySQLimg\MySQL数据类型.png)

**timestamp最大值只能到2038年，不推荐使用**

```
double(总长度,小数点后保留的位数 )

如果我们要存入1-100,小数点保留2位，那么我们就应该这么写(整数部分+小数部分 = 总长度)

score double(5,2)
```

```
如果存入 "力汗阿"
name char(10) 存储字符10 存储性能高 浪费空间

name varchar(10) 根据输入字符自动改变存储模式 存储3个字符 存储性能低 节约空间
```

# 8.约束

## 1.约束的概念

![约束的概念](.\MySQLimg\约束的概念.png)

​	

```
aotu_increment //自动增长
```

### 外键约束

![外键约束](.\MySQLimg\外键约束.png)

### 1.创建表时添加外键

```
constraint 外键名称 foreign key 从表 references 主表
```

添加数据时，要先添加主表的数据

### 2.建完表后添加外键

```
alter table 从表 add constraint 外键名称 foreign key(从表.列名) references 主表(列名);
```

### 3.删除外键

```
alter tbale 表名 drop foreign key 外键名称;
```

# 9.数据库设计

## 表关系

### 1一对多

![一对多](.\MySQLimg\一对多.png)

### 2.多对多

![多对多](.\MySQLimg\多对多.png)

### 3.一对一

![一对一](.\MySQLimg\一对一.png)

# 10.多表查询

![多表查询](.\MySQLimg\多表查询.png)

## 1.内连接

![内连接](.\MySQLimg\内连接.png)

显示内连接的inner可以省略

## 2.外连接

![外连接](.\MySQLimg\外连接.png)

outer可以省略

## 3.子查询

在查询中的嵌套查询称为子查询

![子查询](.\MySQLimg\子查询.png)

# 11.事务

![事务](.\MySQLimg\事务.png)

![事务四大特征](.\MySQLimg\事务四大特征.png)

![自动提交事务](.\MySQLimg\自动提交事务.png)

# 12.JDBC

![JDBC简介](.\MySQLimg\JDBC简介.png)

![连接数据库的步骤](.\MySQLimg\连接数据库的步骤.png)

## 1.JDBC的API

### 1.DriverManager

作用：

#### 1.注册驱动

![DriverManager](.\MySQLimg\DriverManager.png)

#### 2.获取数据库连接

![DriverManager获取连接](.\MySQLimg\DriverManager获取连接.png)

###  2.Connection

作用：

#### 1.执行SQL的对象

![Connection](.\MySQLimg\Connection获取执行对象.png)

#### 2.Connection事务管理

![Connection事务管理](.\MySQLimg\Connection事务管理.png)

```java
try {
    //开启事务
    conn.setAutoCommit(false);
    stat.executeUpdate(sql);
    System.out.println("测试1执行成功");

    stat.executeUpdate(sql);
    System.out.println("测试2执行成功");
    //代码没有错误，提交
    conn.commit();
} catch (Exception e) {
    //回滚
    conn.rollback();
    e.printStackTrace();
}
```

## 3.Statement

执行SQL语句

![Statement](.\MySQLimg\Statement.png)

## 4.ResultSet

![ResultSet](.\MySQLimg\ResultSet.png)

![ResultSet使用方法](.\MySQLimg\ResultSet使用方法.png)

```java
@Test
public void testResultSet() throws  Exception {
   //1. 注册驱动
   //Class.forName("com.mysql.jdbc.Driver");
   //2. 获取连接：如果连接的是本机mysql并且端口是默认的 3306 可以简化书写
   String url = "jdbc:mysql:///db1?useSSL=false";
   String username = "root";
   String password = "1234";
   Connection conn = DriverManager.getConnection(url, username, password);

   //3. 定义sql
    String sql = "select * from account";

    //4. 获取statement对象
    Statement stmt = conn.createStatement();

    //5. 执行sql
    ResultSet rs = stmt.executeQuery(sql);

    //6. 处理结果， 遍历rs中的所有数据
   /* // 6.1 光标向下移动一行，并且判断当前行是否有数据
    while (rs.next()){
        //6.2 获取数据  getXxx()
        int id = rs.getInt(1);
        String name = rs.getString(2);
        double money = rs.getDouble(3);

        System.out.println(id);
        System.out.println(name);
        System.out.println(money);

        System.out.println("--------------");

    }*/

    // 6.1 光标向下移动一行，并且判断当前行是否有数据
    while (rs.next()){
        //6.2 获取数据  getXxx()
        int id = rs.getInt("id");
        String name = rs.getString("name");
        double money = rs.getDouble("money");

        System.out.println(id);
        System.out.println(name);
        System.out.println(money);

        System.out.println("--------------");

    }


    //7. 释放资源
    rs.close();
    stmt.close();
    conn.close();
}




/**
 * 查询account账户表数据，封装为Account对象中，并且存储到ArrayList集合中
 * 1. 定义实体类Account
 * 2. 查询数据，封装到Account对象中
 * 3. 将Account对象存入ArrayList集合中
 *
 *
 * @throws Exception
 */
@Test
public void testResultSet2() throws  Exception {
    //1. 注册驱动
    //Class.forName("com.mysql.jdbc.Driver");
    //2. 获取连接：如果连接的是本机mysql并且端口是默认的 3306 可以简化书写
    String url = "jdbc:mysql:///db1?useSSL=false";
    String username = "root";
    String password = "1234";
    Connection conn = DriverManager.getConnection(url, username, password);

    //3. 定义sql
    String sql = "select * from account";

    //4. 获取statement对象
    Statement stmt = conn.createStatement();

    //5. 执行sql
    ResultSet rs = stmt.executeQuery(sql);

    // 创建集合
    List<Account> list = new ArrayList<>();

    // 6.1 光标向下移动一行，并且判断当前行是否有数据
    while (rs.next()){
        Account account = new Account();

        //6.2 获取数据  getXxx()
        int id = rs.getInt("id");
        String name = rs.getString("name");
        double money = rs.getDouble("money");

        //赋值
        account.setId(id);
        account.setName(name);
        account.setMoney(money);

        // 存入集合
        list.add(account);
    }

    System.out.println(list);

    //7. 释放资源
    rs.close();
    stmt.close();
    conn.close();
}
```

## 5.PreparedStatement

![PreparedStatement](.\MySQLimg\PreparedStatement.png)

![PreparedStatement作用](.\MySQLimg\PreparedStatement作用.png)

![PreparedStatement使用方法](.\MySQLimg\PreparedStatement使用方法.png)

# 13.数据库连接池

![数据库连接池](.\MySQLimg\数据库连接池.png)

![数据库连接池实现](.\MySQLimg\数据库连接池实现.png)

![Driud使用步骤](.\MySQLimg\Driud使用步骤.png)

# 14.Maven

![Maven](.\MySQLimg\Maven.png)

## 1.简介

![Maven简介](.\MySQLimg\Maven简介.png)

![Maven仓库](.\MySQLimg\Maven仓库.png)

## 2.Maven安装配置

![Maven安装配置](.\MySQLimg\Maven安装配置.png)

## 3.Maven的常用命令

![Maven常用命令](.\MySQLimg\Maven常用命令.png)

```
<mirror>
<id>alimaven-new</id>
<mirrorOf>central</mirrorOf>
<name>aliyun maven</name>
<url>https://maven.aliyun.com/repository/central/</url>
</mirror>
```



## 4.Maven的生命周期

![Maven的生命周期](.\MySQLimg\Maven的生命周期.png)

![Maven default构建生命周期](.\MySQLimg\Maven default构建生命周期.png)

## 5.在IDEA配置Maven

![IDEA配置Maven](.\MySQLimg\IDEA配置Maven.png)

### 1.Maven坐标

![Maven坐标](.\MySQLimg\Maven坐标.png)

### 2.IDEA创建Maven项目

![IDEA创建Maven项目](.\MySQLimg\IDEA创建Maven项目.png)

### 3.IDEA导入Maven项目

![IDEA导入Maven项目](.\MySQLimg\IDEA导入Maven项目.png)

## 6.依赖管理

### 1.导入

maven包下载

https://mvnrepository.com/

![Maven配置jar包](.\MySQLimg\Maven配置jar包.png)

### 2.依赖范围

![依赖范围](.\MySQLimg\依赖范围.png)

# 15.MyBatis

![MyBatis简化](.\MySQLimg\MyBatis简化.png)

## 1.MyBatis快速入门

查询表中所有数据

![查询表中所有数据](.\MySQLimg\查询表中所有数据.png)

### 1.创建一个Maven项目

### 2.MyBatis导入Maven项目中 

![MyBatis导入Maven项目中](.\MySQLimg\MyBatis导入Maven项目中.png)

```
<!--导入MyBatis-->
<dependency>
    <groupId>org.mybatis</groupId>
    <artifactId>mybatis</artifactId>
    <version>3.5.5</version>
</dependency>
<!--导入mysql-->
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>5.1.32</version>
</dependency>
```

### 3.创建一个xml配置文件

![创建一个xml配置文件](.\MySQLimg\创建一个xml配置文件.png)

![第二步](.\MySQLimg\第二步.png)

```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE configuration
  PUBLIC "-//mybatis.org//DTD Config 3.0//EN"
  "http://mybatis.org/dtd/mybatis-3-config.dtd">
<configuration>
  <environments default="development">
    <environment id="development">
      <transactionManager type="JDBC"/>
      <dataSource type="POOLED">
        <property name="driver" value="${driver}"/>
        <property name="url" value="${url}"/>
        <property name="username" value="${username}"/>
        <property name="password" value="${password}"/>
      </dataSource>
    </environment>
  </environments>
  <mappers>
    <mapper resource="org/mybatis/example/BlogMapper.xml"/>
  </mappers>
</configuration>
```

将代码复制到配置文件中去

![配置第二步](.\MySQLimg\配置第二步.png)

### 4.配置第三步

![配置第三步](.\MySQLimg\配置第三步.png)

![配置第三步2](.\MySQLimg\配置第三步2.png)

```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE mapper
        PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<!--
    namespace:命名空间
-->
<mapper namespace="test">
    <select id="selectALL" resultType="com.whh.pojo.User">
        select * from tb_user;
    </select>
</mapper>
```

### 5.配置第四步

![配置第四步](.\MySQLimg\配置第四步2.png)

```
public class MyBatisDemo {
    public static void main(String[] args) throws Exception {
        //1.加载mybatis的核心配置文件，获取SqlSeesionFactory
        String resource = "mybatis-config.xml";
        InputStream inputStream = Resources.getResourceAsStream(resource);
        SqlSessionFactory sqlSessionFactory = new SqlSessionFactoryBuilder().build(inputStream);
        //2.获取SqlSession对象,用它来执行sql
        SqlSession sqlSession = sqlSessionFactory.openSession();
        //3.执行sql
        List<Object> selectList = sqlSession.selectList("test.selectALL");
        System.out.println(selectList);
        //4.释放资源
        sqlSession.close();
    }
}
```

### 6.IDEA配置MySQL

![IDEA配置MySQL](.\MySQLimg\IDEA配置MySQL.png)

## 2.Mapper代理开发

### 1.配置文件

![Mapper配置文件步骤](.\MySQLimg\Mapper配置文件步骤.png)

![Mapper配置文件](.\MySQLimg\Mapper配置文件.png)

![Mapper配置文件结果](.\MySQLimg\Mapper配置文件结果.png)

![Mapper配置文件修改](.\MySQLimg\Mapper配置文件修改.png)

```java
public class MyBatisDemo {
    public static void main(String[] args) throws Exception {
        //1.加载mybatis的核心配置文件，获取SqlSeesionFactory
        String resource = "mybatis-config.xml";
        InputStream inputStream = Resources.getResourceAsStream(resource);
        SqlSessionFactory sqlSessionFactory = new SqlSessionFactoryBuilder().build(inputStream);
        //2.获取SqlSession对象,用它来执行sql
        SqlSession sqlSession = sqlSessionFactory.openSession();
        //3.执行sql
//        List<Object> selectList = sqlSession.selectList("test.selectALL");
        //3.获取sql接口方法
        UserMapper usersMapper = sqlSession.getMapper(UserMapper.class);
        List<User> users = usersMapper.selectALL();

        System.out.println(users);

        //4.释放资源
        sqlSession.close();
    }
}
```

![getMapper执行顺序](.\MySQLimg\getMapper执行顺序.png)

![配置Mapper](.\MySQLimg\配置Mapper.png)

### 2.MyBatis核心配置文件

![MyBatis核心配置文件](.\MySQLimg\MyBatis核心配置文件.png)

## 3.MyBatis增删改查

![MyBatis增删改查](.\MySQLimg\MyBatis增删改查.png)

### 1.查询

![MyBatis查询步骤](.\MySQLimg\MyBatis查询步骤.png)

```
数据库表的字段名称  和  实体类的属性名称 不一样，则不能自动封装数据
            * 起别名：对不一样的列名起别名，让别名和实体类的属性名一样
                * 缺点：每次查询都要定义一次别名
                    * sql片段
                        * 缺点：不灵活
            * resultMap：
                1. 定义<resultMap>标签
                2. 在<select>标签中，使用resultMap属性替换 resultType属性
```

```
<!--
    sql片段
-->
<!--
<sql id="brand_column">
     id, brand_name as brandName, company_name as companyName, ordered, description, status
 </sql>

 <select id="selectAll" resultType="brand">
     select
         <include refid="brand_column" />
     from tb_brand;
 </select>
```

```

       	<!--
            id：完成主键字段的映射
                column：表的列名
                property：实体类的属性名
            result：完成一般字段的映射
                column：表的列名
                property：实体类的属性名
        -->
     <resultMap id="brandResultMap" type="brand">
        <result column="brand_name" property="brandName"/>
        <result column="company_name" property="companyName"/>
    </resultMap>



    <select id="selectAll" resultMap="brandResultMap">
        select *
        from tb_brand;
    </select>
```

#### 1.查看详情

![查看详情](.\MySQLimg\查看详情.png)

![转义字符查询](.\MySQLimg\转义字符查询.png)

```
 <!--
     * 参数占位符：
         1. #{}:会将其替换为 ?，为了防止SQL注入
         2. ${}：拼sql。会存在SQL注入问题
         3. 使用时机：
             * 参数传递的时候：#{}
             * 表名或者列名不固定的情况下：${} 会存在SQL注入问题

      * 参数类型：parameterType：可以省略
      * 特殊字符处理：
         1. 转义字符：
         2. CDATA区:
 -->
<!-- <select id="selectById"  resultMap="brandResultMap">
     select *
     from tb_brand where id = #{id};

 </select>
 -->
 <select id="selectById" resultMap="brandResultMap">
     select *
     from tb_brand
     where id
      <![CDATA[
         <
      ]]>
      #{id};

 </select>
```

![查询总结](.\MySQLimg\查询总结.png)

#### 2.条件查询

![多条件查询](.\MySQLimg\多条件查询.png)

```
<!--
    条件查询
-->
<!-- <select id="selectByCondition" resultMap="brandResultMap">
     select *
     from tb_brand
     where status = #{status}
       and company_name like #{companyName}
       and brand_name like #{brandName}
 </select>-->
```

```
//List<Brand> selectByCondition(@Param("status") int status, @Param("companyName") String companyName, @Param("brandName") String brandName);


//List<Brand> selectByCondition(Brand brand);

List<Brand> selectByCondition(Map map);
```

```
@Test
    public void testSelectByCondition() throws IOException {
        //接收参数
        int status = 1;
        String companyName = "华为";
        String brandName = "华为";

        // 处理参数
        companyName = "%" + companyName + "%";
        brandName = "%" + brandName + "%";

        //封装对象
       /* Brand brand = new Brand();
        brand.setStatus(status);
        brand.setCompanyName(companyName);
        brand.setBrandName(brandName);*/

        Map map = new HashMap();
        // map.put("status" , status);
        map.put("companyName", companyName);
        // map.put("brandName" , brandName);

        //1. 获取SqlSessionFactory
        String resource = "mybatis-config.xml";
        InputStream inputStream = Resources.getResourceAsStream(resource);
        SqlSessionFactory sqlSessionFactory = new SqlSessionFactoryBuilder().build(inputStream);

        //2. 获取SqlSession对象
        SqlSession sqlSession = sqlSessionFactory.openSession();

        //3. 获取Mapper接口的代理对象
        BrandMapper brandMapper = sqlSession.getMapper(BrandMapper.class);

        //4. 执行方法

        //List<Brand> brands = brandMapper.selectByCondition(status, companyName, brandName);
//        List<Brand> brands = brandMapper.selectByCondition(brand);
        List<Brand> brands = brandMapper.selectByCondition(map);
        System.out.println(brands);

        //5. 释放资源
        sqlSession.close();

    }
```

![条件查询总结](.\MySQLimg\条件查询总结.png)

#### 3.多条件动态查询

![多条件动态查询](.\MySQLimg\多条件动态查询.png)

```
<select id="selectByCondition" resultMap="brandResultMap">
    select *
    from tb_brand
    where
    <if test="status != null">
        status = #{status}
    </if>
    <if test="companyName != null and companyName != '' ">
        and company_name like #{companyName}
    </if>
    <if test="brandName != null and brandName != '' ">
        and brand_name like #{brandName}
    </if>
</select>
```

改进版

```
<select id="selectByCondition" resultMap="brandResultMap">
    select *
    from tb_brand
    where 1 = 1
    <if test="status != null">
        and status = #{status}
    </if>
    <if test="companyName != null and companyName != '' ">
        and company_name like #{companyName}
    </if>
    <if test="brandName != null and brandName != '' ">
        and brand_name like #{brandName}
    </if>
</select>
```

究极改进版

```
<select id="selectByCondition" resultMap="brandResultMap">
        select *
        from tb_brand
--         where 1 = 1
        <where>
            <if test="status != null">
                and status = #{status}
            </if>
            <if test="companyName != null and companyName != '' ">
                and company_name like #{companyName}
            </if>
            <if test="brandName != null and brandName != '' ">
                and brand_name like #{brandName}
            </if>
        </where>
    </select>
```

#### 4.单条件动态查询

![单条件动态查询](.\MySQLimg\单条件动态查询.png)

### 2.插入

![添加](.\MySQLimg\添加.png)

```java
<insert id="add" useGeneratedKeys="true" keyProperty="id">
    insert into tb_brand (brand_name, company_name, ordered, description, status)
    values (#{brandName},#{companyName},#{ordered},#{description},#{status})
</insert>
```

![sqlsesion默认情况](.\MySQLimg\sqlsesion默认情况.png)

### 3.修改

#### 1.修改动态字段

![修改动态字段](.\MySQLimg\修改动态字段.png)

#### 2.修改全部字段

![修改全部字段](.\MySQLimg\修改全部字段.png)

### 4.删除

#### 1.删除一个

![删除一个](.\MySQLimg\删除一个.png)

#### 2.批量删除

![批量删除](.\MySQLimg\批量删除.png)

## 4.MyBatis参数传递

![MyBatis参数传递](.\MySQLimg\MyBatis参数传递.png)

MyBatis默认会将参数进行封装称为Map集合，一般键的名字为arg0，arg1，arg2...或者param1,param2,param3.....	

我们一般使用**@Param("参数名")**替换掉默认的参数名

![参数传递](.\MySQLimg\参数传递.png)

## 5.注解完成增删改查

![注解完成增删改查](.\MySQLimg\注解完成增删改查.png)

![注解](.\MySQLimg\注解.png)

```
//查询id为x的数据
@Select("select * from tb_brand where id = #{id}")
Brand selectId(int id);
```

