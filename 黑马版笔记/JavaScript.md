# 1.JavaScript简介

![JavaScript简介](..\笔记\JavaScriptimg\JavaScript简介.png)

# 2.JavaScript引入方式

![JS引入方式](..\笔记\JavaScriptimg\JS引入方式.png)

## 1.内部脚本

![内部脚本](..\笔记\JavaScriptimg\内部脚本.png)

## 2.外部脚本

![外部脚本](..\笔记\JavaScriptimg\外部脚本.png)

# 3.JavaScript基础语法

## 1.书写语法

![书写语法](..\笔记\JavaScriptimg\书写语法.png)

## 2.输出语句

![输出语句](..\笔记\JavaScriptimg\输出语句.png)

## 3.变量

![变量](..\笔记\JavaScriptimg\变量.png)

## 4.数据类型

![数据类型](..\笔记\JavaScriptimg\数据类型.png)

## 5.运算符

![运算符](..\笔记\JavaScriptimg\运算符.png)

```
var age1 = 21;
var age2 = "21";
alert(age1 == age2); //true
==
1.判断类型是否一样，不一样则进行转换
2.再去比较其值
alert(age1 === age2); //false
=== 
1.判断类型是否一样，不一样不进行类型转换，直接返回false
2.再去比较其值
```

### 类型转换

#### 1.其他类型转为number：

##### 1.string

按照字符串的字面值进行转换，如果字面值不是数字，则转为NaN，一般使用paresInt(变量)方法进行转换

##### 2.boolean

true转为1，false转为0

#### 2.其他类型转为boolean：

##### 1.number

0和NaN转换为false，其他数值转换为true

##### 2.string

空字符串转为false，其他字符串传为true

##### 3.null

false

##### 4.undefined

false

#### 3.总结

![类型转换总结](..\笔记\JavaScriptimg\类型转换总结.png)

## 6.流程控制语句

![流程控制语句](..\笔记\JavaScriptimg\流程控制语句.png)

跟java一样，略

## 7.函数

![函数](..\笔记\JavaScriptimg\函数.png)

### 定义方法2

![定义方式2](..\笔记\JavaScriptimg\定义方式2.png)

# 4.JavaScript对象

## 1.Array

![Array](..\笔记\JavaScriptimg\Array.png)

### 属性方法

![Array属性方法](..\笔记\JavaScriptimg\Array属性方法.png)

```
var arr1 = [1, 2, 3];
arr1.push(4);//从某位添加元素
alert(arr1);//1，2，3，4

var arr1 = [1, 2, 3];
arr1.pop(4);//从某位删除元素
alert(arr1);//1，2，3

var arr1 = [1, 2, 3];
arr1.splice(0,1);//从x位，删除x个元素
alert(arr1);//1，2，3
```

## 2.string

![string](..\笔记\JavaScriptimg\string.png)

trim()去除字符串前后两端的空白字符

## 3.自定义对象

![自定义对象](..\笔记\JavaScriptimg\自定义对象.png)

# 5.BOM

![BOM](..\笔记\JavaScriptimg\BOM.png)

## 1.Window

![Window](..\笔记\JavaScriptimg\Window.png)

confirm()点击确定按钮会返回值true或者false

```
var r = confirm("你好吗?");
```

setInterval()和setTimeout()的区别

```
setInterval(参数1,参数2)//函数，执行毫秒数
setInterval(function() {
    alert("111");
}, 5000);
//每隔五秒执行一次
```

```
setTimeout(参数1,参数2)//函数，执行毫秒数
setTimeout(function() {
    alert("setTimeout");
}, 5000);
//只执行一次
```

## 2.History

![History](..\笔记\JavaScriptimg\History.png)

## 3.Location

![Location](..\笔记\JavaScriptimg\Location.png)

# 6.DOM

![DOM](..\笔记\JavaScriptimg\DOM.png)

![DOM2](..\笔记\JavaScriptimg\DOM2.png)

## 1.获取Element

![获取Element对象](..\笔记\JavaScriptimg\获取Element对象.png)

## 2.常见HTML Element对象的使用

查阅文档

# 7.事件监听

![事件监听](..\笔记\JavaScriptimg\事件监听.png)

## 1.事件绑定

![事件绑定](..\笔记\JavaScriptimg\事件绑定.png)

## 2.常见事件

![常见事件](..\笔记\JavaScriptimg\常见事件.png)

**onsubmit**输出**true提交表单**，**false不提交表单**

# 8.正则表达式

![正则表达式](..\笔记\JavaScriptimg\正则表达式.png)

