# 1.java的长期维护版

jdk（java development kit）

jdk8、jdk11、jdk17

# 2.JDK,JRE,JVM三者之间的关系

JDK = JRE + Java的开发工具(javac.exe,java.exe,javadoc.exe)

JRE = JVM + Java核心类库

# 3.关键字的定义（Key word）

被java语言赋予特殊的含义，用于专门用途的单词

true、false、null不算是关键字

# 4.保留字（Reserved word）

现有版本java尚未使用，以后可能会当关键是使用。 goto、const

# 5.标识符（Idnetifier）

java对各种变量、方法和类等要素命名时使用的字符序列称为标识符

定义合法标识符规则：

- 由26个英文字母大小写，0-9，_或$组成。
- 不可以以数字开头。
- 不可以使用关键字和保留字，但能包含关键字和保留字。
- java中严格区分大小写，长度无限制
- 标识符不能包含空格

根据**阿里巴巴开发规范**，**不能以$和_开头或者结束**，要见名知意，不要故意缩写，可以适当缩写

**包名**：多个单词组成都用小写，单词和单词之间使用.隔开，单词使用**单数**形式

**类名**：遵行大驼峰(UpperCamelCase)风格

**方法名、参数名、成员变量**：遵守小驼峰（LowerCamelCase）风格

**常量**：全部用大写，单词间隔使用_隔开，不建议简写

**抽象类**：命名使用Abstract或Base开头

**异常类**：命名使用Exception结尾

**测试类**：以测试名称开始，以Test作为结尾

**数组**：int[] arr来代表一个数组，不要使用int arr[]格式

# 6.变量（Variable）

**概念**：

- 内存中的一个内存区域
- 该区域的数据可以在同一个类型范围内不断地变换
- 变量是程序中最基本的存储单元，包含变量类型、变量名、存储的值

变量的使用: 数据类型 变量名 = 变量值;

**注意**：

- 变量要先赋值在使用
- 变量要定义在作用域内
- 同一个作用域中不可以定义两个相同的变量

# 7.数据类型

**基本数据类型**

- 整形：byte、short、int、long
- 浮点型：float、double
- 字符型：char
- 布尔型：boolean

**引用数据类型**

- 类（class）
- 接口（interface）
- 数组（array）

## 整形

| 类型  | 占用存储空间 | 范围                 |
| ----- | ------------ | -------------------- |
| byte  | 1字节(1Byte) | -128~127             |
| short | 2字节(2Byte) | $-2^{15}$~$2^{15}-1$ |
| int   | 4字节(4Byte) | $-2^{31}$~$2^{31}-1$ |
| long  | 8字节(8Byte) | $-2^{63}$~$2^{63}-1$ |

定义long型数据要在变量后面+l或L

```
lont i = 300L;
long i = 300l;
```

bit（位）：计算机中的**最小存储单元**

byte（字节）：计算机中**基本存储单元**

## 浮点型

| 类型           | 占用存储空间 | 范围                 |
| -------------- | ------------ | -------------------- |
| float(单精度)  | 4字节(4Byte) | -3.403E38~3.403E38   |
| double(双精度) | 8字节(8Byte) | -1.798E308~1.798E308 |

float尾数可以精确到7位有效数字

double精度是float的两倍

声明**float类**型常量，**必须**在**后面加f或F**

```java
float f = 3.14f;
float f = 3.14F;
```

## 字符型

| 类型 | 占用存储空间 |
| ---- | ------------ |
| char | 2字节(2Byte) |

# MVC设计模式

分为三个层次：视图模型层、控制器层、数据模型层

**模型层 model** 主要处理数据

数据对象封装 bean/domain/dao

**控制层 controller**  处理业务逻辑

服务相关的类 service

抽取的基类 base

**视图层 view**  显示数据

相关的工具类 utils

自定义的视图 ui
