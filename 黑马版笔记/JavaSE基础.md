# 1.java入门

## 1.基础知识

JDK 8、JDK11、JDK17是LTS（long-term support）长期支持版

oracle官网下载[Oracle 甲骨文中国 - 云服务 - 云基础设施 | 集成的云应用和平台服务](https://www.oracle.com/cn/index.html)

javac -version 查看java版本

javac 编译命令 **javac 类名.class**

java 运行 **java 类名**

<img src=".\img\image-20220315104312846.png" alt="image-20220315104312846" align="left"/>

开发的三个步骤：**编写代码，编译代码，运行代码**

文件名必须与代码的类名一致

**JDK11**之后，**javac 类名.class**可以直接运行！

编程语言的发展历程

1. 机器语言
2. 汇编语言
3. 高级语言

java是一种高级语言

**JVM(Java Virtual Machine)Java虚拟机** ：真正运行java程序的地方

**核心类库**：java自己写好的一些程序，方便开发者调用

**JRE(Java Runtime Environment)Java的运行环境**

**JDK(Java Development Kit)Java开发工具包**

![QQ截图20220315111211](.\img\QQ截图20220315111211.png)

**Java的跨平台**

**一次编译，处处可用**：程序只需要开发一次，就可以在各种安装了JVM的系统平台上运行

![QQ截图20220315111330](.\img\QQ截图20220315111330.png)

## **2.path环境变量**



![QQ截图20220315111921](.\img\QQ截图20220315111921.png ) 

<img src=".\img\QQ截图20220315111937.png" alt="QQ截图20220315111937"  />

![QQ截图20220315111947](.\img\QQ截图20220315111947.png)

path的不同

![QQ截图20220315112206](.\img\QQ截图20220315112206.png)

上者针对当前用户有效，下者针对全部用户有效

将java的bin目录保存，创建JAVA_HOME文件路径

![QQ截图20220315112334](.\img\QQ截图20220315112334.png)

然后复制到path路径中

![QQ截图20220315112351](.\img\QQ截图20220315112351.png)

完成创建，我们就可以在cmd窗口里面使用java命令了

## **3.工程文件体系结构**

![QQ截图20220315113243](.\img\QQ截图20220315113243.png)

![QQ截图20220315113648](.\img\QQ截图20220315113648.png)

![QQ截图20220315113812](.\img\QQ截图20220315113812.png)

![QQ截图20220315114008](.\img\QQ截图20220315114008.png)

## **3.IDEA中的快捷键**

![QQ截图20220315114220](.\img\QQ截图20220315114220.png)

**修改类/模块名：shift+f6**

## **4.模块和工程的导入删除：**

### **1.从磁盘导入**

<img src=".\img\QQ截图20220315114940.png" alt="QQ截图20220315114940" style="zoom:50%;" align="left"/>

<img src=".\img\QQ截图20220315115056.png" alt="QQ截图20220315115056" style="zoom:50%;" align="left"/>

此种方法存在一个问题就是，一旦被导入的模块被修改，项目中的模块也会随之改变，此时我们应该采用第二种方法

### **2.新建模块，在复制模块中的文件**

<img src=".\img\QQ截图20220315115518.png" alt="QQ截图20220315115518" style="zoom: 50%;" align="left"/>

现在我们再去修改原模块中的文件，我们本模块的文件也不会发生改变

### **3.删除模块**

1.在idea里面移除模块

<img src=".\img\QQ截图20220315120025.png" alt="QQ截图20220315120025" style="zoom:80%;" align="left"/>

2.然后在磁盘里删除

### **4.打开工程**

<img src=".\img\QQ截图20220315120325.png" alt="QQ截图20220315120325" style="zoom:80%;" align="left"/>

### **5.关闭工程**

<img src=".\img\QQ截图20220315120441.png" alt="QQ截图20220315120441" style="zoom: 80%;" align="left" />

## 5.**注释**

<img src=".\img\QQ截图20220315132910.png" alt="QQ截图20220315132910" style="zoom:50%;" align="left"/><img src=".\img\QQ截图20220315132900.png" alt="QQ截图20220315132900" style="zoom: 50%;" align="left"/><img src=".\img\QQ截图20220315132905.png" alt="QQ截图20220315132905" style="zoom:50%;" />

ctrl+/单行注释

ctrl+shift+/多行注释

## 6.字面量

字面量：就是数据在程序中书写的格式

![QQ截图20220315134341](.\img\QQ截图20220315134341.png)

字符在程序中的输入格式：‘我’

字符串在程序中的输入格式：“怡宝没有农夫三拳好喝”

## 7.变量variable	

变量：变量就是数据在内存中存储数据的一段内存区域，存储区域里面的数据可以改变

变量的定义格式：数据类型 变量名 = 初始值；

变量的注意事项

1.变量的作用域是在{}里面的，同一范围内变量名不可以重复

2.变量类型声明后，不能再存储其他类型的数据

3.先声明，在使用

4.变量可以定义初始化值，但是使用的时候必须要定义初始值

## 8.进制

1.**二进制(Binary)（计算机的语言）**

只有0，1

2.**八进制(Octal)**

以0开头，0-7，逢7进1

3.**十六进制(Hexadecimal)**

以0x开头，0-15，10-A,11-B,12-C,13-D,14-E,15-F,逢15进1

4.**十进制**

0-9，逢10进1

## 9.计算机单位

### 1.**字节（Byte）**

二进制的一位代表bit，8 bit = 1 Byte

计算机的**基本存储单位**，一般计算机为8位为一个字节

![QQ截图20220315141739](.\img\QQ截图20220315141739.png)

### 2.**ASCLL编码**

![QQ截图20220315140859](.\img\QQ截图20220315140859.png)

常用的ASCLL编码 a=97，A=65，0=45

# 2.基本数据类型

数据类型分为两种：基本数据类型和引用数据类型

![QQ截图20220315141854](.\img\QQ截图20220315141854.png)

定义**long型数据**，需要在初始值**后面加上L/l。**

定义**float型数据**，需要在初始值**后面加上F/f。**

## 1.关键字和标识符

### 1.**关键字**

关键字不能拿来定义变量名，否则会报错

![QQ截图20220315142639](.\img\QQ截图20220315142639.png)

### 2.**标识符**

标识符：就是给变量，类，方法等起名字的规范

由数字、字母、下划线和美元$组成

不能以数字开头，不能是关键字，区分大小写

命名规则：

变量名，方法：一般由小驼峰形式

类名：大驼峰模式

## 2.自动类型转换

**字节数小**的类型的值赋给**字节数大**的类型的时候，会发生**自动类型转换**

但是**字节数大**的类型的值赋给**字节数小**的类型时，**会报错**

![QQ截图20220315144549](.\img\QQ截图20220315144549.png)

**运算规则注意事项**

![QQ截图20220315144946](.\img\QQ截图20220315144946.png)

**强制类型转换**

数据类型 变量 = （数据类型）变量/数据；

![QQ截图20220315145459](.\img\QQ截图20220315145459.png)

# 3.运算符

### 1.算符运算符

![QQ截图20220315145942](.\img\QQ截图20220315145942.png)

3 / 2 = 1

3.0 / 2 = 1.5

3 / 2.0 = 1.0

三位数求个、十、百位

各位：i % 10

十位：i / 10 % 10

百位：i / 100

**”+“作为连接符**

当数据之间可以计算时就计算，但不可以结算时，就连接在一起（能算则算，不能算就连接在一起）

eg：10 + 10 = 20，”skdj“ + ”askdjf“ = ”skdjaskdjf“

### 2.自增自减运算符

![QQ截图20220315151021](.\img\QQ截图20220315151021.png)

int i =1;

i++ 表达式：1，i变量自身：2

i-- 表达式：1，i变量自身：0

++i 表达式：2，i变量自身：2

--i 表达式：0，i变量自身：0

### 3.基本赋值运算符

![QQ截图20220315151833](.\img\QQ截图20220315151833.png)

```
byte i = 10;

byte j = 10;

**i += j;   =====>  i = (byte)i + j;
```



### 4.关系运算符

![QQ截图20220315152156](.\img\QQ截图20220315152156.png)

```
int i = 0;

int j = 5;

**Systeam.out.prinln(i = j);   ======> 5
```



### 5.逻辑运算符

![QQ截图20220315152657](.\img\QQ截图20220315152657.png)

![QQ截图20220315152947](.\img\QQ截图20220315152947.png)

### 6.三元运算符

![QQ截图20220315153146](.\img\QQ截图20220315153146.png)

### 7.运算符优先级关系

![QQ截图20220315153306](.\img\QQ截图20220315153306.png)

### 8.Scanner用户输入类

```java
格式：Scanner s = new Scanner(System.in);

int i = s.nextInt();//输入int类型的数据

double i = s.nextDouble();//输入double类型的数据

String i = s.next();//获取字符串类型的数据

String i = s.nextLine()//获取字符串类型的数据，包括返回跳过的输入
```

详情请参考API

# 4.程序流程控制

## 1.分支结构

### 1.if

![if](.\img\if.png)

### 2.switch

![switch](.\img\switch.png)

![switch2](.\img\switch2.png)

## 2.循环结构

### 1.for

![for](.\img\for.png)

### 2.while

![while](.\img\while.png)

### 3.do-while

![do-while](.\img\do-while.png)

**3种循环的特点**

for：**循环变量**在循环完成之后**不可以使用**

while：**循环变量**在循环完成之后**可以使用**

do-while：继承了上面**while的特性**，而且**无论如何都要执行一次**

## 4.死循环

![死循环](.\img\死循环.png)

## 5.循环关键字

### 1.break,continue

![循环关键字](.\img\循环关键字.png)

## 6.随机数Random类

![random](.\img\random.png)

**Random类取数值，遵循[0,N),包含左边，不包含右边。**

```java
格式： Random r = new Random();

int i = r.nextInt(10)//0-10之间的随机整数,不包含10

double i = r.nextDouble(10)//0-10之间的随机数,不包含10
```

详情参考RandomAPI

# 5.数组

## 1.静态初始化数组

### 1.完整格式

```
数据类型[] 数组名 = new 数据类型[]{元素1，元素2....}；

int[] i =new int[]{1,2,3....};
```



### 2.简化格式

```
数据类型[] 数组名 = {元素1，元素2....}；

int[] i ={1,2,3.....};
```



### 3.存储原理

![数组1](.\img\数组1.png)

如何获取数组地址，在控制台输出数组名即可Systeam.out.prinln(ages);

获取数组值  数组名[下标]

```
ages.length  ==> 获取数组长度

ages.length - 1 ==>最大下标  //**前提元素个数大于0
```



### 4.注意事项

![数组2](.\img\数组2.png)

```
int[] i ={1,2,3.....}; ==> int i[] = {1,2,3.....};
```



## 2.动态初始化数组

### 1.定义形式

![数组3](.\img\数组3.png)

```
int[] i = new int[3];

System.out.prinln(i[0]);  ===> 0  //**当定义数组时没有赋值，就会采用默认值
```



### 2.动态初始化数组的默认值

![数组4](.\img\数组4.png)

## 3.数组的遍历

![数组遍历](.\img\数组遍历.png)

## 4.冒泡排序

![冒泡排序关键代码](.\img\冒泡排序关键代码.png)

## 5.java的内存分配

**基本数据类型存的是值**

```
int i = 20;

System.out.prinlt(i); ===> 20
```

**引用数据类型存的是地址**

```
int[] i = {1,2,3};

System.out.prinln(i);  ===> [i@4c873330]
```

**黑马视屏 p52 6:50开始讲解内存**[Java入门基础视频教程，java零基础自学首选黑马程序员Java入门教程（含Java项目和Java真题）_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Cv411372m?p=52&spm_id_from=pageDriver)

![内存](.\img\内存.png)

**当一个数组赋值给另一个数组时，传递的是数组的地址，而不是值，更改前者的值，后者的值也会随之改变**

![内存2](.\img\内存2.png)

# 6.Debug

![Debug](.\img\Debug.png)

# 7.方法

## 1.方法的优点

1.提高程序的复用性和开发效率

2.让程序逻辑更清晰

## 2.方法的定义格式

![方法定义格式](.\img\方法定义格式.png)

![方法例子](.\img\方法例子.png)

调用方法: **方法名(参数列表);**

![方法调用](.\img\方法调用.png)

rs = 300



方法若不需要返回值，定义类型为void类型

## 3.方法的常见问题

1.方法定义顺序无所谓

2.方法和方法是平级关系，无法嵌套

3.若方法为void类型，则不能返回数据

4.return的返回值类型必须和方法定义的返回值一致，否则会报错！

5.return语句下面不能写代码，因为永远执行不到，同时也会报错

6.有返回值的方法可以直接用变量接受，或者输出，甚至直接调用

7.无返回值的方法不可以接收，否则会报错

## 4.方法的内存的调用

![方法内存销毁](.\img\方法内存销毁.png)

黑马讲义：p58 6:00 [Java入门基础视频教程，java零基础自学首选黑马程序员Java入门教程（含Java项目和Java真题）_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Cv411372m?p=58)

方法运行区域:**栈内存**

## 5.方法的参数传递机制

### 1.基本数据类型的传递

![基本数据类型传递](.\img\基本数据类型传递.png)

**当传递类型为基本数据类型时，实参传递的是实参本身的值**

输出 10，20，10

### 2.引用类型的传递

![引用数据类型传递](.\img\引用数据类型传递.png)

**当传递类型为引用数据类型时，实参传递的是实参地址**

输出 20，222，222

## 6.方法重载

### 1.概念

在同一个类中，**多个方法的名称相同，但是形参列表不同** ，那么这些方法就是方法重载（**修饰符，返回值，形参变量名无所谓**）

![方法重载](.\img\方法重载.png)

### 2.优点

代码可读性好

### 3.return语句

return语句可以**立即跳出并结束当前方法的执行**，return可以**放在任何方法中**

**break、return、continue的区别**

break：跳出并结束当前循环

return：跳出并结束当前方法的执行

continue：结束当前循环的本轮执行，进行下一次执行

# 8.面向对象（object oriented project）

## 1.设计类

![设计类](.\img\设计类.png)

## 2.创建对象

![创建对象](.\img\创建对象.png)

## 3.拿对象信息

![拿对象](.\img\拿对象.png)

## 4.定义类的注意事项

1.类名大写，满足驼峰式和标识符命名规则

2.一个Java文件中可以创建多个类，但是只能有一个类是public修饰的，而且public修饰的类名必须成为文件名，**实际开发中建议一个文件定义一个类**

3.成员变量的完成格式是：修饰符 数据类型 变量名称 = 初始化值；没有初始化的变量，一般有默认值（满足上面的默认值）

## 5.对象在内存中的运行机制

### 1.对象的内存图

黑马p72 [Java入门基础视频教程，java零基础自学首选黑马程序员Java入门教程（含Java项目和Java真题）_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Cv411372m?p=72&spm_id_from=pageDriver)

![对象内存执行机制](.\img\对象内存执行机制.png)

c1 接受的是地址

c1.name ===> 在c1地址中寻找name的值

c1.start() ===>在c1存放的堆地址中寻找方法的地址，然后再到方法区里面调用

.....

c2 接受的也是地址

c2.name ===> 在c2地址中寻找name的值

c2.start() ===>在c2存放的堆地址中寻找方法的地址，然后再到方法区里面调用

.....

### 2.两个对象指向同一个内存区域

![两个对象指向同一个内存](.\img\两个对象指向同一个内存.png)

s1.name == s2.name

s1.sex == s2.sex

s1.study() == s2.study()

......

**因为s1的地址和s2的地址是一样的，所以他们输出的值一模一样，跟数组相同**

### 3.Java内存自动清理

![Java内存清理](.\img\Java内存清理.png)

## 6.构造器

### 1.构造器的基本格式

![构造器的基本格式](.\img\构造器的基本格式.png)

#### 1.构造器的作用

初始化类的对象，并返回对象的地址

#### 2.构造器的种类及作用

##### 1.无参构造器

初始化对象时，成员变量的数据均采用默认值

##### 2.有参构造器

在初始化对象时，同时可以接收参数为对象进行赋值

##### 3.注意事项

1.任何类定义出来，无参构造器你写不写都存在

2.但是如果写了有参构造器，还想用无参，就要自己写一个无参构造器

### 2.this关键字

#### 1.概念

代表当前对象的地址

#### 2.作用

可以用于指定当前类中的成员变量、成员方法

## 7.封装

面向对象的三大特征之一：**封装**，继承，多态

### 1.什么是封装

对象代表什么，就得封装对应的数据，并提供数据对应的行为

### 2.封装的好处

让编程变得简单，有什么事，找对象，掉方法就好了

### 3.封装getter和setter方法即构造方法

![构造器方法](.\img\构造器方法.png)

![构造器的所有方法](.\img\构造器的所有方法.png)

### 4.JavaBean要求

![JavaBean要求](.\img\JavaBean要求.png)

### 5.成员变量和局部变量的区别

![成员变量和局部变量的区别](.\img\成员变量和局部变量的区别.png)

# 9.常用API(String，ArrayList)

**API:应用程序编程接口**

## 1.String类

java.lang包是java默认加载的包

java.lang.String 包类

### 1.String类的特点

String常被称为不可变字符串类型，它的**对象在创建之后就不能更改**

![字符串不可改变](.\img\字符串不可改变.png)

String类型的变量每次只是指向了不同的地址，而本身的值并没有改变

![String创建方法](.\img\String创建方法.png)

```java
//方式1
String s1 = new String();
System.out.println(s1);//==>""
//方式2
String s2 = new String("LKSJFALK");
System.out.println(s2);//==>"LKSJFALK"
//方式3
char[] c = {'a','b','c','d'};
String s3 = new String(c);
System.out.println(s3);//==>"abcd"
//方式4
byte[] b = {97,65};
String s4 = new String(b);
System.out.println(s4);//==>"aA"
```

### 2.常量池和堆内存比较

![常量池和堆内存比较](.\img\常量池和堆内存比较.png)

因为“abc”创建在常量池里面，常量池里面相同的数据只会创建一份，所以s1 == s2

s3 ！= s4 因为创建在堆内存里面，s3和s4存储的是地址

![常量对比](.\img\常量对比.png)

![堆内存比较](.\img\堆内存比较.png)

![比较总结](.\img\比较总结.png)

### 3.面试题

![String面试题](.\img\String面试题.png)

### 2.String类型比较

![字符串比较](.\img\字符串比较.png)

```java
 String s1 = "abc";
 String s2 = "abC";
//比较地址
 System.out.println(s1 == s2);//false
 //比较是否相同
 System.out.println(s1.equals(s2));//false
 //忽略大小写
 System.out.println(s1.equalsIgnoreCase(s2));//true
```

**字符串比较不能使用"==",使用"=="比较的是两个字符串的地址**

### 3.String常用API

![String常用API](.\img\String常用API.png)

```java
String s = "123456";
//字符串长度
System.out.println(s.length());//==>6
//获取某个索引位置的字符
System.out.println(s.charAt(0));//==>1
//将字符串转换为字符数组返回
char[] c = s.toCharArray();
for (int i = 0; i < c.length; i++) {
    System.out.print(c[i]);
}
System.out.println();//==>123456
//截取字符串 从  索引开始位置  取 索引结束位置 如果索引结束位置大于索引长度，会报错
String s2 = s.substring(0, 2);//代表索引0开始取到索引2，不包括索引2
System.out.println(s2);//==>12
//截取字符串 从  开始位置  取到最后
String s3 = s.substring(0);
System.out.println(s3);//==>123456
//替换字符串
String s4 = s.replace("123","***");
System.out.println(s4);//==>***456
//是否包含字符串
System.out.println(s.contains("123"));//==>true
//是否以 字符串 开始
System.out.println(s.startsWith("123"));//==>true
//分割字符串
String[] s5 = s.split("3");
System.out.println(Arrays.toString(s5));//==>[12,456]
```

## 2.ArrayList集合

### 1.集合和数组的区别

1.数组类型确定，长度固定，适合元素确定，功能单一

2.集合大小不固定，类型也可以不固定，适合元素不确定，适合增删改查，由很多丰富的功能

### 2.添加方法

![ArrayList添加方法](.\img\ArrayList添加方法.png)

```java
ArrayList a = new ArrayList();
a.add(1);
a.add(2);
boolean r = a.add(3);//会返回一个布尔值，是否添加成功
System.out.println(r);//true
//在索引值为1的地方添加一个元素2
a.add(1,2);
System.out.println(a);//==>[1, 2, 2, 3]
```

![ArrayList创建](.\img\ArrayList创建.png)

```java
 ArrayList<String> a = new ArrayList<可以省略不写>();//JDK1.7以后支持不写
        a.add("13");
        a.add("15");
        a.add("15lajkshn");
//        a.add(123)//会报错，只能添加String类型的数据
```

### 3.常用API

![ArrayList常用API](.\img\ArrayList常用API.png)

```java
ArrayList<String> a = new ArrayList();
a.add("13");
a.add("15");
a.add("asdf");
a.add("ahr");
a.add("grthr");
//获取索引值为x的元素
System.out.println(a.get(1));
//获取元素个数
System.out.println(a.size());
//删除索引值为x的元素,返回被删除的值
String s = a.remove(1);
System.out.println(s);
//删除索引值为x的元素,删除成功true,否者为false
boolean b = a.remove("13");
System.out.println(b);//如果列表里有两个相同的值，默认删除前面一个元素
//设置索引位置为x的元素的值，返回原来被修改的值
String s1 = a.set(0,"777");
System.out.println(s1);//==>asdf
```

# 10.static关键字

static就是静态的意思

被static修饰的变量在内存中只存储一份， 可以被共享、修改

## 1.static访问

![static访问](.\img\static访问.png)

 

![static访问2](.\img\static访问2.png)

**同一个类中访问静态成员变量，可以省略类名**

定义情况，当变量需要被共享时定义，一般是在线人数之类的

## 2.static修饰成员变量的内存原理

![static内存](.\img\static内存.png)

如果用**对象访问成员变量要中转两次**，而**类名访问成员变量只需要中转一次**，所以系统更推荐后者

## 3.static修饰成员方法的基本用法

![方法的区别](.\img\方法的区别.png)

![定义方法](.\img\定义方法.png)

![static访问3](.\img\static访问3.png)

## 4.static内存调用

15：00[Java入门基础视频教程，java零基础自学首选黑马程序员Java入门教程（含Java项目和Java真题）_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Cv411372m?p=96)

![static内存访问机制](.\img\static内存访问机制.png)

## 5.static的注意事项

![static的注意事项](.\img\static的注意事项.png)

![static注意事项1](.\img\static注意事项1.png)

## 6.static工具类

工具类里面全是静态方法,每一个方法完成一个功能，方便别人调用，一次编写，处处可用

由于工具类无需向外面创建实例对象，所以把构造器私有化

```java
private Tool(){

}
```

## 7.代码块

代码块是类的五大成分之一（成员变量、构造器、方法、代码块、内部类）

### 1.static代码块

静态代码块

格式：

```java
static{

}
```

特点：需要static关键字修饰，随着类的加载而加载，并且自动触发，**只执行一次**

### 2.构造代码块

格式：

```java
{}
```

特点：**每次创建对象**，调用构造器时，都会执行改代码块中的代码，并且在构造器之前执行

## 8.static单例设计模式

### 1.设计模式

在解决方法的一种模式，称为设计模式

### 2.单例模式

永远只**创建一个实例对象的设计模式**，叫做单例模式

#### 1.饿汉模式

![饿汉单例](.\img\饿汉单例.png)

**不管定义多少次，只会创建一个类**

```java
public class SingleInstance {    
    //构建一个向外可以访问的变量    
    public static SingleInstance singleInstance = new SingleInstance();    
    //必须私有构造器
    private SingleInstance(){}
}
```

调用

```java
SingleInstance s = SingleInstance.singleInstance;
```

#### 2.懒汉单例

![懒汉单例设计模式](.\img\懒汉单例设计模式.png)

```java
public class SingleInstance {    
    private static SingleInstance singleInstance;        
    public static SingleInstance getInstance(){        
        //如果第一次调用该方法        
        if(singleInstance == null){singleInstance = new SingleInstance();}        
        return singleInstance;    
    }    
    private SingleInstance(){  }
}
```

调用

```java
SingleInstance s = SingleInstance.getInstance();
```

# 11.继承

## 1.什么是继承

java中使用extends关键字，让一个类和另外一个类建立起一种父子关系

## 2.继承的好处

提高代码的复用性，减少代码冗余，增强类的功能扩展性

## 3.继承的格式

子类 extends 父类

## 4.继承后的特点

子类继承父类，子类可以得到父类的属性和行为，子类可以使用

## 5.继承的设计规范

子类们的相同特征放在父类的定义中，子类的独有属性和行为应该定义在子类里面

## 6.继承的内存空间

![子类和父类是在一个地址空间里](.\img\子类和父类是在一个地址空间里.png)

## 7.继承的特点

1.子类可以继承父类的属性和行为，但是子类不能继承父类的构造器

2.java是单继承模式：一个类只能继承一个直接父类

3.Java不支持多继承，但是支持多层继承（**如果出现父类跟祖宗类的方法重名，就近原则，使用父类的**）

4.java中所有的类都是继承object类（**祖宗类**）

5.子类是可以继承父类中的私有方法的，只是不能直接访问

6.子类没有继承静态成员的这种说法，因为静态成员只有一份，因此只能叫做共享

## 8.继承后访问成员变量、成员方法的访问

满足一个原则：**就近原则**

1.先在子类局部范围里面查找

2.子类成员范围里面查找

3.然后在父类里面查找，如果在父类中没有找到就会报错

## 9.方法重写

### 1.重写特点

当子类需要父类中的功能，但是父类又不能满足子类需要的需求，就需要重写

### 2.@override关键字（重写关键字）

1.加上该关键字后，方法必须是正确重写的，否则会报错

2.提高程序的可读性

### 3.重写注意事项

1.重写的名称，形参变量必须与被重写的方法的名称，形参变量一致

2.**私有方法不能被重写**

3.子类重写父类方法时，访问权限必须大于或者等于父类方法的权限（默认<protected<public）

4.子类不能重写父类的静态方法，会报错

## 10.继承后子类构造器的特点

1.**子类**的全部构造器默认会**先访问父类的无参构造器**在执行自己

2.**子类**构造器**第一句**代码**默认是super()**，不写也存在

## 11.子类构造器访问父类有参构造器

![super传值](.\img\super传值.png)

**如果父类没有无参构造器，则子类无参构造器调用就会报错**

![父类没有无参构造器](.\img\父类没有无参构造器.png)

## 12.this关键字和super关键字的使用总结

![this和super总结](.\img\this和super总结.png)

![this构造器](.\img\this构造器.png)

this()和super()两者只能存在于一个构造器中，而且都是在构造器的第一行

# 12.包

## 1.包的语法格式：

**package 公司域名倒写.技术名称**

相同包下的类可以直接访问，不同包下的类需要导入

## 2.导包的语法：

**import 包名.类名；**

当**两个不同的包下的类名**相同时，第二个类名只能用**全名访问**

![相同的包名](.\img\相同的包名.png)

# 13.权限修饰符

1.定义：是用来控制一个成员能够被访问的范围

2.权限修饰符的分类和作用范围

从大到小：（private -> 缺省(包访问权限) -> protected -> public）

![权限范围](.\img\权限范围.png)

# 14.final

final关键字是最终的意思

被修饰的**类**：该类为最终类 ，不能被继承

被修饰的**方法**：该方法为最终方法，不能够被重写

被修饰的**变量**：该变量被第一次赋值以后，不能被再次赋值（有且仅能被赋值一次）

 变量主要分为两种：

1.**局部变量**

2.**成员变量**

1. 实例成员变量
2. 静态成员变量

final的注意事项

![final注意事项](.\img\final注意事项.png)

# 15.常量

概念：使用public static final 修饰的成员变量被称为常量，必须有初始值，执行中其值不可改变

命名一般是由大写字母，多个单词之间使用（ _ ）来间隔

常量在编译阶段会被替换成字面量，方便维护，提高程序可读性

# 16.枚举

枚举就是java中的一种特殊类型，**为了做信息的标识和分类**

![枚举定义](.\img\枚举定义.png)

### 1.枚举的特点

![枚举的特点](.\img\枚举的特点.png)

### 2.枚举的优点

代码的可读性好，是最好的信息分类技术

# 17.抽象类

![抽象类](.\img\抽象类.png)

注意事项：

1.抽象方法只有方法签名，不能声明方法体

2.一个类中如果定义了抽象方法，就必须将类必须声明成抽象类，否则会报错

3.子类继承了父类抽象方法，则子类必须**重写抽象方法**或则把自己也**定义为抽象类**，否则会报错

4.抽象类里面不一定有抽象方法，有抽象方法的一定是抽象类

5.不能用abstract修饰变量、代码块、构造器

6.**得到了抽象方法，失去了创建对象的能力**（锁死，不能改变）

# 18.final和abstract关系

**互斥关系**

1.abstract定义的抽象类作为模板让子类继承，而final修饰的类不能被继承

2.抽象方法必须重写，而final修饰的方法不允许重写

# 19.模板方法

**优点：提高代码的复用性**

![模板方法](.\img\模板方法.png)

一般会在模板方法前面写**final修饰**，防止别人修改

# 20.接口

![接口定义方法](.\img\接口定义方法.png)

## 1.特点

在JDK1.8之前，接口中只能存在**常量**和**抽象方法**

接口就是一种规范

由于接口体现规范思想，规范默认都是公开的，所以代码层面

方法中：**public abstract可以省略不写**

常量：**public static final可以省略不写**

## 2.实现接口

![实现接口](.\img\实现接口.png)

**接口可以被类单实现，也可以被多个类实现**

如果一个类继承了接口，就要重写所有方法，否则这个类需要被定义成抽象类

## 3.JDK1.8开始接口新增的方法

![接口JDK1.8新增方法](.\img\接口JDK1.8新增方法.png)



## 4.接口的注意事项

![接口的注意事项](.\img\接口的注意事项.png)

# 21.类和接口的继承关系

1.类和类之间的关系：只能单继承

2.类和接口的关系：一个类可以继承多个类

3.接口和接口之间的关系：多继承，一个接口可以同时继承多个接口

# 22.多态(polymorphic)

## 1.多态的定义形式

![多态的形式](.\img\多态的形式.png)

```java
public class Test {   
    public static void main(String[] args) {        
        Animal d = new Dog();        
        d.run();//==>子类方法        
        System.out.println(d.name);//==>父类    
    }
}
```

```java
public class Dog extends Animal{    
    public String name = "子类";    
    public void run(){        
        System.out.println("子类方法");    
    }
}
```

```java
public class Animal {   
    public String name = "父类";    
    public void run(){        
        System.out.println("父类方法");    
    }
}
```

![多态的访问特点](.\img\多态的访问特点.png)

## 2.多态的优点

![多态的优点](.\img\多态的优点.png)

## 3.多态的缺点

不能访问子类中的独有功能

## 4.类型转换

### 1.自动类型转换（子类转父类）

```java
public class Test {    
    public static void main(String[] args) {        
        Animal d = new Dog();    
    }
}
```

### 2.强制类型转换（父类转子类）

```java
public class Test {
	public static void main(String[] args) {        
		Animal d = new Dog();       
		Dog dog = (Dog)d;    
	}
}
```

# 23.内部类

![内部类](.\img\内部类.png)

## 1.静态内部类

![静态内部类](.\img\静态内部类.png)

**静态内部类中可以访问外部类的静态成员**

**静态内部类中不可以直接访问外部类的实例成员**

##  2.成员内部类

![成员内部类](.\img\成员内部类.png)

![成员内部类的访问拓展](.\img\成员内部类的访问拓展.png)

![成员内部类面试题](.\img\成员内部类面试题.png)

成员内部类中访问所在外部类对象，格式：**外部类名.this**

## 3.局部内部类

![局部内部类](.\img\局部内部类.png)

## 4.匿名内部类

![匿名内部类](.\img\匿名内部类.png)

# 24.常用API

## 1.object

**所有类的祖宗类**

![object](.\img\object.png)

### 1.toString

toString()默认是返回对象的地址，其作用是让子类重写，以便返回对象的内容

```java
@Override
public String toString() {    
    return "Dog{" +            
        "name='" + 
        name + '\'' +            
        '}';
}
```

### 2.equals

equals()默认是比较两个对象的地址，其作用是让子类重写，以便比较对象中的值

```java
@Override
public boolean equals(Object o) {    
    if (this == o) return true;    
    if (o == null || getClass() != o.getClass()) return false;    
    Dog dog = (Dog) o;    
    return Objects.equals(name, dog.name);
}
```

## 2.objects

![objects](.\img\objects.png)

## 3.StringBuilder

![StringBuilder](.\img\StringBuilder.png)

StringBuilder支持链式编程

### 1.String底层拼接字符串

![String拼接字符串](.\img\String拼接字符串.png)

### 2.为什么选择StringBuilder拼接字符串

![StringBuilder拼接字符串](.\img\StringBuilder拼接字符串.png)

因为底层只会创建一个StringBuilder来拼接字符串，会比String拼接快的多，所以拼接字符串推荐使用StringBuilder

### 3.String和StringBuilder作比较

![String与StringBuilder作比较](.\img\String与StringBuilder作比较.png)

## 4.Math类

**Math成员里面的方法都是静态的，直接调用即可**

![Math](.\img\Math.png)

## 5.System类

![System](.\img\System.png)

**时间起始时间为1970年1月1日，c语言的生日** 1s == 1000ms

## 6.BigDecimal类

解决浮点型数据精度失真问题

![BigDecimal](.\img\BigDecimal.png)

建议定义方法

```java
BigDecimal b = BigDecimal.valueOf(变量值);
BigDecimal a1 = BigDecimal.valueOf(a);
BigDecimal b1 = BigDecimal.valueOf(b);
BigDecimal c1 = a1.add(b1);
BigDecimal c1 = a1.subtract(b1);
BigDecimal c1 = a1.multiply(b1);
BigDecimal c1 = a1.divide(b1);
// 注意事项：BigDecimal是一定要精度运算的
BigDecimal a11 = BigDecimal.valueOf(10.0);
BigDecimal b11 = BigDecimal.valueOf(3.0);
/**参数一：除数 
参数二：保留小数位数  
参数三：舍入模式*/
BigDecimal c11 = a11.divide(b11, 2, RoundingMode.HALF_UP); // 3.3333333333      
```

![BigDecimal解决问题](.\img\BigDecimal解决问题.png)

# 25.时间与日期

属于java.ulit类

## 1.Date

![Date](.\img\Date.png)

```java
// 1、创建一个Date类的对象：代表系统此刻日期时间对象        
Date d = new Date();        
System.out.println(d);        
// 2、获取时间毫秒值        
long time = d.getTime();        
System.out.println(time);        
long time1 = System.currentTimeMillis();        
System.out.println(time1);
```

![DateAPI](.\img\DateAPI.png)

```java
// 1、得到当前时间
Date d1 = new Date();
System.out.println(d1);
// 2、当前时间往后走 1小时  121s
long time2 = System.currentTimeMillis();
time2 += (60 * 60 + 121) * 1000;
// 3、把时间毫秒值转换成对应的日期对象。
//方法1
Date d2 = new Date(time2);
System.out.println(d2);
//方法2
Date d3 = new Date();
d3.setTime(time2);
System.out.println(d3);
```

## 2.SimpleDateFormat

![SimpleDateFormat](.\img\SimpleDateFormat.png)

![SimpleDateFormatAPI](.\img\SimpleDateFormatAPI.png)

![SimpleDateFormat格式化形式](.\img\SimpleDateFormat格式化形式.png)

```java
// 1、日期对象
Date d = new Date();
System.out.println(d);
// 2、格式化这个日期对象 (指定最终格式化的形式)
SimpleDateFormat sdf = new SimpleDateFormat("yyyy年MM月dd日 HH:mm:ss EEE a");
// 3、开始格式化日期对象成为喜欢的字符串形式
String rs = sdf.format(d);
System.out.println(rs);
System.out.println("----------------------------");
// 4、格式化时间毫秒值
// 需求：请问121秒后的时间是多少
long time1 = System.currentTimeMillis() + 121 * 1000;
String rs2 = sdf.format(time1);
System.out.println(rs2);
```

![SimpleDateFormat解析时间](.\img\SimpleDateFormat解析时间.png)

```java
// 目标: 学会使用SimpleDateFormat解析字符串时间成为日期对象。
// 有一个时间 2021年08月06日 11:11:11 往后 2天 14小时 49分 06秒后的时间是多少。
// 1、把字符串时间拿到程序中来
String dateStr = "2021年08月06日 11:11:11";
// 2、把字符串时间解析成日期对象（本节的重点）:形式必须与被解析时间的形式完全一样，否则运行时解析报错！
SimpleDateFormat sdf = new SimpleDateFormat("yyyy年MM月dd日 HH:mm:ss");
Date d = sdf.parse(dateStr);
// 3、往后走2天 14小时 49分 06秒
long time = d.getTime() + (2L*24*60*60 + 14*60*60 + 49*60 + 6) * 1000;
// 4、格式化这个时间毫秒值就是结果
System.out.println(sdf.format(time));
```

## 3.calendar

**抽象类，不能创建**

![calendar](.\img\calendar.png)

```java
Calendar c = Calendar.getInstance();
```

![calendar常用API](.\img\calendar常用API.png)

**calendar是可变日期对象，一旦更改其本身时间会发生变化**

```java
// 1、拿到系统此刻日历对象
Calendar cal = Calendar.getInstance();
System.out.println(cal);
// 2、获取日历的信息:public int get(int field)：取日期中的某个字段信息。
int year = cal.get(Calendar.YEAR);
System.out.println(year);
int mm = cal.get(Calendar.MONTH) + 1;
System.out.println(mm);
int days = cal.get(Calendar.DAY_OF_YEAR) ;
System.out.println(days);
// 3、public void set(int field,int value)：修改日历的某个字段信息。
 cal.set(Calendar.HOUR , 12);
 System.out.println(cal);
// 4.public void add(int field,int amount)：为某个字段增加/减少指定的值
// 请问64天后是什么时间
cal.add(Calendar.DAY_OF_YEAR , 64);
cal.add(Calendar.MINUTE , 59);
//  5.public final Date getTime(): 拿到此刻日期对象。
Date d = cal.getTime();
System.out.println(d);
//  6.public long getTimeInMillis(): 拿到此刻时间毫秒值
long time = cal.getTimeInMillis();
System.out.println(time);
```

## 4.JDK8新增日期时间对象

![JDK8新增日期时间对象](.\img\JDK8新增日期时间对象.png)

### 1.LocalDate、LocalTime、LocalDateTime

![新增日期时间1](.\img\新增日期时间1.png)

![LocalDateTime](.\img\LocalDateTime.png)

所以我们一般使用LoaclDateTime对象

```java
// 日期 时间
LocalDateTime nowDateTime = LocalDateTime.now();
System.out.println("今天是：" + nowDateTime);
//今天是：
System.out.println(nowDateTime.getYear());
//年
System.out.println(nowDateTime.getMonthValue());
//月
System.out.println(nowDateTime.getDayOfMonth());
//日
System.out.println(nowDateTime.getHour());
//时
System.out.println(nowDateTime.getMinute());
//分
System.out.println(nowDateTime.getSecond());
//秒
System.out.println(nowDateTime.getNano());
//纳秒//日：当年的第几天
System.out.println("dayOfYear：" + nowDateTime.getDayOfYear());//dayOfYear：249
//星期
System.out.println(nowDateTime.getDayOfWeek());
//THURSDAYSystem.out.println(nowDateTime.getDayOfWeek().getValue());//4
//月份
System.out.println(nowDateTime.getMonth());
SEPTEMBERSystem.out.println(nowDateTime.getMonth().getValue());//9
LocalDate ld = nowDateTime.toLocalDate();
System.out.println(ld);
LocalTime lt=nowDateTime.toLocalTime();
System.out.println(lt.getHour());System.out.println(lt.getMinute());System.out.println(lt.getSecond());
```

### 2.LocalDateTime使用

![LocalDateTimeAPI](.\img\LocalDateTimeAPI.png)

```java
LocalTime nowTime = LocalTime.now();
System.out.println(nowTime);//当前时间
System.out.println(nowTime.minusHours(1));//一小时前
System.out.println(nowTime.minusMinutes(1));//一分钟前
System.out.println(nowTime.minusSeconds(1));//一秒前
System.out.println(nowTime.minusNanos(1));//一纳秒前
System.out.println("----------------");
System.out.println(nowTime.plusHours(1));//一小时后
System.out.println(nowTime.plusMinutes(1));//一分钟后
System.out.println(nowTime.plusSeconds(1));//一秒后
System.out.println(nowTime.plusNanos(1));//一纳秒后
System.out.println("------------------");
// 不可变对象，每次修改产生新对象！
System.out.println(nowTime);
System.out.println("---------------");
LocalDate myDate = LocalDate.of(2018, 9, 5);
LocalDate nowDate = LocalDate.now();
System.out.println("今天是2018-09-06吗？ " + nowDate.equals(myDate));//今天是2018-09-06吗？ false
System.out.println(myDate + "是否在" + nowDate + "之前？ " + myDate.isBefore(nowDate));//2018-09-05是否在2018-09-06之前？ true
System.out.println(myDate + "是否在" + nowDate + "之后？ " + myDate.isAfter(nowDate));//2018-09-05是否在2018-09-06之后？ false
System.out.println("---------------------------");
// 判断今天是否是你的生日
LocalDate birDate = LocalDate.of(1996, 8, 5);
LocalDate nowDate1 = LocalDate.now();
MonthDay birMd = MonthDay.of(birDate.getMonthValue(), birDate.getDayOfMonth());
MonthDay nowMd = MonthDay.from(nowDate1);
System.out.println("今天是你的生日吗？ " + birMd.equals(nowMd));//今天是你的生日吗？ false
```

### 3.instant

![instant](.\img\instant.png)

```java
// 1、得到一个Instant时间戳对象
Instant instant = Instant.now();
System.out.println(instant);
// 2、系统此刻的时间戳怎么办？
Instant instant1 = Instant.now();
System.out.println(instant1.atZone(ZoneId.systemDefault()));
// 3、如何去返回Date对象
Date date = Date.from(instant);
System.out.println(date);
Instant i2 = date.toInstant();
System.out.println(i2);
```

### 4.DateTimeFormatter

![DateTimeFormatter](.\img\DateTimeFormatter.png)

```java
// 本地此刻  日期时间 对象
LocalDateTime ldt = LocalDateTime.now();
System.out.println(ldt);// 解析/格式化器
DateTimeFormatter dtf = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss EEE a");// 正向格式化
System.out.println(dtf.format(ldt));
// 逆向格式化
System.out.println(ldt.format(dtf));
// 解析字符串时间
DateTimeFormatter dtf1 = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");
// 解析当前字符串时间成为本地日期时间对象
LocalDateTime ldt1 = LocalDateTime.parse("2019-11-11 11:11:11" ,  dtf1);
System.out.println(ldt1);System.out.println(ldt1.getDayOfYear());
```

### 5.计算两个时间之间的差别和两个日期之间的差别

#### 1.period

![period](.\img\period.png)

```java
// 当前本地 年月日
LocalDate today = LocalDate.now();
System.out.println(today);
// 生日的 年月日
LocalDate birthDate = LocalDate.of(1998, 10, 13);
System.out.println(birthDate);
Period period = Period.between(birthDate, today);
//第二个参数减第一个参数
System.out.println(period.getYears());
System.out.println(period.getMonths());
System.out.println(period.getDays());
```

#### 2.duration

![duration](.\img\duration.png)

```java
// 本地日期时间对象。
LocalDateTime today = LocalDateTime.now();
System.out.println(today);
// 出生的日期时间对象
LocalDateTime birthDate = LocalDateTime.of(2021,8,06,01,00,00);
System.out.println(birthDate);
Duration duration = Duration.between(   birthDate , today );//第二个参数减第一个参数
System.out.println(duration.toDays());//两个时间差的天数
System.out.println(duration.toHours());//两个时间差的小时数
System.out.println(duration.toMinutes());//两个时间差的分钟数
System.out.println(duration.toMillis());//两个时间差的毫秒数
System.out.println(duration.toNanos());//两个时间差的纳秒数
```

#### 3.**总结**

![period和duration的特点](.\img\period和duration的特点.png)

### 6.ChronoUnit

**比较两个日期时间最全的类**

```java
// 本地日期时间对象：此刻的
LocalDateTime today = LocalDateTime.now();
System.out.println(today);
// 生日时间
LocalDateTime birthDate = LocalDateTime.of(1990,10,1,10,50,59);
System.out.println(birthDate);
System.out.println("相差的年数：" + ChronoUnit.YEARS.between(birthDate, today));
System.out.println("相差的月数：" + ChronoUnit.MONTHS.between(birthDate, today));
System.out.println("相差的周数：" + ChronoUnit.WEEKS.between(birthDate, today));
System.out.println("相差的天数：" + ChronoUnit.DAYS.between(birthDate, today));
System.out.println("相差的时数：" + ChronoUnit.HOURS.between(birthDate, today));
System.out.println("相差的分数：" + ChronoUnit.MINUTES.between(birthDate, today));
System.out.println("相差的秒数：" + ChronoUnit.SECONDS.between(birthDate, today));
System.out.println("相差的毫秒数：" + ChronoUnit.MILLIS.between(birthDate, today));
System.out.println("相差的微秒数：" + ChronoUnit.MICROS.between(birthDate, today));
System.out.println("相差的纳秒数：" + ChronoUnit.NANOS.between(birthDate, today));
System.out.println("相差的半天数：" + ChronoUnit.HALF_DAYS.between(birthDate, today));
System.out.println("相差的十年数：" + ChronoUnit.DECADES.between(birthDate, today));
System.out.println("相差的世纪（百年）数：" + ChronoUnit.CENTURIES.between(birthDate, today));
System.out.println("相差的千年数：" + ChronoUnit.MILLENNIA.between(birthDate, today));
System.out.println("相差的纪元数：" + ChronoUnit.ERAS.between(birthDate, today));
```

## 5.包装类

![包装类](.\img\包装类.png)

#### 1.特点

**自动装箱**：基本数据类型的数据可以直接赋值给包装类型的变量

**自动拆箱**：包装类型的变量可以直接赋值给基本数据类型的变量

![包装类的特点](.\img\包装类的特点.png)

```java
int a = 10;       
Integer a1 = 11;        
Integer a2 = a; 
// 自动装箱        
System.out.println(a);       
System.out.println(a1);       
Integer it = 100;        
int it1 = it; 
// 自动拆箱        
System.out.println(it1);        
double db = 99.5;       
Double db2 = db; 
// 自动装箱了        
double db3 = db2; 
// 自动拆箱        
System.out.println(db3);        
// int age = null;
// 报错了！        
Integer age1 = null;        
Integer age2 = 0;        
System.out.println("-----------------");        
// 1、包装类可以把基本类型的数据转换成字符串形式。（没啥用）        
Integer i3 = 23;        
String rs = i3.toString();        
System.out.println(rs + 1);        
String rs1 = Integer.toString(i3);        
System.out.println(rs1 + 1);       
// 可以直接+字符串得到字符串类型        
String rs2 = i3 + "";       
System.out.println(rs2 + 1);        
System.out.println("-----------------");        
String number = "23";       
//转换成整数        
// int age = Integer.parseInt(number);        
int age = Integer.valueOf(number);        
System.out.println(age + 1);        
String number1 = "99.9";        
//转换成小数
//        double score = Double.parseDouble(number1);        
double score = Double.valueOf(number1);        
System.out.println(score + 0.1);
```

#### 2.总结

![包装类的总结](.\img\包装类的总结.png)

## 6.正则表达式（patternAPI）

### 1.匹配规则

![正则表达式](.\img\正则表达式.png)

```java
 //public boolean matches(String regex):判断是否与正则表达式匹配，匹配返回true
        // 只能是 a  b  c
        System.out.println("a".matches("[abc]")); // true
        System.out.println("z".matches("[abc]")); // false

        // 不能出现a  b  c
        System.out.println("a".matches("[^abc]")); // false
        System.out.println("z".matches("[^abc]")); // true

        System.out.println("a".matches("\\d")); // false
        System.out.println("3".matches("\\d")); // true
        System.out.println("333".matches("\\d")); // false
        System.out.println("z".matches("\\w")); // true
        System.out.println("2".matches("\\w")); // true
        System.out.println("21".matches("\\w")); // false
        System.out.println("你".matches("\\w")); //false
        System.out.println("你".matches("\\W")); // true
        System.out.println("---------------------------------");
        //  以上正则匹配只能校验单个字符。

        // 校验密码
        // 必须是数字 字母 下划线 至少 6位
        System.out.println("2442fsfsf".matches("\\w{6,}"));
        System.out.println("244f".matches("\\w{6,}"));

        // 验证码 必须是数字和字符  必须是4位
        System.out.println("23dF".matches("[a-zA-Z0-9]{4}"));
        System.out.println("23_F".matches("[a-zA-Z0-9]{4}"));
        System.out.println("23dF".matches("[\\w&&[^_]]{4}"));
        System.out.println("23_F".matches("[\\w&&[^_]]{4}"));
```

### 2.总结

![正则表达式总结](.\img\正则表达式总结.png)

### 3.正则表达式的API

![正则表达式的API](.\img\正则表达式的API.png)

```java
String names = "小路dhdfhdf342蓉儿43fdffdfbjdfaf小何";
String[] arrs = names.split("\\w+");
for (int i = 0; i < arrs.length; i++) {    
    System.out.println(arrs[i]);
}
//==>小路==>蓉儿==>小何
String names2 = names.replaceAll("\\w+", "  ");
System.out.println(names2);//==>小路  蓉儿  小何
```

### 4.爬取规则

```java
String rs = "来黑马程序学习Java,电话020-43422424，或者联系邮箱" +        "itcast@itcast.cn,电话18762832633，0203232323" +        "邮箱bozai@itcast.cn，400-100-3233 ，4001003232";
// 需求：从上面的内容中爬取出 电话号码和邮箱。
// 1、定义爬取规则，字符串形式
String regex = "(\\w{1,30}@[a-zA-Z0-9]{2,20}(\\.[a-zA-Z0-9]{2,20}){1,2})|(1[3-9]\\d{9})" +        "|(0\\d{2,6}-?\\d{5,20})|(400-?\\d{3,9}-?\\d{3,9})";
// 2、把这个爬取规则编译成匹配对象。
Pattern pattern = Pattern.compile(regex);
// 3、得到一个内容匹配器对象
Matcher matcher = pattern.matcher(rs);
// 4、开始找了
while (matcher.find()) {    
    String rs1 = matcher.group();    
    System.out.println(rs1);
}
```

## 7.Arrays类

![Arrays类](.\img\Arrays类.png)

### sort排序(默认是升序)

![sort排序](.\img\sort排序.png)

 

```java
Integer[] ages1 = {34, 12, 42, 23};        
/**           
参数一：被排序的数组 必须是引用类型的元素           
参数二：匿名内部类对象，代表了一个比较器对象。         
*/       
Arrays.sort(ages1, new Comparator<Integer>() {            
    @Override            
    public int compare(Integer o1, Integer o2) 
    {                
        // 指定比较规则。
        //if(o1 > o2){
        //    return 1;
        //}else if(o1 < o2){
        //    return -1;
        //}
        //return 0;                
        // return o1 - o2; // 默认升序                
        return o2 - o1; //  降序            
    }        
});        
System.out.println(Arrays.toString(ages1));
--------------------------------------------------------------------------------------------
Student[] students = new Student[3];        
students[0] = new Student("吴磊",23 , 175.5);        
students[1] = new Student("谢鑫",18 , 185.5);        
students[2] = new Student("王亮",20 , 195.5);        
System.out.println(Arrays.toString(students));        
// Arrays.sort(students);  
// 直接运行奔溃        
Arrays.sort(students, new Comparator<Student>() {            
    @Override            
    public int compare(Student o1, Student o2) {                
        // 自己指定比较规则                
        // return o1.getAge() - o2.getAge(); 
        // 按照年龄升序排序！                
        // return o2.getAge() - o1.getAge(); 
        // 按照年龄降序排序！！                
        // return Double.compare(o1.getHeight(), o2.getHeight()); 
        // 比较浮点型可以这样写 升序                
        return Double.compare(o2.getHeight(), o1.getHeight()); 
        // 比较浮点型可以这样写  降序            
    }        
}); 
System.out.println(Arrays.toString(students));
```

## 8.lambda表达式

### 1.初阶

**JDK1.8**以后才支持的语法

![lambda表达式](.\img\lambda表达式.png)

**@FunctionalInterface注解才可以简化**

```java
public class LambdaDemo2 {    
    public static void main(String[] args) {        
        // 目标：学会使用Lambda的标准格式简化匿名内部类的代码形式        
        // 注意：Lambda只能简化接口中只有一个抽象方法的匿名内部类形式（函数式接口）
        
        //方法一
        Swimming s1 = new Swimming() {
            @Override
            public void swim() {
                System.out.println("老师游泳贼溜~~~~~");
            }
        };
        //方式二
        Swimming s1 = () -> {
            System.out.println("老师游泳贼溜~~~~~");
        }; 
        //方法三
        Swimming s1 = () -> System.out.println("老师游泳贼溜~~~~~");  
        
        go(s1);   
        
        System.out.println("---------------------");
        
        //方式一
        go(new Swimming() {
            @Override
            public void swim() {
                System.out.println("学生游泳很开心~~~");
            }
        });
        //方法二
        go(() ->{
                System.out.println("学生游泳很开心~~~");
        });  
        //方法三
        go(() -> System.out.println("学生游泳很开心~~~"));    
    }    
    public static void go(Swimming s){        
        System.out.println("开始。。。");        
        s.swim();        
        System.out.println("结束。。。");    
    }
}
@FunctionalInterface // 一旦加上这个注解必须是函数式接口，里面只能有一个抽象方法
interface Swimming{    
    void swim();
}
```

![lambda](.\img\lambda.png)

![lambda总结](.\img\lambda总结.png)

###  2.进阶

![lambda进阶](.\img\lambda进阶.png)

```java
 Integer[] ages1 = {34, 12, 42, 23};
        /**
         参数一：被排序的数组 必须是引用类型的元素
         参数二：匿名内部类对象，代表了一个比较器对象。
         */
		//方法一
//        Arrays.sort(ages1, new Comparator<Integer>() {
//            @Override
//            public int compare(Integer o1, Integer o2) {
//                return o2 - o1; //  降序
//            }
//        });
		//方法二
//        Arrays.sort(ages1, (Integer o1, Integer o2) -> {
//                return o2 - o1; //  降序
//        });

		//方法三
//        Arrays.sort(ages1, ( o1,  o2) -> {
//            return o2 - o1; //  降序
//        });

        Arrays.sort(ages1, ( o1,  o2 ) ->  o2 - o1 );

        System.out.println(Arrays.toString(ages1));
```

# 26.集合

**数组和集合的特点**

**数组**：长度固定，定义后类型确定，可以存储基本数据类型和引用类型，适用于个数确定和类型确定的场景

**集合**：类型不固定，长度可以改变，只能存储引用类型，适用于个数不确定的场景，需要增删查改

**集合中存储的是对象的地址**

## 1.集合的体系

![集合的体系结构](.\img\集合的体系结构.png)

### 1.Collection

#### 1.Collection体系结构（单例集合）

![Collection体系结构](.\img\Collection体系结构.png)

```java
// 有序 可重复 有索引
Collection list = new ArrayList();
list.add("Java");
list.add("Java");
list.add("Mybatis");
list.add(23);
list.add(23);
list.add(false);
list.add(false);
System.out.println(list);
// 无序 不重复  无索引
Collection list1 = new HashSet();
list1.add("Java");
list1.add("Java");
list1.add("Mybatis");
list1.add(23);
list1.add(23);
list1.add(false);
list1.add(false);
System.out.println(list1);
```

#### 2.集合的定义规则

![集合的定义规则](.\img\集合的定义规则.png)

```java
// Collection<String> list2 = new ArrayList<String>();
Collection<String> list2 = new ArrayList<>(); 
// JDK 7开始之后后面类型申明可以不写
list2.add("Java");
// list2.add(23);
list2.add("黑马");
// 集合和泛型不支持基本数据类型，只能支持引用数据类型
// Collection<int> list3 = new ArrayList<>();
Collection<Integer> list3 = new ArrayList<>();
list3.add(23);
list3.add(233);
list3.add(2333);
Collection<Double> list4 = new ArrayList<>();
list4.add(23.4);
list4.add(233.0);
list4.add(233.3);
```

### 2.Collection常用API

![CollectionAPI](.\img\CollectionAPI.png)

```java
// HashSet:添加的元素是无序，不重复，无索引。
Collection<String> c = new ArrayList<>();
// 1.添加元素, 添加成功返回true。
c.add("Java");
c.add("HTML");
System.out.println(c.add("HTML"));
c.add("MySQL");
c.add("Java");
System.out.println(c.add("黑马"));
System.out.println(c); 
// [Java, HTML, HTML, MySQL, Java, 黑马]
// 2.清空集合的元素。
c.clear();
System.out.println(c);
// 3.判断集合是否为空 是空返回true,反之。
System.out.println(c.isEmpty());
// 4.获取集合的大小。
System.out.println(c.size());
// 5.判断集合中是否包含某个元素。
System.out.println(c.contains("Java"));  // true
System.out.println(c.contains("java")); // false
System.out.println(c.contains("黑马")); // true
// 6.删除某个元素:如果有多个重复元素默认删除前面的第一个！
System.out.println(c.remove("java")); // false
System.out.println(c);
System.out.println(c.remove("Java")); // true
System.out.println(c);
// 7.把集合转换成数组  [HTML, HTML, MySQL, Java, 黑马]
Object[] arrs = c.toArray();
System.out.println("数组：" + Arrays.toString(arrs));
System.out.println("----------------------拓展----------------------");
Collection<String> c1 = new ArrayList<>();
c1.add("java1");
c1.add("java2");
Collection<String> c2 = new ArrayList<>();
c2.add("赵敏");
c2.add("殷素素");
// addAll把c2集合的元素全部倒入到c1中去。
c1.addAll(c2);
System.out.println(c1);
System.out.println(c2);
```

#### 2.Collection集合的遍历方式

##### 1.迭代器

![迭代器遍历](.\img\迭代器遍历.png)

```java
ArrayList<String> lists = new ArrayList<>();        
lists.add("赵敏");        
lists.add("小昭");        
lists.add("素素");        
lists.add("灭绝");        
System.out.println(lists);        
// [赵敏, 小昭, 素素, 灭绝]        
//   it        
// 1、得到当前集合的迭代器对象。        
Iterator<String> it = lists.iterator();
String ele = it.next();
System.out.println(ele);
System.out.println(it.next());
System.out.println(it.next());
System.out.println(it.next());        
System.out.println(it.next()); 
// NoSuchElementException 出现无此元素异常的错误        
// 2、定义while循环        
while (it.hasNext()){            
    String ele = it.next();            
    System.out.println(ele);        
}
```

**迭代器注意事项**

![迭代器注意事项](.\img\迭代器注意事项.png)

##### 2.foreach/增强for循环

![增强for](.\img\增强for.png)

```java
Collection<String> lists = new ArrayList<>();        
lists.add("赵敏");        
lists.add("小昭");        
lists.add("殷素素");        
lists.add("周芷若");        
System.out.println(lists);        
// [赵敏, 小昭, 殷素素, 周芷若]        
//  ele        
for (String ele : lists) {            
    System.out.println(ele);        
}        
System.out.println("------------------");        
double[] scores = {100, 99.5 , 59.5};        
for (double score : scores) {            
    System.out.println(score);
    //            if(score == 59.5){
    //                score = 100.0; 
    // 修改无意义，不会影响数组的元素值。
    //            }        
}        
System.out.println(Arrays.toString(scores));
```

![增强for注意事项](.\img\增强for注意事项.png)

##### 3.lambda表达式

![lambda遍历](.\img\lambda遍历.png)

```java
Collection<String> lists = new ArrayList<>();        
lists.add("赵敏");        
lists.add("小昭");        
lists.add("殷素素");        
lists.add("周芷若");        
System.out.println(lists);        
// [赵敏, 小昭, 殷素素, 周芷若]        
//方式4      
lists.forEach(new Consumer<String>() {            
    @Override            
    public void accept(String s) {                
        System.out.println(s);            
    }        
});
//方式1
lists.forEach(s -> {
        System.out.println(s);
});   
//方式2
lists.forEach(s ->  System.out.println(s) );   
//方法3
lists.forEach(System.out::println );
```

# 27.常见的数据结构

数据结构就是计算机底层，组织数据的方式

## 1.栈

先进后出，后进先出

![栈](.\img\栈.png)

## 2.队列

![队列](.\img\队列.png)

## 3.数组

![数组](.\img\数组.png)

## 4.链表

### 1.特点

![链表的特点](.\img\链表的特点.png)

### 2.链表的种类

![链表的种类](.\img\链表的种类.png)

## 5.二叉树、二叉查找树

### 1.概述

![二叉树概述](.\img\二叉树概述.png)

### 2.特点

![二叉树的特点](.\img\二叉树的特点.png)

### 3.二叉树和二叉查找树

![二叉查找树](.\img\二叉查找树.png)

### 4.二叉查找树添加节点

![二叉查找树添加节点](.\img\二叉查找树添加节点.png)

## 6.平衡二叉树

### 1.概述

![平衡二叉树](.\img\平衡二叉树.png)

### 2.平衡二叉树的要求

![平衡二叉树的要求](.\img\平衡二叉树的要求.png)

### 3.二叉树变成平衡二叉树的条件

![二叉树变成平衡二叉树的条件](.\img\二叉树变成平衡二叉树的条件.png)

#### 1.左左

![左左1](.\img\左左1.png)

![左左2](.\img\左左2.png)

#### 2.左右

![左右1](.\img\左右1.png)

![左右2](.\img\左右2.png)

![左右3](.\img\左右3.png)

#### 3.右右

![右右1](.\img\右右1.png)

![右右2](.\img\右右2.png)

#### 4.右左

![右左1](.\img\右左1.png)

![右左2](.\img\右左2.png)

![右左3](.\img\右左3.png)

## 7.红黑树 

### 1.概述

![红黑树概述](.\img\红黑树概述.png)

### 2.红黑规则

![红黑规则](.\img\红黑规则.png)

### 3.添加规则

![添加节点](.\img\添加节点.png)

#### 1.默认黑色

![添加黑色](.\img\添加黑色.png)

#### 2.默认红色

![添加红色](.\img\添加红色.png)

**综上所述，红色效率更高**

### 4.红黑树小结

![红黑树小结](.\img\红黑树小结.png)

## 8.所有数据结构的小结

![数据结构的小结](.\img\数据结构的小结.png)

# 28.List集合

## 1.特点

![List集合的特点](.\img\List集合的特点.png)

## 2.List常用API

![List常用API](.\img\List常用API.png)

```java
// 1.创建一个ArrayList集合对象：
// List:有序，可重复，有索引的。
ArrayList<String> list = new ArrayList<>(); // 一行经典代码！
list.add("Java");
list.add("Java");
list.add("HTML");
list.add("HTML");
list.add("MySQL");
list.add("MySQL");

// 2.在某个索引位置插入元素。
list.add(2, "黑马");
System.out.println(list);

// 3.根据索引删除元素,返回被删除元素
System.out.println(list.remove(1));
System.out.println(list);

// 4.根据索引获取元素:public E get(int index):返回集合中指定位置的元素。
System.out.println(list.get(1));

// 5.修改索引位置处的元素: public E set(int index, E element)
System.out.println(list.set(1, "传智教育"));
System.out.println(list);
```

## 3.List集合小结

![List集合小结](.\img\List集合小结.png)

## 4.List集合的遍历模式

![List集合的遍历模式](.\img\List集合的遍历模式.png)

```java
List<String> lists = new ArrayList<>();
lists.add("java1");
lists.add("java2");
lists.add("java3");
/** （1）for循环。 */
System.out.println("-----------------------");
for (int i = 0; i < lists.size(); i++) {    
    String ele = lists.get(i);    
    System.out.println(ele);
}
/** （2）迭代器。 */
System.out.println("-----------------------");
Iterator<String> it = lists.iterator();
while (it.hasNext()){    
    String ele = it.next();    
    System.out.println(ele);
}
/** （3）foreach */
System.out.println("-----------------------");
for (String ele : lists) {    
    System.out.println(ele);
}
/** （4）JDK 1.8开始之后的Lambda表达式  */
System.out.println("-----------------------");
lists.forEach(s -> {    System.out.println(s);});
```

## 5.ArrayList的底层原理

![ArrayList的底层原理](.\img\ArrayList的底层原理.png)

每次超过了数组的长度，就会进行1.5倍的扩容

![ArrayList默认长度即扩容](.\img\ArrayList默认长度即扩容.png)

## 6.LinkedList集合的底层原理

![LinkedList的特点](.\img\LinkedList的特点.png)

```java
// LinkedList可以完成队列结构，和栈结构 （双链表）
// 1、做一个队列：
LinkedList<String> queue = new LinkedList<>();
// 入队
queue.addLast("1号");
queue.addLast("2号");
queue.addLast("3号");
System.out.println(queue);
// 出队
System.out.println(queue.getFirst());
System.out.println(queue.removeFirst());
System.out.println(queue.removeFirst());
System.out.println(queue);
// 2、做一个栈
LinkedList<String> stack = new LinkedList<>();
// 入栈 压栈 (push)
stack.push("第1颗子弹");
stack.push("第2颗子弹");
stack.push("第3颗子弹");
stack.push("第4颗子弹");
System.out.println(stack);
// 出栈  弹栈 (pop)
popSystem.out.println(stack.pop());
System.out.println(stack.pop());
System.out.println(stack.pop());
System.out.println(stack);
```

## 7.修改删除问题

![修改删除问题](.\img\修改删除问题.png)

```java
 // 1、准备数据        
ArrayList<String> list = new ArrayList<>();        
list.add("黑马");        
list.add("Java");        
list.add("Java");        
list.add("赵敏");        
list.add("赵敏");        
list.add("素素");        
System.out.println(list);        
// [黑马, Java, Java, 赵敏, 赵敏, 素素]        
//        it        
// 需求：删除全部的Java信息。       
// a、迭代器遍历删除        
Iterator<String> it = list.iterator();        
while (it.hasNext()){           
    String ele = it.next();           
    if("Java".equals(ele)){                
        // 删除Java                
        // list.remove(ele); 
        // 集合删除会出毛病                
        it.remove(); 
        // 删除迭代器所在位置的元素值（没毛病）           
    }        
}        
System.out.println(list);        
// b、foreach遍历删除 (会出现问题，这种无法解决的，foreach不能边遍历边删除，会出bug)
for (String s : list) {
    if("Java".equals(s)){
        list.remove(s);
    }
}        
 //c、lambda表达式(会出现问题，这种无法解决的，Lambda遍历不能边遍历边删除，会出bug)
list.forEach(s -> {
    if("Java".equals(s)){
        list.remove(s);
    }
});        
// d、for循环(边遍历边删除集合没毛病，但是必须从后面开始遍历删除才不会出现漏掉应该删除的元素)        
for (int i = list.size() - 1; i >= 0 ; i--) {            
    String ele = list.get(i);            
    if("Java".equals(ele)){                
        list.remove(ele);            
    }        
}        
System.out.println(list);
```

## 8.泛型深入

### 1.泛型的概述

![泛型深入](.\img\泛型深入.png)

![泛型定义](.\img\泛型定义.png)

### 2.自定义泛型类

![自定义泛型类](.\img\自定义泛型类.png)

![自定义泛型MyArrayList](.\img\自定义泛型MyArrayList.png)

**总结**

![泛型总结](.\img\泛型总结.png)

### 3.自定义泛型方法

![泛型方法](.\img\泛型方法.png)

```java
public static void main(String[] args) {    
    String[] names = {"小璐", "蓉容", "小何"};    
    printArray(names);    
    Integer[] ages = {10, 20, 30};    
    printArray(ages);    
    Integer[] ages2 = getArr(ages);    
    String[]  names2 = getArr(names);}
public static <T> T[] getArr(T[] arr){    
    return arr;
}
public static <T> void printArray(T[] arr){    
    if(arr != null){        
        StringBuilder sb = new StringBuilder("[");        
        for (int i = 0; i < arr.length; i++) {            
            sb.append(arr[i]).append(i == arr.length - 1 ? "" : ", ");        
        }        
        sb.append("]");        
        System.out.println(sb);    
    }else {        
        System.out.println(arr);    
    }
}
```

**总结**

![泛型方法的总结](.\img\泛型方法的总结.png)

### 4.自定义泛型接口

![自定义泛型接口](.\img\自定义泛型接口.png)

```java
public interface Data<E> {    
    void add(E e);    
    void delete(int id);    
    void update(E e);    
    E queryById(int id);
}
```

```java
public class StudentData implements Data<Student>{    
    @Override    
    public void add(Student student) {    
    }    
    @Override    
    public void delete(int id) {    
    }    
    @Override    
    public void update(Student student) {    
    }    
    @Override    
    public Student queryById(int id) {        
        return null;    
    }
}
```

**总结**

![自定义泛型接口的总结](.\img\自定义泛型接口的总结.png)

### 5.泛型的通配符

![泛型通配符](.\img\泛型通配符.png)

```java
public class GenericDemo {    
    public static void main(String[] args) {        
        ArrayList<BMW> bmws = new ArrayList<>();        
        bmws.add(new BMW());        
        bmws.add(new BMW());        
        bmws.add(new BMW());        
        go(bmws);        
        ArrayList<BENZ> benzs = new ArrayList<>();        
        benzs.add(new BENZ());        
        benzs.add(new BENZ());        
        benzs.add(new BENZ());        
        go(benzs);        
        ArrayList<Dog> dogs = new ArrayList<>();        
        dogs.add(new Dog());        
        dogs.add(new Dog());        
        dogs.add(new Dog());        
        // go(dogs);    
    }    
    /**       
    所有车比赛     
    */    
    public static void go(ArrayList<? extends Car> cars){    
    }
}
class Dog{}
class BENZ extends Car{}
class BMW extends Car{}
// 父类
class Car{}
```

# 29.Set集合

## 1.特点

![set集合特点](.\img\set集合特点.png)

```java
// 看看Set系列集合的特点： HashSet LinkedHashSet TreeSet
//Set<String> sets = new HashSet<>(); 
// 一行经典代码  无序不重复，无索引
// Set<String> sets = new LinkedHashSet<>(); 
// 有序  不重复 无索引sets.add("MySQL");
sets.add("MySQL");
sets.add("Java");
sets.add("Java");
sets.add("HTML");
sets.add("HTML");
sets.add("SpringBoot");
sets.add("SpringBoot");
System.out.println(sets);
```

## 2.总结

![set特点总结](.\img\set特点总结.png)

## 3.HashSet底层原理（哈希表）

### 1.哈希表的组成

![哈希表的组成](.\img\哈希表的组成.png)

### 2.哈希值

![哈希值](.\img\哈希值.png)

### 3.JDK1.7哈希表底层

![JDK1.7哈希表底层](.\img\JDK1.7哈希表底层.png)

### 4.JDK1.8哈希表底层

![JDK1.8哈希数底层](.\img\JDK1.8哈希数底层.png)

### 5.HashSet集合总结

![Set集合总结](.\img\Set集合总结.png)

![set结合总结2](.\img\set结合总结2.png)

### 6.HashSet去重复原理

![](.\img\HashSet去重复原理.png)

![去重复](.\img\去重复.png)

![重写hashcode](.\img\重写hashcode.png)

### 7.LinkedHashSet

![LinkedHashSet](.\img\LinkedHashSet.png)

![LinkedHashSet总结](.\img\LinkedHashSet总结.png)

### 8.TreeSet

#### 1.特点

![TreeSet](.\img\TreeSet.png)

![TreeSet默认规则](.\img\TreeSet默认规则.png)

#### 2.定义排序规则

![TreeSet比较排序](.\img\TreeSet比较排序.png)

![比较规则](.\img\比较规则.png)

##### 1.方式1

![比较方法1](.\img\比较方法1.png)

##### 2.方法2

```java
// 方式二：sort方法自带比较器对象        
Collections.sort(apples, new Comparator<Apple>() {            
    @Override            
    public int compare(Apple o1, Apple o2) {                
        return Double.compare(o1.getPrice() , o2.getPrice()); // 按照价格排序！！            
    }        
});
```

#### 3.总结

![TreeSet总结](.\img\TreeSet总结.png)

# 30.Collection集合的体系特点

![Collection集合的体系特点](.\img\Collection集合的体系特点.png)

# 31.可变参数

![可变参数](.\img\可变参数.png)

```java
public static void main(String[] args) {    
    sum(); 
    // 1、不传参数    
    sum(10); 
    // 2、可以传输一个参数    
    sum(10, 20, 30); 
    // 3、可以传输多个参数    
    sum(new int[]{10, 20, 30, 40, 50}); 
    // 4、可以传输一个数组}
    /**   
    注意：一个形参列表中只能有一个可变参数,可变参数必须放在形参列表的最后面 * 
    @param nums 
    */
    public static void sum(int...nums){    
        // 注意：可变参数在方法内部其实就是一个数组。 nums    
        System.out.println("元素个数：" + nums.length);    
        System.out.println("元素内容：" + Arrays.toString(nums));
    }
}
```

# 32.集合工具类Collections

**Collections不属于集合，而是属于操作集合的工具类**

![CollectionsAPI](.\img\CollectionsAPI.png)

![CollectionsAPI2](.\img\CollectionsAPI2.png)

# 33.Map集合体系

## 1.Map概述

![Map概述](.\img\Map概述.png)

## 2.Map集合的体系特点

![Map体系结构](.\img\Map体系结构.png)

![Map集合特点](.\img\Map集合特点.png)

##  3.Map集合常用API

![Map集合常用API](.\img\Map集合常用API.png)

```java
// 1、创建一个Map集合对象
// Map<String, Integer> maps = new HashMap<>(); 
// 一行经典代码
Map<String, Integer> maps = new LinkedHashMap<>();
maps.put("鸿星尔克", 3);
maps.put("Java", 1);
maps.put("枸杞", 100);
maps.put("Java", 100); // 覆盖前面的数据
maps.put(null, null);
System.out.println(maps);
```

**value()，获得所有键的值，返回一个Collection集合**

## 4.Map集合遍历

### 1.Map集合遍历1

![Map集合遍历1](.\img\Map集合遍历1.png)

```java
Map<String , Integer> maps = new HashMap<>();
// 1.添加元素: 无序，不重复，无索引。
maps.put("娃娃",30);
maps.put("iphoneX",100);
maps.put("huawei",1000);
maps.put("生活用品",10);
maps.put("手表",10);
System.out.println(maps);
// maps = {huawei=1000, 手表=10, 生活用品=10, iphoneX=100, 娃娃=30}
// 1、键找值：第一步：先拿到集合的全部键。
Set<String> keys = maps.keySet();
// 2、第二步：遍历每个键，根据键提取值
for (String key : keys) {    
    int value = maps.get(key);    
    System.out.println(key + "===>" + value);
}
```

### 2.Map集合遍历2

![Map集合遍历2](.\img\Map集合遍历2.png)

```java
Map<String , Integer> maps = new HashMap<>(); 
// 1.添加元素: 无序，不重复，无索引。 
maps.put("娃娃",30); 
maps.put("iphoneX",100); 
maps.put("huawei",1000);
maps.put("生活用品",10); 
maps.put("手表",10); 
System.out.println(maps); 
// maps = {huawei=1000, 手表=10, 生活用品=10, iphoneX=100, 娃娃=30} 

// 1、把Map集合转换成Set集合 
Set<Map.Entry<String, Integer>> entries = maps.entrySet(); 
// 2、开始遍历 
for(Map.Entry<String, Integer> entry : entries){     
    String key = entry.getKey();     
    int value = entry.getValue();     
    System.out.println(key + "====>" + value); 
}
```

### 3.Map集合遍历3

![Map集合遍历3](.\img\Map集合遍历3.png)

![lambda遍历源码](.\img\lambda遍历源码.png)

```java
 Map<String , Integer> maps = new HashMap<>();        
// 1.添加元素: 无序，不重复，无索引。        
maps.put("娃娃",30);        
maps.put("iphoneX",100);
//  Map集合后面重复的键对应的元素会覆盖前面重复的整个元素！        
maps.put("huawei",1000);        
maps.put("生活用品",10);        
maps.put("手表",10);        
System.out.println(maps);   
//方式1
//maps = {huawei=1000, 手表=10, 生活用品=10, iphoneX=100, 娃娃=30}
maps.forEach(new BiConsumer<String, Integer>() {
    @Override
    public void accept(String key, Integer value) {
        System.out.println(key + "--->" + value);
    }
});   
//方式2
maps.forEach((k, v) -> {                
    System.out.println(k + "--->" + v);        
});
```

##  5.HashMap

![HashMap](.\img\HashMap.png)

## 6.LinkedHashMap

![LinkedHashMap](.\img\LinkedHashMap.png)

## 7.TreeMap

![TreeMap](.\img\TreeMap.png)

## 8.总结

![Map总结](.\img\Map总结.png)

# 34.不可变集合

## 1.概述

![不可变集合](.\img\不可变集合.png)

## 2.不可变集合创建

![不可变集合创建](.\img\不可变集合创建.png)

```java
// 1、不可变的List集合
List<Double> lists = List.of(569.5, 700.5, 523.0,  570.5);
lists.add(689.0);
lists.set(2, 698.5);
System.out.println(lists);
double score = lists.get(1);
System.out.println(score);
// 2、不可变的Set集合
Set<String> names = Set.of("迪丽热巴", "迪丽热九", "马尔扎哈", "卡尔眨巴" );
names.add("三少爷");
System.out.println(names);
// 3、不可变的Map集合
Map<String, Integer> maps = Map.of("huawei",2, "Java开发", 1 , "手表", 1);
maps.put("衣服", 3);
System.out.println(maps);
```

修改会报错，UnsupportedOperationExceprion

**总结**

![不可变集合总结](.\img\不可变集合总结.png)

# 35.stream流

## 1.概述

![stream流简介](.\img\stream流简介.png)

![stream流的案例](.\img\stream流的案例.png)

方法一

```java
List<String> names = new ArrayList<>();        
Collections.addAll(names, "张三丰","张无忌","周芷若","赵敏","张强");       
System.out.println(names);        
// 1、从集合中找出姓张的放到新集合        
List<String> zhangList = new ArrayList<>();        
for (String name : names) {            
    if(name.startsWith("张")){                
        zhangList.add(name);            
    }        
}        
System.out.println(zhangList);        
// 2、找名称长度是3的姓名        
List<String> zhangThreeList = new ArrayList<>();        
for (String name : zhangList) {            
    if(name.length() == 3){                
        zhangThreeList.add(name);            
    }        
}        
System.out.println(zhangThreeList);
```

方法二

```java
names.stream().filter(s -> s.startsWith("张")).filter(s -> s.length() == 3).forEach(s -> System.out.println(s));
```

## 2.stream流的思想

![stream流的思想](.\img\stream流的思想.png)

## 3.stream流的小结

![stream流的总结](.\img\stream流的总结.png)

## 4.得到stream流

![stream流的获取](.\img\stream流的获取.png)

```java
/** --------------------Collection集合获取流-------------------------------   */
Collection<String> list = new ArrayList<>();
Stream<String> s =  list.stream();
/** --------------------Map集合获取流-------------------------------   */
Map<String, Integer> maps = new HashMap<>();
// 键流
Stream<String> keyStream = maps.keySet().stream();
// 值流
Stream<Integer> valueStream = maps.values().stream();
// 键值对流（拿整体）
Stream<Map.Entry<String,Integer>> keyAndValueStream =  maps.entrySet().stream();
/** ---------------------数组获取流------------------------------   */
String[] names = {"赵敏","小昭","灭绝","周芷若"};
Stream<String> nameStream = Arrays.stream(names);
Stream<String> nameStream2 = Stream.of(names);
```

**总结**

## 5.stream流的常用API

### 1.中间操作方法

![stream流的常用API](.\img\stream流的常用API.png)

**distinct()** 删除重复值

1.**中间方法也称为非终结方法，调用完成之后返回的新的stream流可以继续使用，支持链式编程**

2.**stream流中无法直接修改集合中或者数组中的数据**

```java
List<String> list = new ArrayList<>();       
list.add("张无忌");        
list.add("周芷若");        
list.add("赵敏");        
list.add("张强");        
list.add("张三丰");        
list.add("张三丰");        
// Stream<T> filter(Predicate<? super T> predicate)        
list.stream().filter(s -> s.startsWith("张")).forEach(s -> System.out.println(s));        
long size = list.stream().filter(s -> s.length() == 3).count();        
System.out.println(size);       
// list.stream().filter(s -> s.startsWith("张")).limit(2).forEach(s -> System.out.println(s));        list.stream().filter(s -> s.startsWith("张")).limit(2).forEach(System.out::println);        list.stream().filter(s -> s.startsWith("张")).skip(2).forEach(System.out::println);        
// map加工方法: 第一个参数原材料  -> 第二个参数是加工后的结果。        
// 给集合元素的前面都加上一个：黑马的：        
list.stream().map(s -> "黑马的：" + s).forEach(a -> System.out.println(a));        
// 需求：把所有的名称 都加工成一个学生对象。         
list.stream().map(s -> new Student(s)).forEach(s -> System.out.println(s));
//        list.stream().map(Student::new).forEach(System.out::println); 
// 构造器引用  方法引用        
// 合并流。        
Stream<String> s1 = list.stream().filter(s -> s.startsWith("张"));        
Stream<String> s2 = Stream.of("java1", "java2");       
// public static <T> Stream<T> concat(Stream<? extends T> a, Stream<? extends T> b)       
Stream<String> s3 = Stream.concat(s1 , s2);        
s3.distinct().forEach(s -> System.out.println(s));
```

### 2.终结方法

![stream流中的终结方法](.\img\stream流中的终结方法.png)

**get()获取当前对象**

### 3.小结

![终结方法和非终结方法的总结](.\img\终结方法和非终结方法的总结.png)

## 6.收集stream流

![收集stream流](.\img\收集stream流.png)

**注意：流只能使用一次**

```java
List<String> list = new ArrayList<>();        
list.add("张无忌");        
list.add("周芷若");        
list.add("赵敏");        
list.add("张强");        
list.add("张三丰");        
list.add("张三丰");        
Stream<String> s1 = list.stream().filter(s -> s.startsWith("张"));        
List<String> zhangList = s1.collect(Collectors.toList()); 
// 可变集合        
zhangList.add("java1");        
System.out.println(zhangList);
//       List<String> list1 = s1.toList(); 
// 得到不可变集合
//       list1.add("java");
//       System.out.println(list1);        
// 注意注意注意：“流只能使用一次”        
Stream<String> s2 = list.stream().filter(s -> s.startsWith("张"));        
Set<String> zhangSet = s2.collect(Collectors.toSet());        
System.out.println(zhangSet);       
Stream<String> s3 = list.stream().filter(s -> s.startsWith("张"));
//         Object[] arrs = s3.toArray();        
String[] arrs = s3.toArray(String[]::new); 
// 可以不管，拓展一下思维！！        
System.out.println("Arrays数组内容：" + Arrays.toString(arrs));
```

![收集stream流小结](.\img\收集stream流小结.png)

# 36.异常处理

## 1.概述

![异常的概述](.\img\异常的概述.png)

## 2.异常体系结构

![异常体系结构](.\img\异常体系结构.png)

## 3.异常的种类

![异常种类](.\img\异常种类.png)

## 4.异常的小总结

![异常小总结](.\img\异常小总结.png)

## 5.常见的运行时异常

![运行时异常](.\img\运行时异常.png)

```java
System.out.println("程序开始。。。。。。");
/** 1.数组索引越界异常: ArrayIndexOutOfBoundsException。*/
int[] arr = {1, 2, 3};System.out.println(arr[2]);
// System.out.println(arr[3]); // 运行出错，程序终止
/** 2.空指针异常 : NullPointerException。直接输出没有问题。但是调用空指针的变量的功能就会报错！！ */
String name = null;System.out.println(name); // null
// System.out.println(name.length()); // 运行出错，程序终止
/** 3.类型转换异常：ClassCastException。 */
Object o = 23;
// String s = (String) o;  // 运行出错，程序终止
/** 5.数学操作异常：ArithmeticException。 */
//int c = 10 / 0;
/** 6.数字转换异常： NumberFormatException。 */
//String number = "23";
String number = "23aabbc";
Integer it = Integer.valueOf(number); // 运行出错，程序终止
System.out.println(it + 1);
System.out.println("程序结束。。。。。");
```

## 6.常见的编译时异常

![编译时异常](.\img\编译时异常.png)

```java
public class ExceptionDemo {    
    public static void main(String[] args) throws ParseException {        
        String date = "2015-01-12 10:23:21";        // 创建一个简单日期格式化类：        
        SimpleDateFormat sdf = new SimpleDateFormat("yyyy/MM-dd HH:mm:ss");        
        // 解析字符串时间成为日期对象        
        Date d = sdf.parse(date);             
        System.out.println(d);    
    }
}
```

![编译时异常小结](.\img\编译时异常小结.png)

## 7.默认异常情况

![异常](.\img\异常.png)

![默认异常处理机制](.\img\默认异常处理机制.png)

## 8.编译时异常处理机制

### 1.方式1

![异常处理方式1](.\img\异常处理方式1.png)

```java
public static void main(String[] args) throws Exception {    
    System.out.println("程序开始。。。。。");    
    parseTime("2011-11-11 11:11:11");    
    System.out.println("程序结束。。。。。");
}
public static void parseTime(String date) throws Exception {    
    SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");    
    Date d = sdf.parse(date);    
    System.out.println(d);    
    InputStream is = new FileInputStream("E:/meinv.jpg");
}
```

### 2.方式2

![异常处理方式2](.\img\异常处理方式2.png)

```java
public class ExceptionDemo02 {    
    public static void main(String[] args) {        
        System.out.println("程序开始。。。。");        
        parseTime("2011-11-11 11:11:11");        
        System.out.println("程序结束。。。。");    
    }    
    public static void parseTime(String date) {        
        try {            
            SimpleDateFormat sdf = new SimpleDateFormat("yyyy/MM-dd HH:mm:ss");            
            Date d = sdf.parse(date);            
            System.out.println(d);            
            InputStream is = new FileInputStream("E:/meinv.jpg");        
        } catch (Exception e) {           
            e.printStackTrace(); // 打印异常栈信息        
        }
    }
```

### 3.方式3

![异常处理方式3](.\img\异常处理方式3.png)

### 4.总结

![处理异常总结](.\img\处理异常总结.png)

## 9.运行时异常处理机制

![运行时异常处理机制](.\img\运行时异常处理机制.png)

```java
System.out.println("程序开始。。。。。。。。。。");    
try {        
    chu(10, 0);    
} catch (Exception e) {        
    e.printStackTrace();    
}    
System.out.println("程序结束。。。。。。。。。。");
}
public static void chu(int a , int b) { 
    // throws RuntimeException{    
    System.out.println(a);    
    System.out.println(b);    
    int c = a / b;    
    System.out.println(c);
}
```

## 10.自定义异常

![自定义异常](.\img\自定义异常.png)

```java
public static void main(String[] args) {//        try {//            checkAge(-34);//        } catch (ItheimaAgeIlleagalException e) {//            e.printStackTrace();//        }        try {            checkAge2(-23);        } catch (Exception e) {            e.printStackTrace();        }    }    public static void checkAge2(int age)  {        if(age < 0 || age > 200){            // 抛出去一个异常对象给调用者            // throw ：在方法内部直接创建一个异常对象，并从此点抛出            // throws : 用在方法申明上的，抛出方法内部的异常            throw new ItheimaAgeIlleagalRuntimeException(age + " is illeagal!");        }else {            System.out.println("年龄合法：推荐商品给其购买~~");        }    }    public static void checkAge(int age) throws ItheimaAgeIlleagalException {        if(age < 0 || age > 200){            // 抛出去一个异常对象给调用者            // throw ：在方法内部直接创建一个异常对象，并从此点抛出            // throws : 用在方法申明上的，抛出方法内部的异常            throw new ItheimaAgeIlleagalException(age + " is illeagal!");        }else {            System.out.println("年龄合法：推荐商品给其购买~~");        }    }
```

### 1.编译时异常

```java
/**    自定义的编译时异常      1、继承Exception      2、重写构造器 */public class ItheimaAgeIlleagalException extends Exception{    public ItheimaAgeIlleagalException() {    }    public ItheimaAgeIlleagalException(String message) {        super(message);    }}
```

### 2.运行时异常

```java
public class ItheimaAgeIlleagalRuntimeException extends RuntimeException{    public ItheimaAgeIlleagalRuntimeException() {    }    public ItheimaAgeIlleagalRuntimeException(String message) {        super(message);    }}
```

#### 3.总结

![自定义异常总结](.\img\自定义异常总结.png)

# 37.日志框架

![日志技术](.\img\日志技术.png)

## 1.日志技术的体系

![日志框架](.\img\日志框架.png)

![日志小结](.\img\日志小结.png)

## 2.logback概述

![logback概述](.\img\logback概述.png)

**小结**

![logback小结](.\img\logback小结.png)

## 3.logback使用

![logback快熟入门](.\img\logback快熟入门.png)

## 4.logback开发步骤

![logback开发步骤](.\img\logback开发步骤.png)

## 5.logback输出位置、格式

![logback输出位置、格式](.\img\logback输出位置、格式.png)

## 6.logback.xml设置

![logback.xml设置](.\img\logback.xml设置.png)

## 7.日志级别设置

![日志级别](.\img\日志级别.png)

**小结**

![日志级别小结](.\img\日志级别小结.png)

# 38.File类

##  1.File类创建对象

![File类创建对象](.\img\File类创建对象.png)

```java
 // 1、创建File对象（指定了文件的路径）        // 路径写法： D:\resources\xueshan.jpeg        //          D:/resources/xueshan.jpeg        //          File.separator//        File f = new File("D:\\resources\\xueshan.jpeg");//        File f = new File("D:/resources/xueshan.jpeg");        File f = new File("D:" + File.separator+"resources"+ File.separator +"xueshan.jpeg");        long size = f.length(); // 是文件的字节大小        System.out.println(size);        // 2、File创建对象，支持绝对路径 支持相对路径（重点）        File f1 = new File("D:\\resources\\beauty.jpeg"); // 绝对路径        System.out.println(f1.length());        // 相对路径：一般定位模块中的文件的。 相对到工程下！！        File f2 = new File("file-io-app/src/data.txt");        System.out.println(f2.length());        // 3、File创建对象 ，可以是文件也可以是文件夹        File f3 = new File("D:\\resources");        System.out.println(f3.exists()); // 判断这个路径是否存在，这个文件夹存在否
```

## 2.路径的区别

![路径](.\img\路径.png)

## 3.File类小结

![File类小结](.\img\File类小结.png)

## 4.File类的常用API

### 1.判断文件类型、获取文件信息

![File类的API](.\img\File类的API.png)

```java
// 1.绝对路径创建一个文件对象File f1 = new File("D:/resources/xueshan.jpeg");// a.获取它的绝对路径。System.out.println(f1.getAbsolutePath());// b.获取文件定义的时候使用的路径。System.out.println(f1.getPath());// c.获取文件的名称：带后缀。System.out.println(f1.getName());// d.获取文件的大小：字节个数。System.out.println(f1.length()); // 字节大小// e.获取文件的最后修改时间long time = f1.lastModified();System.out.println("最后修改时间：" + new SimpleDateFormat("yyyy/MM/dd HH:mm:ss").format(time));// f、判断文件是文件还是文件夹System.out.println(f1.isFile()); // trueSystem.out.println(f1.isDirectory()); // falseSystem.out.println("-------------------------");File f2 = new File("file-io-app\\src\\data.txt");// a.获取它的绝对路径。System.out.println(f2.getAbsolutePath());// b.获取文件定义的时候使用的路径。System.out.println(f2.getPath());// c.获取文件的名称：带后缀。System.out.println(f2.getName());// d.获取文件的大小：字节个数。System.out.println(f2.length()); // 字节大小// e.获取文件的最后修改时间long time1 = f2.lastModified();System.out.println("最后修改时间：" + new SimpleDateFormat("yyyy/MM/dd HH:mm:ss").format(time1));// f、判断文件是文件还是文件夹System.out.println(f2.isFile()); // trueSystem.out.println(f2.isDirectory()); // falseSystem.out.println(f2.exists()); // trueFile file = new File("D:/");System.out.println(file.isFile()); // falseSystem.out.println(file.isDirectory()); // trueSystem.out.println(file.exists()); // trueFile file1 = new File("D:/aaa");System.out.println(file1.isFile()); // falseSystem.out.println(file1.isDirectory()); // falseSystem.out.println(file1.exists()); // false
```

### 2.创建文件、删除文件

![文件删除、创建API](.\img\文件删除、创建API.png)

```java
 File f = new File("file-io-app\\src\\data.txt");        // a.创建新文件，创建成功返回true ,反之 ,不需要这个，以后文件写出去的时候都会自动创建        System.out.println(f.createNewFile());        File f1 = new File("file-io-app\\src\\data02.txt");        System.out.println(f1.createNewFile()); // （几乎不用的，因为以后文件都是自动创建的！）        // b.mkdir创建一级目录        File f2 = new File("D:/resources/aaa");        System.out.println(f2.mkdir());        // c.mkdirs创建多级目录(重点)        File f3 = new File("D:/resources/ccc/ddd/eee/ffff");//        System.out.println(f3.mkdir());        System.out.println(f3.mkdirs()); // 支持多级创建        // d.删除文件或者空文件夹        System.out.println(f1.delete());        File f4 = new File("D:/resources/xueshan.jpeg");        System.out.println(f4.delete()); // 占用一样可以删除        // 只能删除空文件夹,不能删除非空文件夹.        File f5 = new File("D:/resources/aaa");        System.out.println(f5.delete());
```

### 3.File类的遍历

![File类的遍历功能](.\img\File类的遍历功能.png)

```java
// 1、定位一个目录File f1 = new File("D:/resources");String[] names = f1.list();for (String name : names) {    System.out.println(name);}// 2.一级文件对象// 获取当前目录下所有的"一级文件对象"到一个文件对象数组中去返回（重点）File[] files = f1.listFiles();for (File f : files) {    System.out.println(f.getAbsolutePath());}// 注意事项File dir = new File("D:/resources/ddd");File[] files1 = dir.listFiles();System.out.println(Arrays.toString(files1));
```

# 39.方法递归

## 1.概述

方法直接调用或者间接调用自己，称为**方法递归（recursion）**

递归的形式

**直接递归**：方法自己调用自己

**间接递归**：方法调用其他方法，其他方法又调用了自己

```java
public static void test(){    System.out.println("=======test被执行========");    test(); // 方法递归 直接递归形式}public static void test2(){    System.out.println("=======test2被执行========");    test3(); // 方法递归 间接递归}private static void test3() {    System.out.println("=======test3被执行========");    test2();}
```

## 2.递归的总结思路（有规律）

12：10[Java入门基础视频教程，java零基础自学首选黑马程序员Java入门教程（含Java项目和Java真题）_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Cv411372m?p=155&spm_id_from=pageDriver)

![递归的总结思路](.\img\递归的总结思路.png)

![递归执行内存](.\img\递归执行内存.png)

## 3.非规律递归

### 1.文件搜索

![文件搜索](.\img\文件搜索.png)

```java
public static void searchFile(File dir,String fileName){    // 3、判断dir是否是目录    if(dir != null && dir.isDirectory()){        // 可以找了        // 4、提取当前目录下的一级文件对象        File[] files = dir.listFiles(); // null  []        // 5、判断是否存在一级文件对象，存在才可以遍历        if(files != null && files.length > 0) {            for (File file : files) {                // 6、判断当前遍历的一级文件对象是文件 还是 目录                if(file.isFile()){                    // 7、是不是咱们要找的，是把其路径输出即可                    if(file.getName().contains(fileName)){                        System.out.println("找到了：" + file.getAbsolutePath());                        // 启动它。                        try {                            Runtime r = Runtime.getRuntime();                            r.exec(file.getAbsolutePath());                        } catch (IOException e) {                            e.printStackTrace();                        }                    }                }else {                    // 8、是文件夹，需要继续递归寻找                    searchFile(file, fileName);                }            }        }    }else {        System.out.println("对不起，当前搜索的位置不是文件夹！");    }}
```

### 2.啤酒问题

![啤酒问题](.\img\啤酒问题.png)

```java
// 定义一个静态的成员变量用于存储可以买的酒数量public static int totalNumber; // 总数量public static int lastBottleNumber; // 记录每次剩余的瓶子个数public static int lastCoverNumber; // 记录每次剩余的盖子个数public static void main(String[] args) {    // 1、拿钱买酒    buy(10);    System.out.println("总数：" + totalNumber);    System.out.println("剩余盖子数：" + lastCoverNumber);    System.out.println("剩余瓶子数：" + lastBottleNumber);}public static void buy(int money){    // 2、看可以立马买多少瓶    int buyNumber = money / 2; // 5    totalNumber += buyNumber;    // 3、把盖子 和瓶子换算成钱    // 统计本轮总的盖子数  和 瓶子数    int coverNumber = lastCoverNumber + buyNumber;    int bottleNumber = lastBottleNumber + buyNumber;    // 统计可以换算的钱    int allMoney = 0;    if(coverNumber >= 4){        allMoney += (coverNumber / 4) * 2;    }    lastCoverNumber = coverNumber % 4;    if(bottleNumber >= 2){        allMoney += (bottleNumber / 2) * 2;    }    lastBottleNumber = bottleNumber % 2;    if(allMoney >= 2){        buy(allMoney);    }    Integer[] arr2 = new Integer[]{11, 22, 33};    Arrays.sort(arr2);
```

# 40.字符集

## 1.概述

![字符集](.\img\字符集.png)

## 2.分类

![字符码的分类1](.\img\字符码的分类1.png)

![字符编码2](.\img\字符编码2.png)

## 3.汉字存储过程

![汉字存储过程](.\img\汉字存储过程.png)

## 4.字符集小结

![字符集小结](.\img\字符集小结.png)

## 5.字符集编码和解码

![字符集编码解码](.\img\字符集编码解码.png)

```java
// 1、编码：把文字转换成字节（使用指定的编码）String name = "abc我爱你中国";// byte[] bytes = name.getBytes(); // 以当前代码默认字符集进行编码 （UTF-8）byte[] bytes = name.getBytes("GBK"); // 指定编码System.out.println(bytes.length);System.out.println(Arrays.toString(bytes));// 2、解码：把字节转换成对应的中文形式（编码前 和 编码后的字符集必须一致，否则乱码 ）// String rs = new String(bytes); // 默认的UTF-8String rs = new String(bytes, "GBK"); // 指定GBK解码System.out.println(rs);
```

# 41.IO流

输入输出流

I表示input代表输入，负责读

O表示output代表s输出，负责写

![IO流概述](.\img\IO流概述.png)

## 1.IO流的分类

![IO流的分类](.\img\IO流的分类.png)

![流的四大类](.\img\流的四大类.png)

![流的分类](.\img\流的分类.png)

## 2.小结

![IO流小结](.\img\IO流小结.png)

# 42.字节流的使用

## 1.文件字节输入流（每次读取一个字节）

![FileInputStream](.\img\FileInputStream.png)

```java
 // 1、创建一个文件字节输入流管道与源文件接通。        
InputStream is = new FileInputStream(new File("file-io-app\\src\\data.txt"));        
// 简化写法        
InputStream is = new FileInputStream("file-io-app\\src\\data.txt");        
// 2、读取一个字节返回 （每次读取一滴水）        
int b1 = is.read();        
System.out.println((char)b1);        
int b2 = is.read();        
System.out.println((char)b2);        
int b3 = is.read();        
System.out.println((char)b3);        
int b4 = is.read(); // 读取完毕返回-1        
System.out.println(b4);        
// 3、使用循环改进        
// 定义一个变量记录每次读取的字节    a  b  3   爱        
//                              o  o  o   [ooo]        
int b;        
while (( b = is.read() ) != -1){            
    System.out.print((char) b);        
}
```

![FileInputStream小结](.\img\FileInputStream小结.png)

## 2.文件字节输入流（每次读取一个字节数组）

```java
// 1、创建一个文件字节输入流管道与源文件接通
InputStream is = new FileInputStream("file-io-app/src/data02.txt");
// 2、定义一个字节数组，用于读取字节数组
byte[] buffer = new byte[3]; // 3B
int len = is.read(buffer);
System.out.println("读取了几个字节：" + len);
String rs = new String(buffer);
System.out.println(rs);
int len1 = is.read(buffer);
System.out.println("读取了几个字节：" + len1);
String rs1 = new String(buffer);
System.out.println(rs1);// buffer = [a b c]// buffer = [a b c]  ==>  [c d c]
int len2 = is.read(buffer);
System.out.println("读取了几个字节：" + len2);
// 读取多少倒出多少
String rs2 = new String(buffer,0 ,len2);
System.out.println(rs2);
int len3 = is.read(buffer);
System.out.println(len3); // 读取完毕返回-1
// 3、改进使用循环，每次读取一个字节数组
byte[] buffer = new byte[3];
int len; // 记录每次读取的字节数。
while ((len = is.read(buffer)) != -1) {    
    // 读取多少倒出多少    
    System.out.print(new String(buffer, 0 , len));
}
```

![FileInputStream一次读取一个字符数组小结](.\img\FileInputStream一次读取一个字符数组小结.png)

## 3.文件字节输入流（一次读完所有字节）

![FileInputStream一次性读取所有字节](.\img\FileInputStream一次性读取所有字节.png)

```java
// 1、创建一个文件字节输入流管道与源文件接通
File f = new File("file-io-app/src/data03.txt");
InputStream is = new FileInputStream(f);
// 2、定义一个字节数组与文件的大小刚刚一样大。
byte[] buffer = new byte[(int) f.length()];
int len = is.read(buffer);
System.out.println("读取了多少个字节：" + len);
System.out.println("文件大小：" + f.length());
System.out.println(new String(buffer));
// 读取全部字节数组
byte[] buffer = is.readAllBytes();
System.out.println(new String(buffer));
```

![FileInputStream一次性读取所有字节总结](.\img\FileInputStream一次性读取所有字节总结.png)

## 4.文件字节输出流（写字节数据到文件）

![写文件](.\img\写文件.png)

```java
 // 1、创建一个文件字节输出流管道与目标文件接通        
OutputStream os = new FileOutputStream("file-io-app/src/out04.txt" , true); // 追加数据管道
OutputStream os = new FileOutputStream("file-io-app/src/out04.txt"); // 先清空之前的数据，写新数据进入        
// 2、写数据出去        
// a.public void write(int a):写一个字节出去        
os.write('a');        
os.write(98);        
os.write("\r\n".getBytes()); // 换行        
// os.write('徐'); // [ooo]        
// b.public void write(byte[] buffer):写一个字节数组出去。        
byte[] buffer = {'a' , 97, 98, 99};        
os.write(buffer);        
os.write("\r\n".getBytes()); // 换行        
byte[] buffer2 = "我是中国人".getBytes();
//        byte[] buffer2 = "我是中国人".getBytes("GBK");        
os.write(buffer2);        
os.write("\r\n".getBytes()); // 换行        
// c. public void write(byte[] buffer , int pos , int len):写一个字节数组的一部分出去。        
byte[] buffer3 = {'a',97, 98, 99};        
os.write(buffer3, 0 , 3);       
os.write("\r\n".getBytes()); // 换行        
// os.flush(); // 写数据必须，刷新数据 可以继续使用流        
os.close(); // 释放资源，包含了刷新的！关闭后流不可以使用了
```

![字节输出流总结1](.\img\字节输出流总结1.png)

![字节输出流总结2](.\img\字节输出流总结2.png)

## 5.文件拷贝

![字节输出流](.\img\字节输出流.png)

![文件复制小结](.\img\文件复制小结.png)

```java
InputStream is = null;OutputStream os = null;
try {    
    // System.out.println(10/ 0);    
    // 1、创建一个字节输入流管道与原视频接通     
    is = new FileInputStream("file-io-app/src/out04.txt");    
    // 2、创建一个字节输出流管道与目标文件接通     
    os = new FileOutputStream("file-io-app/src/out05.txt");    
    // 3、定义一个字节数组转移数据    
    byte[] buffer = new byte[1024];    
    int len; // 记录每次读取的字节数。    
    while ((len = is.read(buffer)) != -1){        
        os.write(buffer, 0 , len);    
    }    
    System.out.println("复制完成了！");
```

# 43.资源释放的方式

## 1.try-catch-finally

![资源释放1](.\img\资源释放1.png)

```java
public static int test(int a , int b){   
    try {        
        int c = a / b;        
        return c;    
    }catch (Exception e){        
        e.printStackTrace();        
        return -111111; // 计算出现bug.    
    }finally {        
        System.out.println("--finally--");        
        // 哪怕上面有return语句执行，也必须先执行完这里才可以！        
        // 开发中不建议在这里加return ，如果加了，返回的永远是这里的数据了，这样会出问题！        
        return 100;    
    }
```

![资源释放1小结](.\img\资源释放1小结.png)

## 2.try-with-resource

![资源释放简化](.\img\资源释放简化.png)

### 1.JDK7

```java
try (                
    // 这里面只能放置资源对象，用完会自动关闭：自动调用资源对象的close方法关闭资源（即使出现异常也会做关闭操作）                 // 1、创建一个字节输入流管道与原视频接通               
    InputStream is = new FileInputStream("file-io-app/src/out04.txt");                
    // 2、创建一个字节输出流管道与目标文件接通              
    OutputStream os = new FileOutputStream("file-io-app/src/out05.txt");               
    // int age = 23; // 这里只能放资源               
    MyConnection connection = new MyConnection(); // 最终会自动调用资源的close方法                
) {            
    // 3、定义一个字节数组转移数据           
    byte[] buffer = new byte[1024];            
    int len; // 记录每次读取的字节数。            
    while ((len = is.read(buffer)) != -1){                
        os.write(buffer, 0 , len);            
    }            
    System.out.println("复制完成了！");        
} catch (Exception e){            
    e.printStackTrace();        
}    
}
}
class MyConnection implements AutoCloseable{    
    @Override    
    public void close() throws IOException {        
        System.out.println("连接资源被成功释放了！");    
    }
```

### 2.JDK9

```java
// 这里面只能放置资源对象，用完会自动关闭：自动调用资源对象的close方法关闭资源（即使出现异常也会做关闭操作）
// 1、创建一个字节输入流管道与原视频接通
InputStream is = new FileInputStream("file-io-app/src/out04.txt");
// 2、创建一个字节输出流管道与目标文件接通
OutputStream os = new FileOutputStream("file-io-app/src/out05.txt");
try ( is ; os ) {    
    // 3、定义一个字节数组转移数据    
    byte[] buffer = new byte[1024];    
    int len; // 记录每次读取的字节数。    
    while ((len = is.read(buffer)) != -1){        
        os.write(buffer, 0 , len);    
    }    
    System.out.println("复制完成了！");
} catch (Exception e){    
    e.printStackTrace();
}
```

## 3.小结

![资源释放2小结](.\img\资源释放2小结.png)

# 44.字符流的使用

## 1.文件字符输入流（一次读取一个字符）

![字符流（一次一个字节）](.\img\字符流（一次一个字节）.png)

![Reader](.\img\Reader.png)

```java
// 目标：每次读取一个字符。
// 1、创建一个字符输入流管道与源文件接通
Reader fr = new FileReader("file-io-app\\src\\data06.txt");
// 2、读取一个字符返回，没有可读的字符了返回-1
int code = fr.read();
System.out.print((char)code);
int code1 = fr.read();
System.out.print((char)code1);
// 3、使用循环读取字符
int code;
while ((code = fr.read()) != -1){    
    System.out.print((char) code);
}
```

 ![字符流1总结](.\img\字符流1总结.png)

## 2.文件字符输入流（一次读取一个字符数组）

```java
// 1、创建一个文件字符输入流与源文件接通
Reader fr = new FileReader("file-io-app/src/data07.txt");
// 2、用循环，每次读取一个字符数组的数据。 1024 + 1024 + 8
char[] buffer = new char[1024]; // 1K字符
int len;
while ((len = fr.read(buffer)) != -1) {    
    String rs = new String(buffer, 0, len);    
    System.out.print(rs);
}
```

![字符流2总结](.\img\字符流2总结.png)

## 3.文件字符输出流

![字符输出](.\img\字符输出.png)

![FileWriter构造器](.\img\FileWriter构造器.png)

![FileWriterAPI](.\img\FileWriterAPI.png)

```java
 // 1、创建一个字符输出流管道与目标文件接通        
// Writer fw = new FileWriter("file-io-app/src/out08.txt"); 
// 覆盖管道，每次启动都会清空文件之前的数据        
Writer fw = new FileWriter("file-io-app/src/out08.txt", true); 
// 覆盖管道，每次启动都会清空文件之前的数据
//      a.public void write(int c):写一个字符出去        
fw.write(98);        
fw.write('a');        
fw.write('徐'); // 不会出问题了        
fw.write("\r\n"); // 换行
//       b.public void write(String c)写一个字符串出去        
fw.write("abc我是中国人");        
fw.write("\r\n"); // 换行
//       c.public void write(char[] buffer):写一个字符数组出去        
char[] chars = "abc我是中国人".toCharArray();        
fw.write(chars);       
fw.write("\r\n"); // 换行
//       d.public void write(String c ,int pos ,int len):写字符串的一部分出去        
fw.write("abc我是中国人", 0, 5);        
fw.write("\r\n"); // 换行
//       e.public void write(char[] buffer ,int pos ,int len):写字符数组的一部分出去        
fw.write(chars, 3, 5);       
fw.write("\r\n"); // 换行        
// fw.flush();// 刷新后流可以继续使用        
fw.close(); // 关闭包含刷线，关闭后流不能使用
```

![FileWriter追加数据](.\img\FileWriter追加数据.png)

# 45.字节流和字符流的区别

![字节流和字符流的区别](.\img\字节流和字符流的区别.png)

# 46.缓冲流

## 1.概述

**默认缓冲区为8kb**

![缓冲区的概述](.\img\缓冲区的概述.png)

## 2.体系

![缓存流](.\img\缓存流.png)

![缓冲流小结](.\img\缓冲流小结.png)

## 3.字节缓冲流

![字节缓冲](.\img\字节缓冲.png)

**字节缓冲优化原理**

![字节缓冲优化原理](.\img\字节缓冲优化原理.png)

![字节缓冲流](.\img\字节缓冲流.png)

```java
try (        
    // 这里面只能放置资源对象，用完会自动关闭：自动调用资源对象的close方法关闭资源（即使出现异常也会做关闭操作）        
    // 1、创建一个字节输入流管道与原视频接通        
    InputStream is = new FileInputStream("D:\\resources\\newmeinv.jpeg");        
    // a.把原始的字节输入流包装成高级的缓冲字节输入流        
    InputStream bis = new BufferedInputStream(is);        
    // 2、创建一个字节输出流管道与目标文件接通        
    OutputStream os = new FileOutputStream("D:\\resources\\newmeinv222.jpeg");        
    // b.把字节输出流管道包装成高级的缓冲字节输出流管道        
    OutputStream bos = new BufferedOutputStream(os);) {    
    // 3、定义一个字节数组转移数据    
    byte[] buffer = new byte[1024];    
    int len; // 记录每次读取的字节数。    
    while ((len = bis.read(buffer)) != -1){        
        bos.write(buffer, 0 , len);    
    }    
    System.out.println("复制完成了！");
} catch (Exception e){    
    e.printStackTrace();
}
```

![字节缓冲流小结](.\img\字节缓冲流小结.png)

## 4.不同的字节流比较时间

![不同的字节流比较时间](.\img\不同的字节流比较时间.png)

```java
private static final String SRC_FILE = "D:\\course\\基础加强\\day08-日志框架、阶段项目\\视频\\14、用户购票功能.avi";
private static final String DEST_FILE = "D:\\course\\";
public static void main(String[] args) {    
    // copy01(); 
    // 使用低级的字节流按照一个一个字节的形式复制文件：慢的让人简直无法忍受。直接被淘汰。    
    copy02(); 
    // 使用低级的字节流按照一个一个字节数组的形式复制文件: 比较慢，但是还是可以忍受的！    
    // copy03(); 
    // 缓冲流一个一个字节复制：很慢，不建议使用。    
    copy04(); 
    // 缓冲流一个一个字节数组复制：飞快，简直太完美了（推荐使用）
}
private static void copy04() {    
    long startTime = System.currentTimeMillis();    
    try (            
        // 1、创建低级的字节输入流与源文件接通            
        InputStream is = new FileInputStream(SRC_FILE);            
        // a.把原始的字节输入流包装成高级的缓冲字节输入流            
        InputStream bis = new BufferedInputStream(is);            
        // 2、创建低级的字节输出流与目标文件接通           
        OutputStream os = new FileOutputStream(DEST_FILE + "video4.avi");            
        // b.把字节输出流管道包装成高级的缓冲字节输出流管道            
        OutputStream bos = new BufferedOutputStream(os);    
    ) {        
        // 3、定义一个字节数组转移数据        
        byte[] buffer = new byte[1024];        
        int len; // 记录每次读取的字节数。        
        while ((len = bis.read(buffer)) != -1){            
            bos.write(buffer, 0 , len);       
        }    
    } catch (Exception e){       
        e.printStackTrace();   
    }    
    long endTime = System.currentTimeMillis();    
    System.out.println("使用缓冲的字节流按照一个一个字节数组的形式复制文件耗时：" + (endTime - startTime)/1000.0 + "s");
}
private static void copy03() {    
    long startTime = System.currentTimeMillis();    
    try (            
        // 1、创建低级的字节输入流与源文件接通            
        InputStream is = new FileInputStream(SRC_FILE);            
        // a.把原始的字节输入流包装成高级的缓冲字节输入流           
        InputStream bis = new BufferedInputStream(is);            
        // 2、创建低级的字节输出流与目标文件接通            
        OutputStream os = new FileOutputStream(DEST_FILE + "video3.avi");           
        // b.把字节输出流管道包装成高级的缓冲字节输出流管道           
        OutputStream bos = new BufferedOutputStream(os);   
    ){        
        // 3、定义一个变量记录每次读取的字节（一个一个字节的复制）        
        int b;        
        while ((b = bis.read()) != -1){            
            bos.write(b);       
        }    
    }catch (Exception e){        
        e.printStackTrace();   
    }    
    long endTime = System.currentTimeMillis();    
    System.out.println("使用缓冲的字节流按照一个一个字节的形式复制文件耗时：" + (endTime - startTime)/1000.0 + "s");
}
private static void copy02() {   
    long startTime = System.currentTimeMillis();    
    try (            
        // 这里面只能放置资源对象，用完会自动关闭：自动调用资源对象的close方法关闭资源（即使出现异常也会做关闭操作）            // 1、创建一个字节输入流管道与原视频接通            
        InputStream is = new FileInputStream(SRC_FILE);            
        // 2、创建一个字节输出流管道与目标文件接通            
        OutputStream os = new FileOutputStream(DEST_FILE + "video2.avi")   
    ) {       
        // 3、定义一个字节数组转移数据       
        byte[] buffer = new byte[1024];        
        int len; // 记录每次读取的字节数。       
        while ((len = is.read(buffer)) != -1){           
            os.write(buffer, 0 , len);      
        }   
    } catch (Exception e){       
        e.printStackTrace();   
    }    
    long endTime = System.currentTimeMillis();   
    System.out.println("使用低级的字节流按照一个一个字节数组的形式复制文件耗时：" + (endTime - startTime)/1000.0 + "s");
}
/**  使用低级的字节流按照一个一个字节的形式复制文件 */
private static void copy01() {   
    long startTime = System.currentTimeMillis();   
    try (           
        // 1、创建低级的字节输入流与源文件接通          
        InputStream is = new FileInputStream(SRC_FILE);       
        // 2、创建低级的字节输出流与目标文件接通       
        OutputStream os = new FileOutputStream(DEST_FILE + "video1.avi")         
    ){        
        // 3、定义一个变量记录每次读取的字节（一个一个字节的复制）      
        int b;      
        while ((b = is.read()) != -1){          
            os.write(b);     
        }  
    }catch (Exception e){       
        e.printStackTrace();  
    }   
    long endTime = System.currentTimeMillis();   
    System.out.println("使用低级的字节流按照一个一个字节的形式复制文件耗时：" + (endTime - startTime)/1000.0 + "s");
}
```

## 5.字符缓冲流

![字符缓冲](.\img\字符缓冲.png)

### **1.字符缓冲输入流**

 ![字符缓冲输入流](.\img\字符缓冲输入流.png)

```java
try (        
    // 1、创建一个文件字符输入流与源文件接通。        
    Reader fr = new FileReader("io-app2/src/data01.txt");        
    // a、把低级的字符输入流包装成高级的缓冲字符输入流。        
    BufferedReader br = new BufferedReader(fr);        
){    
    // 2、用循环，每次读取一个字符数组的数据。  1024 + 1024 + 8    
    char[] buffer = new char[1024]; // 1K字符    
    int len;    
    while ((len = br.read(buffer)) != -1) {       
        String rs = new String(buffer, 0, len);   
        System.out.print(rs);  
    }      
    String line;     
    while ((line = br.readLine()) != null){         
        System.out.println(line);  
    }
} catch (IOException e) {   
    e.printStackTrace();
}
```

### 2.字符缓冲输出流

![字符缓冲输出流](.\img\字符缓冲输出流.png)

```java
 // 1、创建一个字符输出流管道与目标文件接通       
Writer fw = new FileWriter("io-app2/src/out02.txt"); // 覆盖管道，每次启动都会清空文件之前的数据       
//Writer fw = new FileWriter("io-app2/src/out02.txt", true); // 追加数据        
BufferedWriter bw = new BufferedWriter(fw);
//      a.public void write(int c):写一个字符出去        
bw.write(98);        
bw.write('a');      
bw.write('徐'); // 不会出问题了        
bw.newLine(); // bw.write("\r\n"); // 换行
//       b.public void write(String c)写一个字符串出去        
bw.write("abc我是中国人");       
bw.newLine(); // bw.write("\r\n"); // 换行
//       c.public void write(char[] buffer):写一个字符数组出去        
char[] chars = "abc我是中国人".toCharArray();       
bw.write(chars);       
bw.newLine(); // bw.write("\r\n"); // 换行
//       d.public void write(String c ,int pos ,int len):写字符串的一部分出去       
bw.write("abc我是中国人", 0, 5);       
bw.newLine(); // bw.write("\r\n"); // 换行
//       e.public void write(char[] buffer ,int pos ,int len):写字符数组的一部分出去       
bw.write(chars, 3, 5);      
bw.newLine(); // bw.write("\r\n"); // 换行       
// fw.flush();// 刷新后流可以继续使用       
bw.close(); // 关闭包含刷线，关闭后流不能使用
```

### 3.字符缓冲流小结

![字符缓冲流小结](.\img\字符缓冲流小结.png)

# 47.转换流

当文件编码不一致时，会出现乱码

![字符输入输出转换流](.\img\字符输入输出转换流.png)

## 1.字符输入转换流

![字符输入转换流API](.\img\字符输入转换流API.png)

```java
// 代码UTF-8   文件 GBK  "D:\\resources\\data.txt"
// 1、提取GBK文件的原始字节流。   abc 我
//                            ooo oo
InputStream is = new FileInputStream("D:\\resources\\data.txt");
// 2、把原始字节流转换成字符输入流
Reader isr = new InputStreamReader(is); 
// 默认以UTF-8的方式转换成字符流。 还是会乱码的  跟直接使用FileReader是一样的
Reader isr = new InputStreamReader(is , "GBK"); 
// 以指定的GBK编码转换成字符输入流  完美的解决了乱码问题
BufferedReader br = new BufferedReader(isr);
String line;
while ((line = br.readLine()) != null){    
    System.out.println(line);
}
```

## 2.字符输出转换流

![字符输出转换流](.\img\字符输出转换流.png)

![字符输出转换流API](.\img\字符输出转换流API.png)

```java
// 1、定义一个字节输出流
OutputStream os = new FileOutputStream("io-app2/src/out03.txt");
// 2、把原始的字节输出流转换成字符输出流
// Writer osw = new OutputStreamWriter(os);
// 以默认的UTF-8写字符出去 跟直接写FileWriter一样
Writer osw = new OutputStreamWriter(os , "GBK"); // 指定GBK的方式写字符出去
// 3、把低级的字符输出流包装成高级的缓冲字符输出流。
BufferedWriter bw = new BufferedWriter(osw);
bw.write("我爱中国1~~");
bw.write("我爱中国2~~");
bw.write("我爱中国3~~");
bw.close();
```

#  48.序列化对象

## 1.对象序列化

把内存文件，存储到磁盘文件中，称为对象序列化

**implements serializable**

![对象序列化](.\img\对象序列化.png)

![对象字节输出流](.\img\对象字节输出流.png)

![ObjectOutputStream](.\img\ObjectOutputStream.png)

![对象序列化小结](.\img\对象序列化小结.png)

```java
// 1、创建学生对象Student s = new Student("陈磊", "chenlei","1314520", 21);// 2、对象序列化：使用对象字节输出流包装字节输出流管道ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("io-app2/src/obj.txt"));// 3、直接调用序列化方法oos.writeObject(s);// 4、释放资源oos.close();System.out.println("序列化完成了~~");
```

## 2.对象的反序列化

![对象反序列化](.\img\对象反序列化.png)

![对象字节输入流](.\img\对象字节输入流.png)

![对象反序列化API](.\img\对象反序列化API.png)

```java
// 1、创建对象字节输入流管道包装低级的字节输入流管道ObjectInputStream is = new ObjectInputStream(new FileInputStream("io-app2/src/obj.txt"));// 2、调用对象字节输入流的反序列化方法Student s = (Student) is.readObject();System.out.println(s);
```

**transient关键字修饰的属性不参与序列化**

**序列号版本要和反序列号版本一致才不会出错**

![对象反序列化小结](.\img\对象反序列化小结.png)

# 49.打印流

![打印流](.\img\打印流.png)

## 1.打印流PrintStream

![打印流PrintStream](.\img\打印流PrintStream.png)

## 2.打印流PrintWriter

![打印流PrintWriter](.\img\打印流PrintWriter.png)

```java
// 1、创建一个打印流对象//        
PrintStream ps = new PrintStream(new FileOutputStream("io-app2/src/ps.txt")); 
// 追加数据，在低级管道后面加True  
PrintStream ps = new PrintStream(new FileOutputStream("io-app2/src/ps.txt" , true)); 
PrintStream ps = new PrintStream("io-app2/src/ps.txt" );        
PrintWriter ps = new PrintWriter("io-app2/src/ps.txt"); 
// 打印功能上与PrintStream的使用没有区别        
ps.println(97);        
ps.println('a');        
ps.println(23.3);       
ps.println(true);        
ps.println("我是打印流输出的，我是啥就打印啥");        
ps.close();
```

## 3.PrintStream和PrintWriter的区别

![PrintStream和PrintWriter的区别](.\img\PrintStream和PrintWriter的区别.png)

## 4.输出重定向

System.out()重定向输出位置

# 50.Properties

![Properties体系](.\img\Properties体系.png)

## 1.Properties的作用

![Properties的作用](.\img\Properties的作用.png)

## 2.PropertiesAPI

![PropertiesAPI](.\img\PropertiesAPI.png)

## 3.存储数据

```java
// 需求：使用Properties把键值对信息存入到属性文件中去。
Properties properties = new Properties();
properties.setProperty("admin", "123456");
properties.setProperty("dlei", "003197");
properties.setProperty("heima", "itcast");
System.out.println(properties);
/**   
参数一：保存管道 字符输出流管道   
参数二：保存心得 
*/
properties.store(new FileWriter("io-app2/src/users.properties"),"this is users!! i am very happy! give me 100!");
```

## 4.取出数据

```java
// 需求：Properties读取属性文件中的键值对信息。（读取）
Properties properties = new Properties();System.out.println(properties);
// 加载属性文件中的键值对数据到属性对象properties中去
properties.load(new FileReader("io-app2/src/users.properties"));
System.out.println(properties);
String rs = properties.getProperty("dlei");
System.out.println(rs);
String rs1 = properties.getProperty("admin");
System.out.println(rs1);
```

## 5.小结

![Properties的小结](.\img\Properties的小结.png)

# 51.IO框架

![IO框架](.\img\IO框架.png)

```java
// 1.完成文件复制！        
IOUtils.copy(new FileInputStream("D:\\resources\\hushui.jpeg"),                new FileOutputStream("D:\\resources\\hushui2.jpeg"));
// 2.完成文件复制到某个文件夹下！        
FileUtils.copyFileToDirectory(new File("D:\\resources\\hushui.jpeg"), new File("D:/"));           
//3.完成文件夹复制到某个文件夹下！          
FileUtils.copyDirectoryToDirectory(new File("D:\\resources") , new File("D:\\new"));           FileUtils.deleteDirectory(new File("D:\\new"));          
//JDK1.7 自己也做了一些一行代码完成复制的操作:New IO的技术          
Files.copy(Path.of("D:\\resources\\hushui.jpeg"), Path.of("D:\\resources\\hushui3.jpeg"));
```

# 52.多线程

**软硬件上执行多条执行流程得技术**

## 1.方式一：继承Thread类

![线程创建方式一](.\img\线程创建方式一.png)

```java
public static void main(String[] args) {        
    // 3、new一个新线程对象        
    Thread t = new MyThread();        
    // 4、调用start方法启动线程（执行的还是run方法）        
    t.start();        
    for (int i = 0; i < 5; i++) {            
        System.out.println("主线程执行输出：" + i);        
    }    
}
}
/**   1、定义一个线程类继承Thread类 */
class MyThread extends Thread{    
    /**       2、重写run方法，里面是定义线程以后要干啥     */    
    @Override    
    public void run() {        
        for (int i = 0; i < 5; i++) {            
            System.out.println("子线程执行输出：" + i);        
        }    
    }
```

![线程方式一注意](.\img\线程方式一注意.png)

![线程方式一的总结](.\img\线程方式一的总结.png)

## 2.方式二：实现Runnable

### 1.接口方式

  ![多线程实现方式二](.\img\多线程实现方式二.png)

```java
public static void main(String[] args) {        
    // 3、创建一个任务对象        
    Runnable target = new MyRunnable();        
    // 4、把任务对象交给Thread处理        
    Thread t = new Thread(target);        
    // Thread t = new Thread(target, "1号");        
    // 5、启动线程        
    t.start();        
    for (int i = 0; i < 10; i++) {            
        System.out.println("主线程执行输出：" + i);        
    }    
}
}
/**   1、定义一个线程任务类 实现Runnable接口 */
class MyRunnable  implements Runnable {    
    /**       2、重写run方法，定义线程的执行任务的     */    
    @Override    
    public void run() {        
        for (int i = 0; i < 10; i++) {            
            System.out.println("子线程执行输出：" + i);        
        }    
    }
```

![线程方式二的优缺点](.\img\线程方式二的优缺点.png)

![线程创建方式二总结](.\img\线程创建方式二总结.png)

### 2.匿名内部类方式

![线程创建方式二-匿名内部类](.\img\线程创建方式二-匿名内部类.png)

```java
Runnable target = new Runnable() {    
    @Override    
    public void run() {        
        for (int i = 0; i < 10; i++) {            
            System.out.println("子线程1执行输出：" + i);        
        }    
    }
};
Thread t = new Thread(target);
t.start();
new Thread(new Runnable() {    
    @Override    
    public void run() {        
        for (int i = 0; i < 10; i++) {            
            System.out.println("子线程2执行输出：" + i);        
        }    
    }
}).start();new Thread(() -> {        
    for (int i = 0; i < 10; i++) {            
        System.out.println("子线程3执行输出：" + i);    
    }
}).start();
for (int i = 0; i < 10; i++) {    
    System.out.println("主线程执行输出：" + i);
}
```

## 3.方式三：JDK5.0新增：实现Callable接口

![前两种方法存在的问题](.\img\前两种方法存在的问题.png)

![多线程实现方式三](.\img\多线程实现方式三.png)

```java
 // 3、创建Callable任务对象        
Callable<String> call = new MyCallable(100);        
// 4、把Callable任务对象 交给 FutureTask 对象        
//  FutureTask对象的作用1： 是Runnable的对象（实现了Runnable接口），可以交给Thread了        
//  FutureTask对象的作用2： 可以在线程执行完毕之后通过调用其get方法得到线程执行完成的结果        
FutureTask<String> f1 = new FutureTask<>(call);        
// 5、交给线程处理        
Thread t1 = new Thread(f1);        
// 6、启动线程        
t1.start();        
Callable<String> call2 = new MyCallable(200);        
FutureTask<String> f2 = new FutureTask<>(call2);        
Thread t2 = new Thread(f2);        
t2.start();        
try {            
    // 如果f1任务没有执行完毕，这里的代码会等待，直到线程1跑完才提取结果。            
    String rs1 = f1.get();            
    System.out.println("第一个结果：" + rs1);        
} catch (Exception e) {            
    e.printStackTrace();        
}        
try {            
    // 如果f2任务没有执行完毕，这里的代码会等待，直到线程2跑完才提取结果。            
    String rs2 = f2.get();            
    System.out.println("第二个结果：" + rs2);        
} catch (Exception e) {            
    e.printStackTrace();        
}    
}
}
/**    1、定义一个任务类 实现Callable接口  应该申明线程任务执行完毕后的结果的数据类型 */
class MyCallable implements Callable<String>{   
    private int n;    
    public MyCallable(int n) {        
        this.n = n;    
    }    
    /**       2、重写call方法（任务方法）     */    
    @Override    
    public String call() throws Exception {        
        int sum = 0;        
        for (int i = 1; i <= n ; i++) {           
            sum += i;        
        }        
        return "子线程执行的结果是：" + sum;   
    }
```

![线程方式三的总结](.\img\线程方式三的总结.png)

## 4.线程三种方式的总结

![线程三种方式的总结](.\img\线程三种方式的总结.png)

## 5.Thread常用方法

![获得线程名字](.\img\获得线程名字.png)

![线程获得当前线程](.\img\线程获得当前线程.png)

![Thread构造器](.\img\Thread构造器.png)

```java
// main方法是由主线程负责调度的
public static void main(String[] args) {    
    Thread t1 = new MyThread("1号");    
    // t1.setName("1号");    
    t1.start();    
    System.out.println(t1.getName());    
    Thread t2 = new MyThread("2号");    
    // t2.setName("2号");    
    t2.start();    
    System.out.println(t2.getName());    
    // 哪个线程执行它，它就得到哪个线程对象（当前线程对象）    
    // 主线程的名称就叫main    
    Thread m = Thread.currentThread();    
    System.out.println(m.getName());    
    m.setName("最牛的线程");    
    for (int i = 0; i < 5; i++) {        
        System.out.println( m.getName() + "输出：" + i);    
    }
}
```

```java
public class MyThread extends Thread{    public MyThread() {    }    public MyThread(String name) {        // 为当前线程对象设置名称，送给父类的有参数构造器初始化名称        super(name);    }    @Override    public void run() {        for (int i = 0; i < 5; i++) {            System.out.println( Thread.currentThread().getName() + "输出：" + i);        }    }}
```

![Thread类休眠](.\img\Thread类休眠.png)

## 6.线程安全

### 1.概述

**多线程同时操作一个共享资源**可能会出现业务安全问题，称为线程安全问题

线程安全出现的原因

1.存在多线程并发

2.同时访问共享资源

3.存在修改共同资源

### 2.线程安全模拟案例

```java
public class DrawThread extends Thread {    
    // 接收处理的账户对象    
    private Account acc;    
    public DrawThread(Account acc,String name){        
        super(name);        
        this.acc = acc;    
    }    
    @Override    
    public void run() {        
        // 小明 小红：取钱        
        acc.drawMoney(100000);    
    }
}
```

```java
public class ThreadDemo {    
    public static void main(String[] args) {        
        // 1、定义线程类，创建一个共享的账户对象        
        Account acc = new Account("ICBC-111", 100000);        
        // 2、创建2个线程对象，代表小明和小红同时进来了。        
        new DrawThread(acc, "小明").start();        
        new DrawThread(acc, "小红").start();    
    }
}
```

```java
public class Account {    
    private String cardId;    
    private double money; // 账户的余额    
    public Account(){    
    }    
    public Account(String cardId, double money) {        
        this.cardId = cardId;        
        this.money = money;    
    }    
    /**       小明 小红     */    
    public void drawMoney(double money) {        
        // 0、先获取是谁来取钱，线程的名字就是人名        
        String name = Thread.currentThread().getName();        
        // 1、判断账户是否够钱        
        if(this.money >= money){            
            // 2、取钱            
            System.out.println(name + "来取钱成功，吐出：" + money);            
            // 3、更新余额            
            this.money -= money;           
            System.out.println(name + "取钱后剩余：" + this.money);        
        }else {            
            // 4、余额不足            
            System.out.println(name +"来取钱，余额不足！");        
        }   
    }   
    public String getCardId() {    
        return cardId;  
    }   
    public void setCardId(String cardId) {    
        this.cardId = cardId;  
    }   
    public double getMoney() {     
        return money; 
    }    
    public void setMoney(double money) {     
        this.money = money;  
    }
}
```

## 7.**线程同步**（synchronized）

解决多线程安全问题，加锁解决

**加锁**：让线程依次访问共享资源

### 1.方式一：同步代码块

#### 1.概述

![同步代码块](.\img\同步代码块.png)

```java
public void drawMoney(double money) {    
    // 1、拿到是谁来取钱    
    String name = Thread.currentThread().getName();    
    // 同步代码块    
    // 小明 小红    
    // this == acc 共享账户    
    synchronized (this) {        
        // 2、判断余额是否足够        
        if(this.money >= money){            
            // 钱够了            
            System.out.println(name+"来取钱，吐出：" + money);            
            // 更新余额            
            this.money -= money;            
            System.out.println(name+"取钱后，余额剩余：" + this.money);        
        }else{            
            // 3、余额不足            
            System.out.println(name+"来取钱，余额不足！");        
        }    
    }
}
```

![取钱](.\img\取钱.png)

#### 2.对象锁的规范要求

![对象锁的规范要求](.\img\对象锁的规范要求.png)

#### 3.小结

![线程安全方式一小结](.\img\线程安全方式一小结.png)

### 2.方式二：同步方法

![同步方法](.\img\同步方法.png)

```java
/**      小明 小红       this == acc*/
public synchronized void drawMoney(double money) {    
    // 1、拿到是谁来取钱    
    String name = Thread.currentThread().getName();    
    // 2、判断余额是否足够    
    // 小明  小红    
    if(this.money >= money){        
        // 钱够了        
        System.out.println(name+"来取钱，吐出：" + money);        
        // 更新余额        
        this.money -= money;        
        System.out.println(name+"取钱后，余额剩余：" + this.money);    
    }else{        
        // 3、余额不足        
        System.out.println(name+"来取钱，余额不足！");    
    }
}
```

![同步方法底层原理](.\img\同步方法底层原理.png)

![同步方法小结](.\img\同步方法小结.png)

### 3.方式三：Lock锁

![Lock锁](.\img\Lock锁.png)

```java
public class Account {    
    private String cardId;    
    private double money; // 余额 关键信息    
    // final修饰后：锁对象是唯一和不可替换的，非常专业    
    private final Lock lock = new ReentrantLock();    
    public Account() {    }    
    public Account(String cardId, double money) {        
        this.cardId = cardId;        
        this.money = money;    
    }    
    public String getCardId() {        return cardId;    }    
    public void setCardId(String cardId) {        this.cardId = cardId;    }    
    public double getMoney() {        return money;    }    
    public void setMoney(double money) {        this.money = money;    }    
    /**      小明 小红     */    
    public void drawMoney(double money) {        
        // 1、拿到是谁来取钱        
        String name = Thread.currentThread().getName();       
        // 2、判断余额是否足够        
        // 小明  小红        
        lock.lock(); // 上锁       
        try {            
            if(this.money >= money){                
                // 钱够了                
                System.out.println(name+"来取钱，吐出：" + money);                
                // 更新余额                
                this.money -= money;                
                System.out.println(name+"取钱后，余额剩余：" + this.money);            
            }else{                
                // 3、余额不足                
                System.out.println(name+"来取钱，余额不足！");            
            }        
        } finally {            
            lock.unlock(); // 解锁        
        }   
    }
}
```

## 8.线程通信

![Object类的等待和唤醒方法](.\img\Object类的等待和唤醒方法.png)

```java
// 定义一个变量记录当前呼入进来的电话。
public static int number = 0; // 最多只接听一个。
/* 接入电话 */
public synchronized static void call() {    
    try {        
        number++;        
        System.out.println("成功接入一个用户，等待分发~~~~");        
        // 唤醒别人 : 1个        
        CallSystem.class.notify();        
        // 让当前线程对象进入等待状态。        
        CallSystem.class.wait();    
    } catch (InterruptedException e) {        
        e.printStackTrace();    
    }
}
/**   分发电话 */
public synchronized static void receive() {    
    try {        
        String name = Thread.currentThread().getName();        
        if(number == 1){           
            System.out.println(name + "此电话已经分发给客服并接听完毕了~~~~~");           
            number--;            
            // 唤醒别人 : 1个            
            CallSystem.class.notify();            
            CallSystem.class.wait(); // 让当前线程等待        
        }else {            
            // 唤醒别人 : 1个           
            CallSystem.class.notify();            
            CallSystem.class.wait(); // 让当前线程等待        
        }    
    } catch (InterruptedException e) {        
        e.printStackTrace();    
    }
```

# 53.线程池

## 1.概述

线程池就是一个**可以复用线程的技术**

![得到线程池](.\img\得到线程池.png)

### 1.ThreadPoolExecutor

#### 1.概述

![ThreadPoolExecutor](.\img\ThreadPoolExecutor.png)

#### 2.常见问题

![线程常见问题](.\img\线程常见问题.png)

## 2.线程ExecutorService常用方法

![线程ExecutorService常用方法](.\img\线程ExecutorService常用方法.png)

### 2.线程处理Runnable任务

```java
 // 1、创建线程池对象        /**         public ThreadPoolExecutor(int corePoolSize,                                 int maximumPoolSize,                                 long keepAliveTime,                                 TimeUnit unit,                                 BlockingQueue<Runnable> workQueue,                                 ThreadFactory threadFactory,                                 RejectedExecutionHandler handler)         */        ExecutorService pool = new ThreadPoolExecutor(3, 5 ,                6, TimeUnit.SECONDS, new ArrayBlockingQueue<>(5) , Executors.defaultThreadFactory(),               new ThreadPoolExecutor.AbortPolicy() );        // 2、给任务线程池处理。        Runnable target = new MyRunnable();        pool.execute(target);        pool.execute(target);        pool.execute(target);        pool.execute(target);        pool.execute(target);        pool.execute(target);        pool.execute(target);        pool.execute(target);        // 创建临时线程        pool.execute(target);        pool.execute(target);//        // 不创建，拒绝策略被触发！！！//        pool.execute(target);        // 关闭线程池（开发中一般不会使用）。        // pool.shutdownNow(); // 立即关闭，即使任务没有完成，会丢失任务的！        pool.shutdown(); // 会等待全部任务执行完毕之后再关闭（建议使用的）
```

#### 拒绝任务策略

![新任务拒绝策略](.\img\新任务拒绝策略.png)

## 3.线程处理Callable任务

```java
// 1、创建线程池对象        /**         public ThreadPoolExecutor(int corePoolSize,                                 int maximumPoolSize,                                 long keepAliveTime,                                 TimeUnit unit,                                 BlockingQueue<Runnable> workQueue,                                 ThreadFactory threadFactory,                                 RejectedExecutionHandler handler)         */        ExecutorService pool = new ThreadPoolExecutor(3, 5 ,                6, TimeUnit.SECONDS, new ArrayBlockingQueue<>(5) , Executors.defaultThreadFactory(),               new ThreadPoolExecutor.AbortPolicy() );        // 2、给任务线程池处理。        Future<String> f1 = pool.submit(new MyCallable(100));        Future<String> f2 = pool.submit(new MyCallable(200));        Future<String> f3 = pool.submit(new MyCallable(300));        Future<String> f4 = pool.submit(new MyCallable(400));        Future<String> f5 = pool.submit(new MyCallable(500));//        String rs = f1.get();//        System.out.println(rs);        System.out.println(f1.get());        System.out.println(f2.get());        System.out.println(f3.get());        System.out.println(f4.get());        System.out.println(f5.get());
```

```java
public class MyCallable implements Callable<String>{    private int n;    public MyCallable(int n) {        this.n = n;    }    /**       2、重写call方法（任务方法）     */    @Override    public String call() throws Exception {        int sum = 0;        for (int i = 1; i <= n ; i++) {            sum += i;        }        return Thread.currentThread().getName()                + "执行 1-" + n+ "的和，结果是：" + sum;    }}
```

## 4.Executor工具类实现线程池

![Executors常用方法](.\img\Executors常用方法.png)

```java
// 1、创建固定线程数据的线程池ExecutorService pool = Executors.newFixedThreadPool(3);pool.execute(new MyRunnable());pool.execute(new MyRunnable());pool.execute(new MyRunnable());pool.execute(new MyRunnable()); // 已经没有多余线程了
```

![Executors存在问题](.\img\Executors存在问题.png)

![阿里巴巴开发规约](.\img\阿里巴巴开发规约.png)

# 54.定时器

![定时器](.\img\定时器.png)

## 1.Timer定时器

![定时器API](.\img\定时器API.png)

```java
// 1、创建Timer定时器        Timer timer = new Timer();  // 定时器本身就是一个单线程。        // 2、调用方法，处理定时任务        timer.schedule(new TimerTask() {            @Override            public void run() {                System.out.println(Thread.currentThread().getName() + "执行AAA~~~" + new Date());//                try {//                    Thread.sleep(5000);//                } catch (InterruptedException e) {//                    e.printStackTrace();//                }            }        }, 0, 2000);        timer.schedule(new TimerTask() {            @Override            public void run() {                System.out.println(Thread.currentThread().getName() + "执行BB~~~"+ new Date());                System.out.println(10/0);            }        }, 0, 2000);        timer.schedule(new TimerTask() {            @Override            public void run() {                System.out.println(Thread.currentThread().getName() + "执行CCC~~~"+ new Date());            }        }, 0, 3000);
```

## 2.ScheduledExecutorService定时器

![ScheduledExecutorService定时器](.\img\ScheduledExecutorService定时器.png)

```java
// 1、创建ScheduledExecutorService线程池，做定时器ScheduledExecutorService pool = Executors.newScheduledThreadPool(3);// 2、开启定时任务pool.scheduleAtFixedRate(new TimerTask() {    @Override    public void run() {        System.out.println(Thread.currentThread().getName() + "执行输出：AAA  ==》 " + new Date());        try {            Thread.sleep(100000);        } catch (InterruptedException e) {            e.printStackTrace();        }    }}, 0, 2, TimeUnit.SECONDS);pool.scheduleAtFixedRate(new TimerTask() {    @Override    public void run() {        System.out.println(Thread.currentThread().getName() + "执行输出：BBB  ==》 " + new Date());        System.out.println(10 / 0);    }}, 0, 2, TimeUnit.SECONDS);pool.scheduleAtFixedRate(new TimerTask() {    @Override    public void run() {        System.out.println(Thread.currentThread().getName() + "执行输出：CCC  ==》 " + new Date());    }}, 0, 2, TimeUnit.SECONDS);
```

# 55.并发、并行

## 1.并发

![并发](.\img\并发.png)

## 2.并行

![并行](.\img\并行.png)

## 3.总结

![并发并行的总结](.\img\并发并行的总结.png)

# 56.线程的生命周期

![线程的状态](.\img\线程的状态.png)

![线程的六种状态](.\img\线程的六种状态.png)

![线程的六种状态总结](.\img\线程的六种状态总结.png)

# 57.网络编程

常见的两种通信模式：Client-Server（C/S）、Browser/Server（B/S）

## 1.CS模式

![CS模式](.\img\CS模式.png)

## 2.BS模式

![BS模式](.\img\BS模式.png)

# 58.网络通信三要素

![网络三要素](.\img\网络三要素.png)

## 1.IP地址

### 1.概述

![IP地址](.\img\IP地址.png)

![IPv6](.\img\IPv6.png)

![IP简介](.\img\IP简介.png)

### 2.InetAddress的使用

![InetAddress的使用](.\img\InetAddress的使用.png)

```java
// 1.获取本机地址对象。
InetAddress ip1 = InetAddress.getLocalHost();
System.out.println(ip1.getHostName());
System.out.println(ip1.getHostAddress());
// 2.获取域名ip对象
InetAddress ip2 = InetAddress.getByName("www.baidu.com");
System.out.println(ip2.getHostName());
System.out.println(ip2.getHostAddress());
// 3.获取公网IP对象。
InetAddress ip3 = InetAddress.getByName("112.80.248.76");
System.out.println(ip3.getHostName());
System.out.println(ip3.getHostAddress());
// 4.判断是否能通： ping  5s之前测试是否可通
System.out.println(ip3.isReachable(5000));
```

## 2.端口号

![端口号简介](.\img\端口号简介.png)

## 3.协议

![协议](.\img\协议.png)

### 1.常见的两个协议TCP

![常见的两个协议TCP](.\img\常见的两个协议TCP.png)



#### 1.TCP三次握手

![TCP三次握手](.\img\TCP三次握手.png)

#### 2.TCP四次挥手

![TCP四次挥手](.\img\TCP四次挥手.png)

### 2.UDP简介

![UDP协议](.\img\UDP协议.png)

### 3.总结

![通信协议总结](.\img\通信协议总结.png)

![通信协议总结2](.\img\通信协议总结2.png)

## 4.UDP

![DatagramPacket](.\img\DatagramPacket.png)

![DatagramPacket常用方法](.\img\DatagramPacket常用方法.png)

![DatagramSocket](.\img\DatagramSocket.png)

### 1.一对一发送 

```java
System.out.println("=====客户端启动======");
// 1、创建发送端对象：发送端自带默认的端口号（人）
DatagramSocket socket = new DatagramSocket(6666);
// 2、创建一个数据包对象封装数据（韭菜盘子）
/** 
public DatagramPacket(byte buf[], int length, InetAddress address, int port) 
参数一：封装要发送的数据（韭菜） 参数二：发送数据的大小 参数三：服务端的主机IP地址 参数四：服务端的端口 */
byte[] buffer = "我是一颗快乐的韭菜，你愿意吃吗？".getBytes();
DatagramPacket packet = new DatagramPacket( buffer, buffer.length,        InetAddress.getLocalHost() , 8888);
// 3、发送数据出去
socket.send(packet);
socket.close();
```

```java
System.out.println("=====服务端启动======");// 1、创建接收端对象：注册端口（人）DatagramSocket socket = new DatagramSocket(8888);// 2、创建一个数据包对象接收数据（韭菜盘子）byte[] buffer = new byte[1024 * 64];DatagramPacket packet = new DatagramPacket(buffer, buffer.length);// 3、等待接收数据。socket.receive(packet);// 4、取出数据即可// 读取多少倒出多少int len = packet.getLength();String rs = new String(buffer,0, len);System.out.println("收到了：" + rs);// 获取发送端的ip和端口String ip  =packet.getSocketAddress().toString();System.out.println("对方地址：" + ip);int port  = packet.getPort();System.out.println("对方端口：" + port);socket.close();
```

![UDP小结](.\img\UDP小结.png)

### 2.多对多发送

```java
System.out.println("=====客户端启动======");

// 1、创建发送端对象：发送端自带默认的端口号（人）
DatagramSocket socket = new DatagramSocket(7777);


Scanner sc = new Scanner(System.in);
while (true) {
    System.out.println("请说：");
    String msg = sc.nextLine();

    if("exit".equals(msg)){
        System.out.println("离线成功！");
        socket.close();
        break;
    }

    // 2、创建一个数据包对象封装数据（韭菜盘子）
    byte[] buffer = msg.getBytes();
    DatagramPacket packet = new DatagramPacket( buffer, buffer.length,
            InetAddress.getLocalHost() , 8888);

    // 3、发送数据出去
    socket.send(packet);
}
```

```java
System.out.println("=====服务端启动======");
// 1、创建接收端对象：注册端口（人）
DatagramSocket socket = new DatagramSocket(8888);

// 2、创建一个数据包对象接收数据（韭菜盘子）
byte[] buffer = new byte[1024 * 64];
DatagramPacket packet = new DatagramPacket(buffer, buffer.length);

while (true) {
    // 3、等待接收数据。
    socket.receive(packet);
    // 4、取出数据即可
    // 读取多少倒出多少
    int len = packet.getLength();
    String rs = new String(buffer,0, len);
    System.out.println("收到了来自：" + packet.getAddress() +", 对方端口是" + packet.getPort() +"的消息：" + rs);
}
```

### 3.UDP广播、组播

![UDP广播、组播](.\img\UDP广播、组播.png)

#### 1.广播

![UDP广播](.\img\UDP广播.png)

#### 2.组播

![UDP组播](.\img\UDP组播.png)

## 5.TCP

![TCP通信演示](.\img\TCP通信演示.png)

### 1.单发单收

#### 1.Socket

![Socket](.\img\Socket.png)

####  2.ServerSocket

![Server](.\img\Server.png)

```java
try {    System.out.println("====客户端启动===");    // 1、创建Socket通信管道请求有服务端的连接    // public Socket(String host, int port)    // 参数一：服务端的IP地址    // 参数二：服务端的端口    Socket socket = new Socket("127.0.0.1", 7777);    // 2、从socket通信管道中得到一个字节输出流 负责发送数据    OutputStream os = socket.getOutputStream();    // 3、把低级的字节流包装成打印流    PrintStream ps = new PrintStream(os);    // 4、发送消息    ps.println("我是TCP的客户端，我已经与你对接，并发出邀请：约吗？");    ps.flush();    // 关闭资源。    // socket.close();} catch (Exception e) {    e.printStackTrace();}
```

```java
try {    System.out.println("===服务端启动成功===");    // 1、注册端口    ServerSocket serverSocket = new ServerSocket(7777);    // 2、必须调用accept方法：等待接收客户端的Socket连接请求，建立Socket通信管道    Socket socket = serverSocket.accept();    // 3、从socket通信管道中得到一个字节输入流    InputStream is = socket.getInputStream();    // 4、把字节输入流包装成缓冲字符输入流进行消息的接收    BufferedReader br = new BufferedReader(new InputStreamReader(is));    // 5、按照行读取消息    String msg;    if ((msg = br.readLine()) != null){        System.out.println(socket.getRemoteSocketAddress() + "说了：: " + msg);    }} catch (Exception e) {    e.printStackTrace();}
```

#### 3.小结

![Socket小结](.\img\Socket小结.png)

```java
try {    System.out.println("====客户端启动===");    // 1、创建Socket通信管道请求有服务端的连接    // public Socket(String host, int port)    // 参数一：服务端的IP地址    // 参数二：服务端的端口    Socket socket = new Socket("127.0.0.1", 7777);    // 2、从socket通信管道中得到一个字节输出流 负责发送数据    OutputStream os = socket.getOutputStream();    // 3、把低级的字节流包装成打印流    PrintStream ps = new PrintStream(os);    Scanner sc =  new Scanner(System.in);    while (true) {        System.out.println("请说：");        String msg = sc.nextLine();        // 4、发送消息        ps.println(msg);        ps.flush();    }    // 关闭资源。    // socket.close();} catch (Exception e) {    e.printStackTrace();}
```

```java
try {    System.out.println("===服务端启动成功===");    // 1、注册端口    ServerSocket serverSocket = new ServerSocket(7777);    while (true) {        // 2、必须调用accept方法：等待接收客户端的Socket连接请求，建立Socket通信管道        Socket socket = serverSocket.accept();        // 3、从socket通信管道中得到一个字节输入流        InputStream is = socket.getInputStream();        // 4、把字节输入流包装成缓冲字符输入流进行消息的接收        BufferedReader br = new BufferedReader(new InputStreamReader(is));        // 5、按照行读取消息        String msg;        while ((msg = br.readLine()) != null){            System.out.println(socket.getRemoteSocketAddress() + "说了：: " + msg);        }    }} catch (Exception e) {    e.printStackTrace();}
```

### 2.多发多收

**利用多线程技术**

![多线程通信框架](.\img\多线程通信框架.png)

```java
try {    System.out.println("====客户端启动===");    // 1、创建Socket通信管道请求有服务端的连接    // public Socket(String host, int port)    // 参数一：服务端的IP地址    // 参数二：服务端的端口    Socket socket = new Socket("127.0.0.1", 7777);    // 2、从socket通信管道中得到一个字节输出流 负责发送数据    OutputStream os = socket.getOutputStream();    // 3、把低级的字节流包装成打印流    PrintStream ps = new PrintStream(os);    Scanner sc =  new Scanner(System.in);    while (true) {        System.out.println("请说：");        String msg = sc.nextLine();        // 4、发送消息        ps.println(msg);        ps.flush();    }    // 关闭资源。    // socket.close();} catch (Exception e) {    e.printStackTrace();}
```

```java
try {
    System.out.println("===服务端启动成功===");
    // 1、注册端口
    ServerSocket serverSocket = new ServerSocket(7777);
    // a.定义一个死循环由主线程负责不断的接收客户端的Socket管道连接。
    while (true) {
        // 2、每接收到一个客户端的Socket管道，交给一个独立的子线程负责读取消息
        Socket socket = serverSocket.accept();
        System.out.println(socket.getRemoteSocketAddress()+ "它来了，上线了！");
        // 3、开始创建独立线程处理socket
        new ServerReaderThread(socket).start();
    }
} catch (Exception e) {
    e.printStackTrace();
}
```

```java
public class ServerReaderThread extends Thread{
    private Socket socket;
    public ServerReaderThread(Socket socket){
        this.socket = socket;
    }
    @Override
    public void run() {
        try {
            // 3、从socket通信管道中得到一个字节输入流
            InputStream is = socket.getInputStream();
            // 4、把字节输入流包装成缓冲字符输入流进行消息的接收
            BufferedReader br = new BufferedReader(new InputStreamReader(is));
            // 5、按照行读取消息
            String msg;
            while ((msg = br.readLine()) != null){
                System.out.println(socket.getRemoteSocketAddress() + "说了：: " + msg);
            }
        } catch (Exception e) {
            System.out.println(socket.getRemoteSocketAddress() + "下线了！！！");
        }
    }
}
```

![多线程接受消息小结](.\img\多线程接受消息小结.png)

### 3.优化多收多发

![优化多线程通信](.\img\优化多线程通信.png)

```java
try {    System.out.println("====客户端启动===");    // 1、创建Socket通信管道请求有服务端的连接    // public Socket(String host, int port)    // 参数一：服务端的IP地址    // 参数二：服务端的端口    Socket socket = new Socket("127.0.0.1", 6666);    // 2、从socket通信管道中得到一个字节输出流 负责发送数据    OutputStream os = socket.getOutputStream();    // 3、把低级的字节流包装成打印流    PrintStream ps = new PrintStream(os);    Scanner sc =  new Scanner(System.in);    while (true) {        System.out.println("请说：");        String msg = sc.nextLine();        // 4、发送消息        ps.println(msg);        ps.flush();    }    // 关闭资源。    // socket.close();} catch (Exception e) {    e.printStackTrace();}
```

```java
public class ServerDemo2 {    // 使用静态变量记住一个线程池对象    private static ExecutorService pool = new ThreadPoolExecutor(300,            1500, 6, TimeUnit.SECONDS,            new ArrayBlockingQueue<>(2)    , Executors.defaultThreadFactory(), new ThreadPoolExecutor.AbortPolicy());    public static void main(String[] args) {        try {            System.out.println("===服务端启动成功===");            // 1、注册端口            ServerSocket serverSocket = new ServerSocket(6666);            // a.定义一个死循环由主线程负责不断的接收客户端的Socket管道连接。            while (true) {                // 2、每接收到一个客户端的Socket管道，                Socket socket = serverSocket.accept();                System.out.println(socket.getRemoteSocketAddress()+ "它来了，上线了！");                // 任务对象负责读取消息。                Runnable target = new ServerReaderRunnable(socket);                pool.execute(target);            }        } catch (Exception e) {            e.printStackTrace();        }    }}
```

```java
public class ServerReaderRunnable implements Runnable{    private Socket socket;    public ServerReaderRunnable(Socket socket){        this.socket = socket;    }    @Override    public void run() {        try {            // 3、从socket通信管道中得到一个字节输入流            InputStream is = socket.getInputStream();            // 4、把字节输入流包装成缓冲字符输入流进行消息的接收            BufferedReader br = new BufferedReader(new InputStreamReader(is));            // 5、按照行读取消息            String msg;            while ((msg = br.readLine()) != null){                System.out.println(socket.getRemoteSocketAddress() + "说了：: " + msg);            }        } catch (Exception e) {            System.out.println(socket.getRemoteSocketAddress() + "下线了！！！");        }    }}
```

![多线程通信优化总结](.\img\多线程通信优化总结.png)

# 59.单元测试

**针对java方法得测试**

## 1.Junit单元测试框架

![Junit](.\img\Junit.png)

![单元测试方法步骤](.\img\单元测试方法步骤.png)

```java
public class TestUserService {    /**       测试方法       注意点：            1、必须是公开的，无参数 无返回值的方法            2、测试方法必须使用@Test注解标记。     */    @Test    public void testLoginName(){        UserService userService = new UserService();        String rs = userService.loginName("admin","123456");        // 进行预期结果的正确性测试：断言。        Assert.assertEquals("您的登录业务可能出现问题", "登录成功", rs );    }    @Test    public void testSelectNames(){        UserService userService = new UserService();        userService.selectNames();    }}
```

![Junit小结](.\img\Junit小结.png)

## 2.Junit常用注解

![Junit常用注解](.\img\Junit常用注解.png)

```java
public class TestUserService {    // 修饰实例方法的    @Before    public void before(){        System.out.println("===before方法执行一次===");    }    @After    public void after(){        System.out.println("===after方法执行一次===");    }    // 修饰静态方法    @BeforeClass    public static void beforeClass(){        System.out.println("===beforeClass方法执行一次===");    }    @AfterClass    public static void afterClass(){        System.out.println("===afterClass方法执行一次===");    }    /**       测试方法       注意点：            1、必须是公开的，无参数 无返回值的方法            2、测试方法必须使用@Test注解标记。     */    @Test    public void testLoginName(){        UserService userService = new UserService();        String rs = userService.loginName("admin","123456");        // 进行预期结果的正确性测试：断言。        Assert.assertEquals("您的登录业务可能出现问题", "登录成功", rs );    }    @Test    public void testSelectNames(){        UserService userService = new UserService();        userService.selectNames();    }}
```

```java
public class UserService {    public String loginName(String loginName , String passWord){        if("admin".equals(loginName) && "123456".equals(passWord)){            return "登录成功";        }else {            return "用户名或者密码有问题";        }    }    public void selectNames(){        System.out.println(10/2);        System.out.println("查询全部用户名称成功~~");    }}
```

![Junit5常用注解](.\img\Junit5常用注解.png)

# 60.反射

## 1.概述

![反射的基本概述](.\img\反射的基本概述.png)

## 2.获取反射

### 1.获取Class对象

![反射的第一步](.\img\反射的第一步.png)

```java
public class Test {
    public static void main(String[] args) throws Exception {
        // 1、Class类中的一个静态方法：forName(全限名：包名 + 类名)
        Class c = Class.forName("com.itheima.d2_reflect_class.Student");
        System.out.println(c); // Student.class

        // 2、类名.class
        Class c1 = Student.class;
        System.out.println(c1);

        // 3、对象.getClass() 获取对象对应类的Class对象。
        Student s = new Student();
        Class c2 = s.getClass();
        System.out.println(c2);
    }
}
```

![反射第一步总结](.\img\反射第一步总结.png)

### 2.获取构造器对象

![反射获取构造器](.\img\反射获取构造器.png)

![反射获取构造器API](.\img\反射获取构造器API.png)

```java
public class Student {
    private String name;
    private int age;

    private Student(){
        System.out.println("无参数构造器执行！");
    }

    public Student(String name, int age) {
        System.out.println("有参数构造器执行！");
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "Student{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }
}
```

```java
public class TestStudent01 {
    // 1. getConstructors:
    // 获取全部的构造器：只能获取public修饰的构造器。
    // Constructor[] getConstructors()
    @Test
    public void getConstructors(){
        // a.第一步：获取类对象
        Class c = Student.class;
        // b.提取类中的全部的构造器对象(这里只能拿public修饰)
        Constructor[] constructors = c.getConstructors();
        // c.遍历构造器
        for (Constructor constructor : constructors) {
            System.out.println(constructor.getName() + "===>" + constructor.getParameterCount());
        }
    }


    // 2.getDeclaredConstructors():
    // 获取全部的构造器：只要你敢写，这里就能拿到，无所谓权限是否可及。
    @Test
    public void getDeclaredConstructors(){
        // a.第一步：获取类对象
        Class c = Student.class;
        // b.提取类中的全部的构造器对象
        Constructor[] constructors = c.getDeclaredConstructors();
        // c.遍历构造器
        for (Constructor constructor : constructors) {
            System.out.println(constructor.getName() + "===>" + constructor.getParameterCount());
        }
    }

    // 3.getConstructor(Class... parameterTypes)
    // 获取某个构造器：只能拿public修饰的某个构造器
    @Test
    public void getConstructor() throws Exception {
        // a.第一步：获取类对象
        Class c = Student.class;
        // b.定位单个构造器对象 (按照参数定位无参数构造器 只能拿public修饰的某个构造器)
        Constructor cons = c.getConstructor();
        System.out.println(cons.getName() + "===>" + cons.getParameterCount());
    }


    // 4.getConstructor(Class... parameterTypes)
    // 获取某个构造器：只要你敢写，这里就能拿到，无所谓权限是否可及。
    @Test
    public void getDeclaredConstructor() throws Exception {
        // a.第一步：获取类对象
        Class c = Student.class;
        // b.定位单个构造器对象 (按照参数定位无参数构造器)
        Constructor cons = c.getDeclaredConstructor();
        System.out.println(cons.getName() + "===>" + cons.getParameterCount());

        // c.定位某个有参构造器
        Constructor cons1 = c.getDeclaredConstructor(String.class, int.class);
        System.out.println(cons1.getName() + "===>" + cons1.getParameterCount());

    }
```

```java
public class TestStudent02 {
    // 1.调用构造器得到一个类的对象返回。
    @Test
    public void getDeclaredConstructor() throws Exception {
        // a.第一步：获取类对象
        Class c = Student.class;
        // b.定位单个构造器对象 (按照参数定位无参数构造器)
        Constructor cons = c.getDeclaredConstructor();
        System.out.println(cons.getName() + "===>" + cons.getParameterCount());

        // 如果遇到了私有的构造器，可以暴力反射
        cons.setAccessible(true); // 权限被打开

        Student s = (Student) cons.newInstance();
        System.out.println(s);

        System.out.println("-------------------");

        // c.定位某个有参构造器
        Constructor cons1 = c.getDeclaredConstructor(String.class, int.class);
        System.out.println(cons1.getName() + "===>" + cons1.getParameterCount());

        Student s1 = (Student) cons1.newInstance("孙悟空", 1000);
        System.out.println(s1);
    }


}
```

![反射构造器总结](.\img\反射构造器总结.png)

### 3.获取成员变量对象

![反射获取成员变量](.\img\反射获取成员变量.png)

![反射成员变量API](.\img\反射成员变量API.png)

```java
@Test
public void setField() throws Exception {
    // a.反射第一步，获取类对象
    Class c = Student.class;
    // b.提取某个成员变量
    Field ageF = c.getDeclaredField("age");

    ageF.setAccessible(true); // 暴力打开权限

    // c.赋值
    Student s = new Student();
    ageF.set(s , 18);  // s.setAge(18);
    System.out.println(s);

    // d、取值
    int age = (int) ageF.get(s);
    System.out.println(age);
```

```java
// a.定位Class对象
    Class c = Student.class;
    // b.定位全部成员变量
    Field[] fields = c.getDeclaredFields();
    // c.遍历一下
    for (Field field : fields) {
        System.out.println(field.getName() + "==>" + field.getType());
    }
}

/**
    2.获取某个成员变量对象 Field getDeclaredField(String name);
 */
@Test
public void getDeclaredField() throws Exception {
    // a.定位Class对象
    Class c = Student.class;
    // b.根据名称定位某个成员变量
    Field f = c.getDeclaredField("age");
    System.out.println(f.getName() +"===>" + f.getType());
}
```

![反射成员变量总结](.\img\反射成员变量总结.png)

### 4.获取方法对象

![反射获取方法](.\img\反射获取方法.png)

![反射方法执行](.\img\反射方法执行.png)

```java
@Test
public void getDeclaredMethods(){
    // a.获取类对象
    Class c = Dog.class;
    // b.提取全部方法；包括私有的
    Method[] methods = c.getDeclaredMethods();
    // c.遍历全部方法
    for (Method method : methods) {
        System.out.println(method.getName() +" 返回值类型：" + method.getReturnType() + " 参数个数：" + method.getParameterCount());
    }
}

/**
 * 2. 获取某个方法对象
 */
@Test
public void getDeclardMethod() throws Exception {
    // a.获取类对象
    Class c = Dog.class;
    // b.提取单个方法对象
    Method m = c.getDeclaredMethod("eat");
    Method m2 = c.getDeclaredMethod("eat", String.class);

    // 暴力打开权限了
    m.setAccessible(true);
    m2.setAccessible(true);

    // c.触发方法的执行
    Dog d = new Dog();
    // 注意：方法如果是没有结果回来的，那么返回的是null.
    Object result = m.invoke(d);
    System.out.println(result);

    Object result2 = m2.invoke(d, "骨头");
    System.out.println(result2);
}
```

```java
public class Dog {
    private String name ;
    public Dog(){
    }

    public Dog(String name) {
        this.name = name;
    }

    public void run(){
        System.out.println("狗跑的贼快~~");
    }

    private void eat(){
        System.out.println("狗吃骨头");
    }

    private String eat(String name){
        System.out.println("狗吃" + name);
        return "吃的很开心！";
    }

    public static void inAddr(){
        System.out.println("在黑马学习Java!");
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

}
```

![反射方法总结](.\img\反射方法总结.png)

## 3.反射的作用

### 1.绕过编译阶段为集合添加数据

![反射作用1](.\img\反射作用1.png)

```java
// 需求：反射实现泛型擦除后，加入其他类型的元素
ArrayList<String> lists1 = new ArrayList<>();
ArrayList<Integer> lists2 = new ArrayList<>();

System.out.println(lists1.getClass());
System.out.println(lists2.getClass());

System.out.println(lists1.getClass() ==  lists2.getClass());  // ArrayList.class

System.out.println("---------------------------");
ArrayList<Integer> lists3 = new ArrayList<>();
lists3.add(23);
lists3.add(22);
// lists3.add("黑马");

Class c = lists3.getClass(); // ArrayList.class  ===> public boolean add(E e)
// 定位c类中的add方法
Method add = c.getDeclaredMethod("add", Object.class);
boolean rs = (boolean) add.invoke(lists3, "黑马");
System.out.println(rs);

System.out.println(lists3);

ArrayList list4 = lists3;
list4.add("白马");
list4.add(false);
System.out.println(lists3);
```

![反射作用1小结](.\img\反射作用1小结.png)

### 2.通过框架的底层原理

```java
/**
 保存任意类型的对象
 * @param obj
 */
public static void save(Object obj){
    try (
            PrintStream ps = new PrintStream(new FileOutputStream("junit-reflect-annotation-proxy-app/src/data.txt", true));
    ){
        // 1、提取这个对象的全部成员变量：只有反射可以解决
        Class c = obj.getClass();  //   c.getSimpleName()获取当前类名   c.getName获取全限名：包名+类名
        ps.println("================" + c.getSimpleName() + "================");

        // 2、提取它的全部成员变量
        Field[] fields = c.getDeclaredFields();
        // 3、获取成员变量的信息
        for (Field field : fields) {
            String name = field.getName();
            // 提取本成员变量在obj对象中的值（取值）
            field.setAccessible(true);
            String value = field.get(obj) + "";
            ps.println(name  + "=" + value);
        }
    } catch (Exception e) {
        e.printStackTrace();
    }
}
```

## 4.反射的总结

![反射的总结](.\img\反射的总结.png)

# 61.注解

![注解的作用](.\img\注解的作用.png)

## 1.自定义注解

![自定义注解的格式](.\img\自定义注解的格式.png)

```java
@MyBook(name="《精通JavaSE》",authors = {"黑马", "dlei"} , price = 199.5)
//@Book(value = "/delete")
// @Book("/delete")
@Book(value = "/delete", price = 23.5)
//@Book("/delete")
public class AnnotationDemo1 {

    @MyBook(name="《精通JavaSE2》",authors = {"黑马", "dlei"} , price = 199.5)
    private AnnotationDemo1(){

    }

    @MyBook(name="《精通JavaSE1》",authors = {"黑马", "dlei"} , price = 199.5)
    public static void main(String[] args) {
        @MyBook(name="《精通JavaSE2》",authors = {"黑马", "dlei"} , price = 199.5)
        int age = 21;
    }
}
```

```java
public @interface MyBook {
    String name();
    String[] authors();
    double price();
}
```

## 2.元注解

![元注解的简介](.\img\元注解的简介.png)

![元注解的解释](.\img\元注解的解释.png)

```java
@Target({ElementType.METHOD,ElementType.FIELD}) // 元注解
@Retention(RetentionPolicy.RUNTIME) // 一直活着，在运行阶段这个注解也不消失
public @interface MyTest {
}
```

## 3.注解解析

![注解解析API](.\img\注解解析API.png)

```java
@Test
    public void parseClass(){
        // a.先得到类对象
        Class c = BookStore.class;
        // b.判断这个类上面是否存在这个注解
        if(c.isAnnotationPresent(Bookk.class)){
            //c.直接获取该注解对象
            Bookk book = (Bookk) c.getDeclaredAnnotation(Bookk.class);
            System.out.println(book.value());
            System.out.println(book.price());
            System.out.println(Arrays.toString(book.author()));
        }
    }

    @Test
    public void parseMethod() throws NoSuchMethodException {
        // a.先得到类对象
        Class c = BookStore.class;

        Method m = c.getDeclaredMethod("test");

        // b.判断这个类上面是否存在这个注解
        if(m.isAnnotationPresent(Bookk.class)){
            //c.直接获取该注解对象
            Bookk book = (Bookk) m.getDeclaredAnnotation(Bookk.class);
            System.out.println(book.value());
            System.out.println(book.price());
            System.out.println(Arrays.toString(book.author()));
        }
    }
}

@Bookk(value = "《情深深雨濛濛》", price = 99.9, author = {"琼瑶", "dlei"})
class BookStore{

    @Bookk(value = "《三少爷的剑》", price = 399.9, author = {"古龙", "熊耀华"})
    public void test(){
    }
}
```

## 4.注解在Junit中的使用

```java
public void test1(){
    System.out.println("===test1===");
}

@MyTest
public void test2(){
    System.out.println("===test2===");
}

@MyTest
public void test3(){
    System.out.println("===test3===");
}

/**
  启动菜单：有注解的才被调用。
 */
public static void main(String[] args) throws Exception {
    AnnotationDemo4 t = new AnnotationDemo4();
    // a.获取类对象
    Class c = AnnotationDemo4.class;
    // b.提取全部方法
    Method[] methods = c.getDeclaredMethods();
    // c.遍历方法，看是否有MyTest注解，有就跑它
    for (Method method : methods) {
        if(method.isAnnotationPresent(MyTest.class)){
            // 跑它
            method.invoke(t);
        }
    }
}
```

# 62.动态代理

**大量代码重复的情况下使用动态代理**

![动态代理的概述](.\img\动态代理的概述.png)

```java
/**
  生成业务对象的代理对象。
 * @param obj
 * @return
 */
public static <T> T  getProxy(T obj) {
    // 返回了一个代理对象了
    return (T)Proxy.newProxyInstance(obj.getClass().getClassLoader(),
            obj.getClass().getInterfaces(),
            new InvocationHandler() {
                @Override
                public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {
                    // 参数一：代理对象本身。一般不管
                    // 参数二：正在被代理的方法
                    // 参数三：被代理方法，应该传入的参数
                   long startTimer = System .currentTimeMillis();
                    // 马上触发方法的真正执行。(触发真正的业务功能)
                    Object result = method.invoke(obj, args);

                    long endTimer = System.currentTimeMillis();
                    System.out.println(method.getName() + "方法耗时：" + (endTimer - startTimer) / 1000.0 + "s");

                    // 把业务功能方法执行的结果返回给调用者
                    return result;
                }
            });
}
```

```java
// 1、把业务对象，直接做成一个代理对象返回，代理对象的类型也是 UserService类型
UserService userService = ProxyUtil.getProxy(new UserServiceImpl());
System.out.println(userService.login("admin", "1234"));
System.out.println(userService.deleteUsers());
userService.selectUsers();
userService.updateUsers(); // 走代理
```

```java
public interface UserService {
    String login(String loginName , String passWord) ;
    void selectUsers();
    boolean deleteUsers();
    void updateUsers();
}
```

```java
public class UserServiceImpl implements UserService{
    @Override
    public String login(String loginName, String passWord)  {
        try {
            Thread.sleep(1000);
        } catch (Exception e) {
            e.printStackTrace();
        }
        if("admin".equals(loginName) && "1234".equals(passWord)) {
            return "success";
        }
        return "登录名和密码可能有毛病";

    }

    @Override
    public void selectUsers() {
        System.out.println("查询了100个用户数据！");
        try {
            Thread.sleep(2000);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }

    @Override
    public boolean deleteUsers() {
        try {
            System.out.println("删除100个用户数据！");
            Thread.sleep(500);
            return true;
        } catch (Exception e) {
            e.printStackTrace();
            return false;
        }
    }

    @Override
    public void updateUsers() {
        try {
            System.out.println("修改100个用户数据！");
            Thread.sleep(2500);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

![动态代理的优点](.\img\动态代理的优点.png)

# 63.XML

![XML概述](.\img\XML概述.png)

## 1.XML文件的创建

![XML文件的创建](.\img\XML文件的创建.png)

![XML语法规则](.\img\XML语法规则.png)

![XML设计规范](.\img\XML设计规范.png)

![XML的其他格式](.\img\XML的其他格式.png)

![XML组成的总结](.\img\XML组成的总结.png)

## 2.XML的文档约束

**用来限制xml文件中的标签以及属性应该怎么写**

### 1.DTD

**无法约束数据类型**

![DTD](.\img\DTD.png)

### 2.schema

![schema](.\img\schema.png)

![schema1](.\img\schema1.png)

# 64.XML解析技术

sax：一行一行的读

dom：所有文件加载到内存中进行解析

![XML解析](.\img\XML解析.png)

![Dom常见的解析工具](.\img\Dom常见的解析工具.png)

## 1.DOM解析对象的模型

![DOM解析对象模型](.\img\DOM解析对象模型.png)

## 2.dom4j解析XML文件

![dom4j下载](.\img\dom4j下载.png)

![dom4j得到document对象](.\img\dom4j得到document对象.png)

![XML执行顺序](.\img\XML执行顺序.png)

![dom4j解析XMLAPI](.\img\dom4j解析XMLAPI.png)

```java
// 需求：解析XML中的数据成为一个List集合对象。
// 1、导入框架（做过）
// 2、创建SaxReader对象
SAXReader saxReader = new SAXReader();
// 3、加载XML文件成为文档对象Document对象。
Document document =
        saxReader.read(Dom4JTest2.class.getResourceAsStream("/Contacts.xml"));
// 4、先拿根元素
Element root = document.getRootElement();
// 5、提取contact子元素
List<Element> contactEles = root.elements("contact");
// 6、准备一个ArrayList集合封装联系人信息
List<Contact> contacts = new ArrayList<>();
// 7、遍历Contact子元素
for (Element contactEle : contactEles) {
    // 8、每个子元素都是一个联系人对象
    Contact contact = new Contact();
    contact.setId(Integer.valueOf(contactEle.attributeValue("id")));
    contact.setVip(Boolean.valueOf(contactEle.attributeValue("vip")));
    contact.setName(contactEle.elementTextTrim("name"));
    contact.setGender(contactEle.elementTextTrim("gender").charAt(0));
    contact.setEmail(contactEle.elementText("email"));
    // 9、把联系人对象数据加入到List集合
    contacts.add(contact);
}
// 10、遍历List集合
for (Contact contact : contacts) {
    System.out.println(contact);
}
```

## 3.XML检索技术：Xpath

![Xpath](.\img\Xpath.png)

```java
 /**
     1.绝对路径: /根元素/子元素/子元素。
     */
    @Test
    public void parse01() throws Exception {
        // a、创建解析器对象
        SAXReader saxReader = new SAXReader();
        // b、把XML加载成Document文档对象
        Document document =
                saxReader.read(XPathDemo.class.getResourceAsStream("/Contacts2.xml"));
        // c、检索全部的名称
        List<Node> nameNodes = document.selectNodes("/contactList/contact/name");
        for (Node nameNode : nameNodes) {
            Element  nameEle = (Element) nameNode;
            System.out.println(nameEle.getTextTrim());
        }
    }

    /**
     2.相对路径： ./子元素/子元素。 (.代表了当前元素)
     */
    @Test
    public void parse02() throws Exception {
        // a、创建解析器对象
        SAXReader saxReader = new SAXReader();
        // b、把XML加载成Document文档对象
        Document document =
                saxReader.read(XPathDemo.class.getResourceAsStream("/Contacts2.xml"));
        Element root = document.getRootElement();
        // c、检索全部的名称
        List<Node> nameNodes = root.selectNodes("./contact/name");
        for (Node nameNode : nameNodes) {
            Element  nameEle = (Element) nameNode;
            System.out.println(nameEle.getTextTrim());
        }
    }

    /**
     3.全文搜索：
     //元素  在全文找这个元素
     //元素1/元素2  在全文找元素1下面的一级元素2
     //元素1//元素2  在全文找元素1下面的全部元素2
     */
    @Test
    public void parse03() throws Exception {
        // a、创建解析器对象
        SAXReader saxReader = new SAXReader();
        // b、把XML加载成Document文档对象
        Document document =
                saxReader.read(XPathDemo.class.getResourceAsStream("/Contacts2.xml"));
        // c、检索数据
        //List<Node> nameNodes = document.selectNodes("//name");
        // List<Node> nameNodes = document.selectNodes("//contact/name");
        List<Node> nameNodes = document.selectNodes("//contact//name");
        for (Node nameNode : nameNodes) {
            Element  nameEle = (Element) nameNode;
            System.out.println(nameEle.getTextTrim());
        }
    }

    /**
     4.属性查找。
     //@属性名称  在全文检索属性对象。
     //元素[@属性名称]  在全文检索包含该属性的元素对象。
     //元素[@属性名称=值]  在全文检索包含该属性的元素且属性值为该值的元素对象。
     */
    @Test
    public void parse04() throws Exception {
        // a、创建解析器对象
        SAXReader saxReader = new SAXReader();
        // b、把XML加载成Document文档对象
        Document document =
                saxReader.read(XPathDemo.class.getResourceAsStream("/Contacts2.xml"));
        // c、检索数据
        List<Node> nodes = document.selectNodes("//@id");
        for (Node node : nodes) {
            Attribute attr = (Attribute) node;
            System.out.println(attr.getName() + "===>" + attr.getValue());
        }

        // 查询name元素（包含id属性的）
//      Node node = document.selectSingleNode("//name[@id]");
        Node node = document.selectSingleNode("//name[@id=888]");
        Element ele = (Element) node;
        System.out.println(ele.getTextTrim());
    }
```

# 65.设计模式

## 1.工厂模式

![工厂设计模式](.\img\工厂设计模式.png)

```java
Computer c1 = FactoryPattern.createComputer("huawei");
c1.start();

Computer c2 = FactoryPattern.createComputer("mac");
c2.start();
```

```java
public class FactoryPattern {
    /**
       定义一个方法，创建对象返回
     */
    public static Computer createComputer(String info){
        switch (info){
            case "huawei":
                Computer c = new Huawei();
                c.setName("huawei pro 16");
                c.setPrice(5999);
                return c;
            case "mac":
                Computer c2 = new Mac();
                c2.setName("MacBook pro");
                c2.setPrice(11999);
                return c2;
            default:
                return null;
        }
    }
}
```

![工厂模式的小结](.\img\工厂模式的小结.png)

## 2.装饰模式

![装饰模式](.\img\装饰模式.png)

```java
public class BufferedInputStream extends InputStream{
    private InputStream is;
    public BufferedInputStream(InputStream is){
        this.is = is;
    }
    @Override
    public int read() {
        System.out.println("提供8KB的缓冲区，提高读数据性能~~~~");
        return is.read();
    }

    @Override
    public int read(byte[] buffer) {
        System.out.println("提供8KB的缓冲区，提高读数据性能~~~~");
        return is.read(buffer);
    }
}
```

```java
public abstract class InputStream {
    public abstract int read();
    public abstract int read(byte[] buffer);
}
public class DecoratorPattern {
    public static void main(String[] args) {
        InputStream is = new BufferedInputStream(new FileInputStream());
        System.out.println(is.read());
        System.out.println(is.read(new byte[3]));
    }
}
```

```java
public abstract class InputStream {
    public abstract int read();
    public abstract int read(byte[] buffer);
}
public class DecoratorPattern {
    public static void main(String[] args) {
        InputStream is = new BufferedInputStream(new FileInputStream());
        System.out.println(is.read());
        System.out.println(is.read(new byte[3]));
    }
}
```

```java
/**
   原始类
 */
public class FileInputStream extends InputStream{
    @Override
    public int read() {
        System.out.println("低性能的方式读取了一个字节a");
        return 97;
    }

    @Override
    public int read(byte[] buffer) {
        buffer[0] = 97;
        buffer[1] = 98;
        buffer[2] = 99;
        System.out.println("低性能的方式读取了一个字节数组：" + Arrays.toString(buffer));
        return 3;
    }
}
```

![装饰模式的作用](.\img\装饰模式的作用.png)

