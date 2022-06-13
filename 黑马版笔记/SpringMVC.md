# SpringMVC

![SpringMVC](.\SpringMVCimg\SpringMVC.png)

![SpringMVC概述](.\SpringMVCimg\SpringMVC概述.png)

# 1.RequestMapping

![RequestMapping](.\SpringMVCimg\RequestMapping.png)

# 2.ResponseBody

![ResponseBody](.\SpringMVCimg\ResponseBody.png)

# 3.AbstractDispatcherServletInitalizer

## 3.1 createServletApplicationContext

![createServletApplicationContext](.\SpringMVCimg\createServletApplicationContext.png)

## 3.2 getServletMappings

![getServletMappings](.\SpringMVCimg\getServletMappings.png)

## 3.3 createRootApplicationContext

![createRootApplicationContext](.\SpringMVCimg\createRootApplicationContext.png)

# 4.SpringMVC工作流程

![SpringMVC工作流程](.\SpringMVCimg\SpringMVC工作流程.png)

# 5.Controller加载

![Controller加载](.\SpringMVCimg\Controller加载.png)

## 5.1 ComponentScan

![ComponentScan](.\SpringMVCimg\ComponentScan.png)

## 5.2 加载指定controller

![加载指定文件](.\SpringMVCimg\加载指定文件.png)

```java
@Configuration
@ComponentScan({"com.whh.controller","com.whh.dao"})
public class SpringConfig {
}
```

## 5.3 bean的加载格式

![bean的加载格式](.\SpringMVCimg\bean的加载格式.png)

## 5.4 bean的加载格式简化版

![bean的加载格式简化版](.\SpringMVCimg\bean的加载格式简化版.png)

# 6.请求路径

![请求路径](.\SpringMVCimg\请求路径.png)

## 6.1 post请求中文乱码处理

![post请求中文乱码处理](.\SpringMVCimg\post请求中文乱码处理.png)

# 7.请求参数传参

## 7.1 普通参数

![普通参数](.\SpringMVCimg\普通参数.png)

## 7.2 普通参数名称不匹配

![普通参数名称不匹配](.\SpringMVCimg\普通参数名称不匹配.png)

## 7.3 RequestParam

![RequestParam](.\SpringMVCimg\RequestParam.png)

## 7.4 POJO参数

![POJO参数](.\SpringMVCimg\POJO参数.png)

## 7.5 集合参数

![集合参数](.\SpringMVCimg\集合参数.png)

# 8.请求参数(json传参)

## 8.1 请求(request)

### 8.1.1 添加json坐标

![添加json坐标](.\SpringMVCimg\添加json坐标.png)

### 8.1.2 设置发送json数据

![设置发送json数据](.\SpringMVCimg\设置发送json数据.png)

### 8.1.3 开启json数据的支持

![开启json数据的支持](.\SpringMVCimg\开启json数据的支持.png)

### 8.1.4 设置接受json数据

![设置发送json数据](.\SpringMVCimg\设置发送json数据.png)

### 8.1.5 RequestBody和requestParam区别

![RequestBody和requestParam区别](.\SpringMVCimg\RequestBody和requestParam区别.png)

### 8.1.6 日期类型参数传递

![日期类型参数传递](.\SpringMVCimg\日期类型参数传递.png)

#### 8.1.6.1 DateTimeFormat

![DateTimeFormat](.\SpringMVCimg\DateTimeFormat.png)

#### 8.1.6.2 类型转换器

![类型转换器](.\SpringMVCimg\类型转换器.png)

## 8.2 响应(response)

### 8.2.1 响应页面

![响应页面](.\SpringMVCimg\响应页面.png)

### 8.2.2 响应文本数据

![响应文本数据](.\SpringMVCimg\响应文本数据.png)

### 8.2.3 响应json数据

![响应json数据](.\SpringMVCimg\响应json数据.png)

### 8.2.4 对象集合

![对象集合](.\SpringMVCimg\对象集合.png)

### 8.2.5 ResponseBody注解

![ResponseBody注解](.\SpringMVCimg\ResponseBody注解.png)

### 8.2.6 类型转换器HttpMessageConverter

![类型转换器HttpMessageConverter](.\SpringMVCimg\类型转换器HttpMessageConverter.png)

# 9.REST风格

## 9.1 REST简介

![REST简介](.\SpringMVCimg\REST简介.png)

## 9.2 REST风格简介

![REST风格简介](.\SpringMVCimg\REST风格简介.png)

## 9.3 REST入门案例

### 9.3.1 设定http请求动作

![设定http请求动作](.\SpringMVCimg\设定http请求动作.png)

### 9.3.2 设置请求参数

![设置请求参数](.\SpringMVCimg\设置请求参数.png)

## 9.4 RequestMapping方法详解

![RequestMapping方法详解](.\SpringMVCimg\RequestMapping方法详解.png)

## 9.5 PathVariable

![PathVariable](.\SpringMVCimg\PathVariable.png)

## 9.6 RequestBody、RequestParam、PathVariable三者区别

![RequestBody、RequestParam、PathVariable三者区别](.\SpringMVCimg\RequestBody、RequestParam、PathVariable三者区别.png)

## 9.7 RestController

![RestController](.\SpringMVCimg\RestController.png)

## 9.8.常用四个注解

![常用四个注解](.\SpringMVCimg\常用四个注解.png)
