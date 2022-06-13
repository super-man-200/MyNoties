# 1.MyBatis Plus

![MyBatisPlus简介](E:\笔记\MyBatisPlus\MyBatisPlus简介.png)

## 1.1 springboot整合mybatisPlus.png

![springboot整合mybatisPlus](E:\笔记\MyBatisPlus\springboot整合mybatisPlus.png)

## 1.2 选择当前模块

![选择当前模块](E:\笔记\MyBatisPlus\选择当前模块.png)

## 1.3 手动添加mp起步依赖

![手动添加mp起步依赖](E:\笔记\MyBatisPlus\手动添加mp起步依赖.png)

## 1.4 设置jdbc

![设置jdbc](E:\笔记\MyBatisPlus\设置jdbc.png)

## 1.5 制作实体类与表结构

![制作实体类与表结构](E:\笔记\MyBatisPlus\制作实体类与表结构.png)

## 1.6 定义数据接口

![定义数据接口](E:\笔记\MyBatisPlus\定义数据接口.png)

## 1.7 测试类中注入dao接口

![测试类中注入dao接口](E:\笔记\MyBatisPlus\测试类中注入dao接口.png)

# 2.MP特征

![mp特征](E:\笔记\MyBatisPlus\mp特征.png)

# 3.标准CRUD功能

![标准CRUD功能](E:\笔记\MyBatisPlus\标准CRUD功能.png)

## 3.1 lombok

![lombok](E:\笔记\MyBatisPlus\lombok.png)

### lombok常用注解

![lombok常用注解](E:\笔记\MyBatisPlus\lombok常用注解.png)

## 3.2 分页功能

### 3.2.1 设置分页拦截器作为spring管理的bean

![设置分页拦截器作为spring管理的bean](E:\笔记\MyBatisPlus\设置分页拦截器作为spring管理的bean.png)

### 3.2.2 执行分页查询

![执行分页查询](E:\笔记\MyBatisPlus\执行分页查询.png)

### 3.2.3 开启日志

![开启日志](E:\笔记\MyBatisPlus\开启日志.png)

# 4.DQL编程控制

## 4.1 条件查询

![设置条件查询1](E:\笔记\MyBatisPlus\设置条件查询1.png)

![设置条件查询2](E:\笔记\MyBatisPlus\设置条件查询2.png)

## 4.2 条件关系

![条件查询](E:\笔记\MyBatisPlus\条件查询.png)

## 4.3 条件查询null值处理

### 4.3.1 if处理

![null值处理1](E:\笔记\MyBatisPlus\null值处理1.png)

### 4.3.2 条件参数控制

![null值处理2](E:\笔记\MyBatisPlus\null值处理2.png)

## 4.4 查询投影

![查询投影](E:\笔记\MyBatisPlus\查询投影.png)

## 4.5 查询条件

![查询条件](E:\笔记\MyBatisPlus\查询条件.png)

![查询条件2](E:\笔记\MyBatisPlus\查询条件2.png)

![查询条件网址](E:\笔记\MyBatisPlus\查询条件网址.png)

## 4.6 字段映射与表名映射

### 4.6.1 表字段与编码属性不一致

![字段映射与表名映射](E:\笔记\MyBatisPlus\字段映射与表名映射.png)

### 4.6.2 编码中添加了数据库中未定义的属性

![编码中添加了数据库中未定义的属性](E:\笔记\MyBatisPlus\编码中添加了数据库中未定义的属性.png)

### 4.6.3 字段不参与查询

![不参与查询](E:\笔记\MyBatisPlus\不参与查询.png)

### 4.6.4 表名和编码开发设计不同步

![表名和编码开发设计不同步](E:\笔记\MyBatisPlus\表名和编码开发设计不同步.png)

## 4.7 TableField

![TableField](E:\笔记\MyBatisPlus\TableField.png)

## 4.8 TableName

![TableName](E:\笔记\MyBatisPlus\TableName.png)

## 4.9 TableId

![TableId](E:\笔记\MyBatisPlus\TableId.png)

## 4.10 id自动生成

![id自动生成](E:\笔记\MyBatisPlus\id自动生成.png)

### 4.10.1 id全局配置

![id全局配置](E:\笔记\MyBatisPlus\id全局配置.png)

## 4.11 多记录操作

![多记录操作](E:\笔记\MyBatisPlus\多记录操作.png)

## 4.12 逻辑删除

### 4.12.1 添加deleted字段

![添加deleted字段](E:\笔记\MyBatisPlus\添加deleted字段.png)

### 4.12.2 实体类中添加对应的字段

![实体类中添加对应的字段](E:\笔记\MyBatisPlus\实体类中添加对应的字段.png)

### 4.12.3 配置通用配置

![配置通用配置](E:\笔记\MyBatisPlus\配置通用配置.png)

要想查询被逻辑删除标记的数据，则需要自己编写sql语句

## 4.13 乐观锁

解决并发带来的问题

### 4.13.1 添加乐观锁字段

![添加乐观锁字段](E:\笔记\MyBatisPlus\添加乐观锁字段.png)

### 4.13.2 添加version字段

![添加version字段](E:\笔记\MyBatisPlus\添加version字段.png)

### 4.13.3 拦截器

![拦截器](E:\笔记\MyBatisPlus\拦截器.png)

### 4.13.4 修改前获取version

![修改前获取version](E:\笔记\MyBatisPlus\修改前获取version.png)

# 5.快速开发

![代码生成器](E:\笔记\MyBatisPlus\代码生成器.png)

## 5.1 获取依赖

![代码生成器第一步](E:\笔记\MyBatisPlus\代码生成器第一步.png)

## 5.2 创建代码生成器对象

![创建代码生成器生成对象](E:\笔记\MyBatisPlus\创建代码生成器生成对象.png)

## 5.3 数据源指定

![数据源指定](E:\笔记\MyBatisPlus\数据源指定.png)

## 5.4 设置全局配置

![设置全局配置](E:\笔记\MyBatisPlus\设置全局配置.png)

## 5.5 包相关配置

![包相关配置](E:\笔记\MyBatisPlus\包相关配置.png)

## 5.6 策略配置

![策略配置](E:\笔记\MyBatisPlus\策略配置.png)

