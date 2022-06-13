# 1.spring发展史

![spring发展史2](..\笔记\Springimg\spring发展史2.png)

![spring发展史](..\笔记\Springimg\spring发展史.png)

# 2.spring系统架构

![spring系统架构图](..\笔记\Springimg\spring系统架构图.png)

![spring系统架构2](..\笔记\Springimg\spring系统架构2.png)

# 3.IoC和DI

![IoC和DI](..\笔记\Springimg\IoC和DI.png)

![IoC和DI目的](..\笔记\Springimg\IoC和DI目的.png)

# 4.DI配置和IoC基本配置

![application获取](..\笔记\Springimg\application获取.png)

![DI配置](..\笔记\Springimg\DI配置.png)

# 5.bean的基本配置

![bean的基本配置](..\笔记\Springimg\bean的基本配置.png)

## 5.1 bean别名

![bean别名](..\笔记\Springimg\bean别名.png)

## 5.2 bean的作用范围

![bean的作用范围](..\笔记\Springimg\bean的作用范围.png)

默认为单例模式

因为如果不是单例模式，那么每次创建一个对象就创建一个实例，内存开销会无穷无尽，不好管理

## 5.3 bean容器的使用

![bean容器的使用](..\笔记\Springimg\bean容器的使用.png)

# 6.bean实例化的三种方法

## 6.1 构造方法

![构造方法](..\笔记\Springimg\构造方法.png)

**报错信息从下往上看**

## 6.2 静态工厂

![静态工厂](..\笔记\Springimg\静态工厂.png)

## 6.3 实例工厂

![实例工厂](..\笔记\Springimg\实例工厂.png)

## 6.4 FactoryBean

![FactoryBean](..\笔记\Springimg\FactoryBean.png)

# 7.bean的生命周期

## 7.1 方法一

![生命周期控制方法1](..\笔记\Springimg\生命周期控制方法1.png)

## 7.2 方法二

![生命周期控制方法2](..\笔记\Springimg\生命周期控制方法2.png)

## 7.3 bean的销毁时机

![bean的销毁时机](..\笔记\Springimg\bean的销毁时机.png)

# 8.依赖注入

## 8.1 setter注入

![setter注入](..\笔记\Springimg\setter注入.png)

## 8.2 构造器注入

### 8.2.1 引用类型

![引用类型](..\笔记\Springimg\引用类型.png)

### 8.2.2 简单类型

![简单类型](..\笔记\Springimg\简单类型.png)

### 8.2.3 参数适配

![参数适配](..\笔记\Springimg\参数适配.png)

## 8.3 依赖注入小结

![依赖注入小结](..\笔记\Springimg\依赖注入小结.png)

# 9.自动分配

## 9.1 按类型自动装配

![按类型自动装配](..\笔记\Springimg\按类型自动装配.png)

## 9.2 自动装配特征

![自动装配特征](..\笔记\Springimg\自动装配特征.png)

# 10.集合注入

**在bean标签里面书写**

## 10.1 数组

![数组](..\笔记\Springimg\数组.png)

## 10.2 List

![List](..\笔记\Springimg\List.png)

## 10.3 set

![set](..\笔记\Springimg\set.png)

## 10.4 map

![map](..\笔记\Springimg\map.png)

## 10.5 properties

![properties](..\笔记\Springimg\properties.png)

# 11.数据源对象管理

![druid](..\笔记\Springimg\druid.png)

# 12.加载properties文件

![加载properties头文件](..\笔记\Springimg\加载properties头文件.png)

![加载properties文件](..\笔记\Springimg\加载properties文件.png)

## properties路径设置

![properties路径](..\笔记\Springimg\properties路径.png)

# 13.容器

## 13.1 创建容器

![创建容器](..\笔记\Springimg\创建容器.png)

## 13.2 获取bean

![获取bean](..\笔记\Springimg\获取bean.png)

## 13.3 容器类层次结构图

![容器类层次结构图](..\笔记\Springimg\容器类层次结构图.png)

## 13.4 BeanFactory初始化

![BeanFactory初始化](..\笔记\Springimg\BeanFactory初始化.png)

# 14.核心容器总结

## 14.1 容器相关

![容器相关](..\笔记\Springimg\容器相关.png)

## 14.2 bean相关

![bean相关](..\笔记\Springimg\bean相关.png)

## 14.3 依赖注入相关

![依赖注入相关](..\笔记\Springimg\依赖注入相关.png)

# 15.注解开发

## 15.1 Component注解

![Component](..\笔记\Springimg\Component.png)

## 15.2 衍生注解

![衍生注解](..\笔记\Springimg\衍生注解.png)

## 15.3 纯注解开发

![纯注解开发](..\笔记\Springimg\纯注解开发.png)

### 配置类

![配置类](..\笔记\Springimg\配置类.png)

# 16.管理bean

## bean的生命周期

![bean生命周期](..\笔记\Springimg\bean生命周期.png)

# 17.注解依赖注入

![注解依赖注入](..\笔记\Springimg\注解依赖注入.png)

## 17.1 注解依赖注入指定装配

![注解依赖注入指定装配](..\笔记\Springimg\注解依赖注入指定装配.png)

## 17.2 value

![value](..\笔记\Springimg\value.png)

## 17.3 注解加载properties文件

![注解加载properties文件](..\笔记\Springimg\注解加载properties文件.png)

# 18.管理第三方bean

## 18.1 使用单独的类管理第三方bean

![管理第三方bean](..\笔记\Springimg\管理第三方bean.png)

## 18.2 导入方式

### 18.2.1 导入式

![导入式](..\笔记\Springimg\导入式.png)

### 18.2.2 扫描式

![扫描式](..\笔记\Springimg\扫描式.png)

# 19.第三方bean依赖注入

## 19.1 简单类型注入

![简单类型注入](..\笔记\Springimg\简单类型注入.png)

## 19.2 引用类型注入

![引用类型注入](..\笔记\Springimg\引用类型注入.png)

# 20.XML配置对比注解配置

![XML配置对比注解配置](..\笔记\Springimg\XML配置对比注解配置.png)

# 21.Spring整合MyBatis

## 21.1 MyBatis

![MyBatis](..\笔记\Springimg\MyBatis.png)

## 21.2 MyBatis整合（XML文件）

![MyBatis整合](..\笔记\Springimg\MyBatis整合.png)

## 21.3 MyBatis类优化

![MyBatis优化1](..\笔记\Springimg\MyBatis优化1.png)

![MyBatis优化2](..\笔记\Springimg\MyBatis优化2.png)

# 22.整合JUnit

![整合JUnit](..\笔记\Springimg\整合JUnit.png)

# 23.AOP

![AOP简介](..\笔记\Springimg\AOP简介.png)

![概念图](..\笔记\Springimg\概念图.png)

![AOP核心概念](..\笔记\Springimg\AOP核心概念.png)

## 23.1 导入aop坐标

![导入aop坐标](..\笔记\Springimg\导入aop坐标.png)

## 23.2 定义dao实现类

![定义dao实现类](..\笔记\Springimg\定义dao实现类.png)

## 23.3 定义通知类

![定义通知类](..\笔记\Springimg\定义通知类.png)

## 23.4 定义切入点

![定义切入点](..\笔记\Springimg\定义切入点.png)

## 23.5 绑定切入点和通知关系

![绑定切入点和通知关系](..\笔记\Springimg\绑定切入点和通知关系.png)

## 23.6 定义通知类受Spring容器管理

![定义通知类受Spring容器管理](..\笔记\Springimg\定义通知类受Spring容器管理.png)

## 23.7 开启Spring对AOP注解驱动的支持

![开启Spring对AOP注解驱动的支持](..\笔记\Springimg\开启Spring对AOP注解驱动的支持.png)

# 24.AOP的工作流程

![AOP工作流程](..\笔记\Springimg\AOP工作流程.png)

![AOP代理对象](..\笔记\Springimg\AOP代理对象.png)

# 25.AOP切入点表达式

![AOP切入点表达式](..\笔记\Springimg\AOP切入点表达式.png)

## 25.1 切入点表达式标准格式

![切入点表达式标准格式](..\笔记\Springimg\切入点表达式标准格式.png)

## 25.2 切入点表达式通配符

![切入点表达式通配符](..\笔记\Springimg\切入点表达式通配符.png)

## 25.3 书写技巧

![书写技巧](..\笔记\Springimg\书写技巧.png)

# 26.AOP通知类型

![通知类型](..\笔记\Springimg\通知类型.png)

## 26.1 Before

![Before](..\笔记\Springimg\Before.png)

## 26.2 After

![After](..\笔记\Springimg\After.png)

## 26.3 Around

![Around](..\笔记\Springimg\Around.png)

![Around注意事项](..\笔记\Springimg\Around注意事项.png)

## 26.4 AfterReturning

![AfterReturning](..\笔记\Springimg\AfterReturning.png)

## 26.5 AfterThrowing

![AfterThrowing](..\笔记\Springimg\AfterThrowing.png)

## 26.执行签名信息

![执行签名信息](..\笔记\Springimg\执行签名信息.png)

```java
Signature signature = pj.getSignature();//获取签名信息
signature.getDeclaringTypeName();//路径名
signature.getName();//方法名
```

# 27.AOP通知获取数据

## 27.1 获取原始方法的调用参数

![获取原始方法的调用参数](..\笔记\Springimg\获取原始方法的调用参数.png)

## 27.2 接受异常信息

![接受异常信息](..\笔记\Springimg\接受异常信息.png)

## 27.3 抛出异常数据

![抛出异常数据](..\笔记\Springimg\抛出异常数据.png)

# 28.删除前后空格

![删除前后空格](..\笔记\Springimg\删除前后空格.png)

# 29.AOP总结

![AOP总结](..\笔记\Springimg\AOP总结.png)

## 29.1 切入点

![切入点](..\笔记\Springimg\切入点.png)

## 29.2 通知类型总结

![通知类型总结](..\笔记\Springimg\通知类型总结.png)

## 29.3 切入点方法的参数

![切入点方法的参数](..\笔记\Springimg\切入点方法的参数.png)

# 30.Spring事务介绍

![事务简介](..\笔记\Springimg\事务简介.png)

## 30.1 事务开启步骤

### 30.1.1 第一步

![事务开启步骤](..\笔记\Springimg\事务开启步骤.png)

### 30.1.2 第二步

![第二步设置事务管理器](..\笔记\Springimg\第二步设置事务管理器.png)

### 30.1.3 第三步

![开启注解事务驱动](..\笔记\Springimg\开启注解事务驱动.png)

# 31.事务相关配置

![](..\笔记\Springimg\事务相关配置.png)

## 31.1 创建新的事务

![创建新的事务](..\笔记\Springimg\创建新的事务.png)

## 31.2 事务传播行为

![事务传播行为](..\笔记\Springimg\事务传播行为.png)



