# 	什么是JavaWeb

![什么是JavaWeb](E:\笔记\JavaScriptimg\什么是JavaWeb.png)

![JavaWeb框架](E:\笔记\JavaWebimg\JavaWeb框架.png)

# 1.HTTP

![HTTP](E:\笔记\JavaWebimg\HTTP.png)

## 1.HTTP请求数据格式

![HTTP请求数据格式](E:\笔记\JavaWebimg\HTTP请求数据格式.png)

## 2.HTTP响应数据格式

![HTTP响应数据格式](E:\笔记\JavaWebimg\HTTP响应数据格式.png)

## 2.Web服务器(Tomcat)

![Tomcat](E:\笔记\JavaWebimg\Tomcat.png)

![Web服务器小结](E:\笔记\JavaWebimg\Web服务器小结.png)

# 2.Tomcat

![Tomcat基本使用](E:\笔记\JavaWebimg\Tomcat基本使用.png)

## 1.Tomcat配置

![Tomcat配置](E:\笔记\JavaWebimg\Tomcat配置.png)

## 2.Tomcat部署项目

![Tomcat部署项目](E:\笔记\JavaWebimg\Tomcat部署项目.png)

## 3.IDEA中创建Maven Web项目

![IDEA中创建Maven Web项目](E:\笔记\JavaWebimg\IDEA中创建Maven Web项目.png)

### 1.使用骨架

![使用骨架](E:\笔记\JavaWebimg\使用骨架.png)

### 2.不使用骨架

![不使用骨架](E:\笔记\JavaWebimg\不使用骨架.png)

# 4.IDEA中使用Tomcat

**tomcat默认编码为ISO-8859-1**

## 1.集成本地Tomcat

![集成本地Tomcat](E:\笔记\JavaWebimg\集成本地Tomcat.png)

## 2.Tomcat Maven插件

![Tomcat Maven插件](E:\笔记\JavaWebimg\Tomcat Maven插件.png)

# 5.Servlet

![Servlet快速入门](E:\笔记\JavaWebimg\Servlet快速入门.png)

## 1.servlet执行流程

![servlet执行流程](E:\笔记\JavaWebimg\servlet执行流程.png)

## 2.servlet生命周期

![servlet生命周期](E:\笔记\JavaWebimg\servlet生命周期.png)

### 1.init

```
/**
 * urlPatterns:路径
 * loadOnStartUp:默认值为-1
 * 如果是正整数或0：创建服务器时加载对象
 * 如果是负整数整数：第一次访问时创建对象
 */
@WebServlet(urlPatterns = "/demo",loadOnStartup = -1)
public class ServletDemo1 implements Servlet {
    /**
     * init
     * servlet创建时调用该方法
     * @param servletConfig
     * @throws ServletException
     */
    @Override
    public void init(ServletConfig servletConfig) throws ServletException {
        System.out.println("init...");
    }
```

#### 1.当loadOnStartup值为默认值时

![init默认值](E:\笔记\JavaWebimg\init默认值.png)

#### 2.当loadOnStartup值为正整数时

![init正整数](E:\笔记\JavaWebimg\init正整数.png)

### 2.service

```
/**
 * 提供服务
 * 1.调用时机：每一次servlet被访问时，调用方法
 * 2.调用次数：多次
 * @param servletRequest
 * @param servletResponse
 * @throws ServletException
 * @throws IOException
 */
@Override
public void service(ServletRequest servletRequest, ServletResponse servletResponse) throws ServletException, IOException {
    System.out.println("Holle Servlet!");
}
```

### 3.destroy

![destroy](E:\笔记\JavaWebimg\destroy.png)

## 3.servlet方法介绍

![servlet方法介绍](E:\笔记\JavaWebimg\servlet方法介绍.png)

## 4.servlet体系结构

![servlet体系结构](E:\笔记\JavaWebimg\servlet体系结构.png)

### 1.get

**HttpServlet默认是get访问方式**

```java
@WebServlet("/demo2")
public class ServletDemo2 extends HttpServlet {
    @Override
    protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
//        super.doGet(req, resp);
        System.out.println("get..");
    }

    @Override
    protected void doPost(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
//        super.doPost(req, resp);
        System.out.println("post..");
    }
}
```

![默认get方式传输](E:\笔记\JavaWebimg\默认get方式传输.png)

### 2.post

![post](E:\笔记\JavaWebimg\post.png)

![post2](E:\笔记\JavaWebimg\post2.png)

### 3.MyHttpServlet

建议自己写一个HttpServlet实现类，以后就不用每次都重复写get和post的判断

**MyHttpServlet**

```java
@Override
public void service(ServletRequest servletRequest, ServletResponse servletResponse) throws ServletException, IOException {
    //根据请求方式不同，进行分别处理
    HttpServletRequest hs = (HttpServletRequest) servletRequest;

    //1.获取请求方式
    String m = hs.getMethod();
    //2.判断传输方式
    if("GET".equals(m)){
        //get方式
        doGet(servletRequest,servletResponse);
    }else if ("POST".equals(m)){
        //post方式
        doPost(servletRequest,servletResponse);
    }
}

protected void doPost(ServletRequest servletRequest, ServletResponse servletResponse) {
    System.out.println("post..");
}

protected void doGet(ServletRequest servletRequest, ServletResponse servletResponse) {
    System.out.println("get..");
}
```

实现类Demo

```java
@WebServlet("/demo3")
public class ServletDemo3 extends MyHttpServlet{
    @Override
    protected void doGet(ServletRequest servletRequest, ServletResponse servletResponse) {
        super.doGet(servletRequest, servletResponse);
    }

    @Override
    protected void doPost(ServletRequest servletRequest, ServletResponse servletResponse) {
        super.doPost(servletRequest, servletResponse);
    }
}
```

## 5.Servlet urlPattern配置

![Servlet urlPattern配置](E:\笔记\JavaWebimg\Servlet urlPattern配置.png)

 ![配置规则](E:\笔记\JavaWebimg\配置规则.png)

**当精确匹配和目录匹配同时满足，则精确匹配先执行**

servlet项目中默认配置了/，用于访问静态资源，如果我们使用webservlet配置/，则本地的静态资源我们就无法访问了

## 6.xml配置servlet

![xml配置servlet](E:\笔记\JavaWebimg\xml配置servlet.png)

# 6.Request&Response

![Request&Response](E:\笔记\JavaWebimg\Request&Response.png)

## 1.Request

### 1.Request继承体系

![Request继承体系](E:\笔记\JavaWebimg\Request继承体系.png)

### 2.Request获取请求数据

#### 1.请求行

![请求行](E:\笔记\JavaWebimg\请求行.png)

```java
@Override
protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
    super.doGet(req, resp);
    //获取请请求方式
    String method = req.getMethod();
    System.out.println(method);
    //获取虚拟路径
    String contextPath = req.getContextPath();
    System.out.println(contextPath);
    //获取url
    StringBuffer requestURL = req.getRequestURL();
    System.out.println(requestURL);
    //获取uri
    String requestURI = req.getRequestURI();
    System.out.println(requestURI);
    //获取请求参数
    String queryString = req.getQueryString();
    System.out.println(queryString);
}
```

#### 2.请求头

![请求头](E:\笔记\JavaWebimg\请求头.png)

```java
//获取请求头
String header = req.getHeader("user-agent");
System.out.println(header);
```

#### 3.请求体

![请求体](E:\笔记\JavaWebimg\请求体.png)

```java
@Override
protected void doPost(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
    super.doPost(req, resp);
    //获取字符输入流
    BufferedReader reader = req.getReader();
    //读取数据
    String s = reader.readLine();
    System.out.println(s);

}
```

### 3.Request请求参数

![request请求参数](E:\笔记\JavaWebimg\request请求参数.png)

#### 1.使用map集合

```java
//1.使用map
Map<String, String[]> parameterMap = servletRequest.getParameterMap();
for (String key : parameterMap.keySet()) {
    System.out.print(key + ":");
    String[] values = parameterMap.get(key);
    for (String v : values) {
        System.out.print(v + " ");
    }
}
```

#### 2.获取参数值

```java
//2.获取参数值
String[] parameterValues = servletRequest.getParameterValues("hobby");
for (String parameterValue : parameterValues) {
    System.out.println(parameterValue);
}
```

#### 3.获取单个参数值

```java
//3.获取单个参数值
String singleParamer = servletRequest.getParameter("hobby");
System.out.println(singleParamer);
```

在get里面写了一次，在post里面调用即可，不需要再写一遍

```java
@Override
protected void doPost(ServletRequest servletRequest, ServletResponse servletResponse) {
    super.doPost(servletRequest, servletResponse);
    System.out.println("post...");
    doGet(servletRequest,servletResponse);
}
```

### 4.Request模板

#### 创建模板

![创建模板](E:\笔记\JavaWebimg\创建模板.png)

#### 更改模板

![request模板](E:\笔记\JavaWebimg\request模板.png)

### 5.中文乱码

![处理乱码](E:\笔记\JavaWebimg\处理乱码.png)

#### 1.post

![post中文乱码](E:\笔记\JavaWebimg\post中文乱码.png)

使用post解决乱码问题

```java
@WebServlet("/demo6")
public class ServletDemo6 extends HttpServlet {
    @Override
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        //1.设置字符集
        request.setCharacterEncoding("UTF-8");

        //2.获取数据
        String username = request.getParameter("username");
        System.out.println(username);
    }

    @Override
    protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        doGet(request,response);
    }
}
```

#### 2.get

```java
//1.获取数据
String username = request.getParameter("username");
System.out.println("转换之前:" + username);
//2.获取字节
byte[] bytes = username.getBytes(StandardCharsets.ISO_8859_1);
//3.转换字节
username = new String(bytes,StandardCharsets.UTF_8);
//4.输出转换后的数据
System.out.println("转换之后:" + username);
```

#### 3.万能代码

```java
//简化版，万能代码，能够代替post的setCharacterEncoding
username = new String(username.getBytes(StandardCharsets.ISO_8859_1),StandardCharsets.UTF_8);
```

tomcat8以后默认编码为utf-8，就不需要我们再去设置了

### 6.Request请求转发

![请求转发](E:\笔记\JavaWebimg\请求转发.png)

```java
@WebServlet("/demo7")
public class ServletDemo7 extends HttpServlet {
    @Override
    protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
        System.out.println("demo7");
        req.setAttribute("msg","hello");
        req.getRequestDispatcher("/demo8").forward(req,resp);

    }

    @Override
    protected void doPost(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

    }
}
```

```java
@WebServlet("/demo8")
public class ServletDemo8 extends HttpServlet {
    @Override
    protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
        System.out.println("demo8");
        Object msg = req.getAttribute("msg");
        System.out.println(msg);
    }

    @Override
    protected void doPost(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {

    }
}
```

## 2.Response

### 1.设置响应数据设置

![response响应数据介绍](E:\笔记\JavaWebimg\response响应数据介绍.png)

### 2.重定向

![response重定向](E:\笔记\JavaWebimg\response重定向.png)

方法一

```java
//1.设置相应码
resp.setStatus(302);
//2.设置响应头
resp.setHeader("Location","/tomcat-demo4/resp2");
```

方法二

```java
resp.sendRedirect("/tomcat-demo4/resp2");
```

### 3.路径问题

![路径问题](E:\笔记\JavaWebimg\路径问题.png)



```java
//获取虚拟路径
String contextPath = req.getContextPath();
//高内聚，低耦合
resp.sendRedirect(contextPath + "/resp2");
```

### 4.响应字符数据

![response响应字符数据](E:\笔记\JavaWebimg\response响应字符数据.png)

```java
@Override
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        //1.获取字符输出流
        PrintWriter writer = response.getWriter();
        //2.设置文件格式
        response.setHeader("content-type","text/html");
        writer.write("你好!");
        writer.write("<h1>aaa<h1>");
    }
```

**此时中文字符会出现乱码，应为tomcat的默认编码不是utf-8**

我们加上

```java
response.setContentType("text/html;charset=utf-8");
```

```java
@Override
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		//设置字符集和文件格式
		response.setContentType("text/html;charset=utf-8");
        //1.获取字符输出流
        PrintWriter writer = response.getWriter();
        writer.write("你好!");
        writer.write("<h1>aaa<h1>");
    }
```

### 5.相应字节数据

![response响应字节数据](E:\笔记\JavaWebimg\response响应字节数据.png)

```java
@Override
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
    //1.读取文件
    FileInputStream fs = new FileInputStream("E:\\笔记\\JavaWebimg\\destroy.png");
    //2.获取response字节输出流
    ServletOutputStream os = response.getOutputStream();
    //3.完成流的copy
    byte[] b = new byte[1024];
    int len = 0;
    while ((len = fs.read()) != - 1){
        os.write(b,0,len);
    }
    fs.close();
}
```

工具类使用

```java
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        //1.读取文件
        FileInputStream fs = new FileInputStream("E:\\笔记\\JavaWebimg\\destroy.png");
        //2.获取response字节输出流
        ServletOutputStream os = response.getOutputStream();
        //3.完成流的copy
        IOUtils.copy(fs,os);
        fs.close();
    }
```

# 7.JSP

## JSP简介

![JSP简介](E:\笔记\JavaWebimg\JSP简介.png)

## 1.JSP快速入门

![JSP快速入门](E:\笔记\JavaWebimg\JSP快速入门.png)

## 2.JSP原理

![JSP原理](E:\笔记\JavaWebimg\JSP原理.png)

## 3.JSP脚本

![JSP脚本](E:\笔记\JavaWebimg\JSP脚本.png)

## 4.JSP缺点

![JSP缺点](E:\笔记\JavaWebimg\JSP缺点.png)

# 8.EL表达式

![EL表达式](E:\笔记\JavaWebimg\EL表达式.png)

# 9.JSTL

![JSTL标签](E:\笔记\JavaWebimg\JSTL标签.png)

## JSTL快速入门

![JSTL快速入门](E:\笔记\JavaWebimg\JSTL快速入门.png)

## forEach

![JSTLforEach](E:\笔记\JavaWebimg\JSTLforEach.png)

# 10.MVC模式

![MVC模式](E:\笔记\JavaWebimg\MVC模式.png)

## 1.三层架构

![三层架构](E:\笔记\JavaWebimg\三层架构.png)

## 2.三层架构解析

![三层架构解析](E:\笔记\JavaWebimg\三层架构解析.png)

# 11.Cookie

![Cookie基本使用](E:\笔记\JavaWebimg\Cookie基本使用.png)

## 1.创建Cookie

```java
protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
    //创建Cookie
    Cookie c = new Cookie("username","whh");
    //发送Cookie
    resp.addCookie(c);
}
```

## 2.获取Cookie

```java
@Override
protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
    //获取Cookie数组
    Cookie[] cookies = req.getCookies();
    //遍历数组
    for (Cookie cookie : cookies) {
        String name = cookie.getName();
        //输出Cookie名为username的值
        if("username".equals(name)){
            String value = cookie.getValue();
            System.out.println(value);
        }
    }
}
```

## 3.Cookie原理

![Cookie原理](E:\笔记\JavaWebimg\Cookie原理.png)

## 4.设置Cookie存活时间

![Cookie使用细节](E:\笔记\JavaWebimg\Cookie使用细节.png)

```java
//设置Cookie存活时间
int t = 60*60*24*7;//七天
c.setMaxAge(t);
```

## 5.设置字符转码

![Cookie存储中文](E:\笔记\JavaWebimg\Cookie存储中文.png)

```
//转码

URLEncoder.encode(变量,"字符编码");

//解码

URLDncoder.encode(变量,"字符编码");
```

# 12.Session

![Session](E:\笔记\JavaWebimg\Session.png)

## 1.创建Session

```
@Override
protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
    //1.获取session
    HttpSession s = req.getSession();
    //2.存储数据
    s.setAttribute("username","whh");
}
```

## 2.获取Session

```
protected void doGet(HttpServletRequest req, HttpServletResponse resp) throws ServletException, IOException {
    //1.获取session
    HttpSession s = req.getSession();
    //2.存储数据
    Object username = s.getAttribute("username");
    //3.在控制台输出
    System.out.println(username);
}
```

## 3.Session原理

![Session原理](E:\笔记\JavaWebimg\Session原理.png)

![JSSESSIONID](E:\笔记\JavaWebimg\JSSESSIONID.png)

## 4.Session使用细节

![Session使用细节](E:\笔记\JavaWebimg\Session使用细节.png)

## 5.销毁

### 1.设置session自动销毁

![设置session自动销毁](E:\笔记\JavaWebimg\设置session自动销毁.png)

### 2.调用invalidate方法

```java
//1.获取session
HttpSession s = req.getSession();
//2.存储数据
Object username = s.getAttribute("username");
//3.销毁
s.invalidate();
```

# 13.Cookie和Session小结

![Cookie和Session小结](E:\笔记\JavaWebimg\Cookie和Session小结.png)

# 14.JSP中获取Cookie

![JSP中获取Cookie](E:\笔记\JavaWebimg\JSP中获取Cookie.png)

## 1.注册

```java
/**
 * 用户注册
 */
public static boolean registerUser(User user){
    SqlSessionFactory factory = SqlSessionFactoryUilts.getSqlSessionFactory();
    SqlSession sqlSession = factory.openSession();
    UserMapper mapper = sqlSession.getMapper(UserMapper.class);
    System.out.println(user.getUsername());
    User u = mapper.selectByName(user.getUsername());
    if(u == null){
        mapper.addUser(user);
        sqlSession.commit();
    }
    sqlSession.close();
    return u == null;
}
```

## 2.登录

```java
/**
 * 用户登录
 * @param name
 * @param password
 * @return
 */
public static User getUser(String name, String password){
    SqlSessionFactory factory = SqlSessionFactoryUilts.getSqlSessionFactory();
    SqlSession sqlSession = factory.openSession();
    UserMapper mapper = sqlSession.getMapper(UserMapper.class);
    User user = mapper.select(name, password);
    sqlSession.close();
    return user;
}
```

# 15.Filter

## 1.Filter快速入门

![Filter快速入门](E:\笔记\JavaWebimg\Filter快速入门.png)

## 2.Filter执行流程

![Filter执行流程](E:\笔记\JavaWebimg\Filter执行流程.png)

## 3.Filter拦截路劲配置

![Filter拦截路劲配置](E:\笔记\JavaWebimg\Filter拦截路劲配置.png)

## 4.过滤器链

![过滤器链](E:\笔记\JavaWebimg\过滤器链.png)

![过滤器链执行](E:\笔记\JavaWebimg\过滤器链执行.png)

# 16.监听器

![Listener](E:\笔记\JavaWebimg\Listener.png)

## ServletContextListener

![ServletContextListener](E:\笔记\JavaWebimg\ServletContextListener.png)

# 17.AJAX

![AJAX](E:\笔记\JavaWebimg\AJAX.png)

## 1.异步和同步

![同步异步](E:\笔记\JavaWebimg\同步异步.png)

## 2.AJAX快速入门

![AJAX快速入门](E:\笔记\JavaWebimg\AJAX快速入门.png)

# 18.Axios

![Axios](E:\笔记\JavaWebimg\Axios.png)

## 1.Axios基本使用

![Axios基本使用](E:\笔记\JavaWebimg\Axios基本使用.png)

```json
//get
axios({
    method:"get",
    url:"http://localhost:8080/Cookie/axios?username=whh"
}).then(function (resp){
    alert(resp.data)
})
```

```json
//post
axios({
    method: "post",
    url: "http://localhost:8080/Cookie/axios",
    data : "username = whh"
}).then(function (resp){
    alert(resp.data)
})
```

## 2.Axios别名

![Axios别名](E:\笔记\JavaWebimg\Axios别名.png)

```json
//get
axios.get("http://localhost:8080/Cookie/axios?username=whh").then(function (resp){
    alert(resp.data)
})
//post
axios.get("http://localhost:8080/Cookie/axios","username=whh").then(function (resp){
    alert(resp.data)
})
```

# 19.JSON

![JSON](E:\笔记\JavaWebimg\JSON.png)

## 1.JSON基础语法

![JSON基础语法](E:\笔记\JavaWebimg\JSON基础语法.png)

## 2.JSON和Java对象的转换

![JSON和Java对象转换](E:\笔记\JavaWebimg\JSON和Java对象转换.png)

```java
public class JSONtest {
    public static void main(String[] args) {
        User u = new User();
        u.setUsername("whh");
        u.setPassword("123456");
        u.setId(1);
        //转换为JSON对象
        String jsonString = JSON.toJSONString(u);
        System.out.println(jsonString);
        //转换为java对象
        User user = JSON.parseObject(jsonString, User.class);
        System.out.println(user);
    }
}
```

# 20.Vue

![Vue](E:\笔记\JavaWebimg\Vue.png)

## 1.Vue基本使用

![Vue基本使用](E:\笔记\JavaWebimg\Vue基本使用.png)

## 2.Vue常用指令

![Vue常用指令](E:\笔记\JavaWebimg\Vue常用指令.png)

### 1.v-bind

![v-bind](E:\笔记\JavaWebimg\v-bind.png)

```html
<div id="app">
    <a :href="url" >别点我</a>
    <a v-bind:href="url">别点我</a>
    <input type="text" name="username" v-model="url">
</div>
<script src="js/vue.js"></script>
<script>
    new Vue({
        el:"#app",
        data(){
            return{
                username:"",
                url:"https://www.baidu.com"
            }
        }
    });
</script>
```

### 2.v-on

![v-on](E:\笔记\JavaWebimg\v-on.png)

```html
<div id="app">
    <button v-on:click="show()">你点我试试</button>
</div>
<script src="js/vue.js"></script>
<script>
    new Vue({
        el:"#app",
        methods:{
            show(){
                alert("我被电了")
            }
        }
    });
</script>
```

### 3.v-if and v-show

![v-if and v-show](E:\笔记\JavaWebimg\v-if and v-show.png)

```html
<div id="app">
    <input v-model="count">
    <button v-on:click="show()">你点我试试</button>
    <div v-if="count == 1">1</div>
    <div v-else-if="count == 2">2</div>
    <div v-else>3</div>
    <div v-show="count == 2">你看不见我</div>
</div>
<script src="js/vue.js"></script>
<script>
    new Vue({
        el:"#app",
        data(){
            return{
                count:2
            }
        },
        methods:{
            show(){
                alert("我被电了")
            }
        }
    });
</script>
```

### 4.v-for

![v-for](E:\笔记\JavaWebimg\v-for.png)

```html
<div id="app">
    <input v-model="count">
    <button v-on:click="show()">你点我试试</button>
    <div v-if="count == 1">1</div>
    <div v-else-if="count == 2">2</div>
    <div v-else>3</div>
    <div v-show="count == 2">你看不见我</div>
    <div v-for="(addr,i) in addrs">
        {{i}}--{{addr}}
    </div>
</div>
<script src="js/vue.js"></script>
<script>
    new Vue({
        el:"#app",
        data(){
            return{
                count:2,
                addrs:["北京","上海","深圳"]
            }
        },
        methods:{
            show(){
                alert("我被电了")
            }
        }
    });
</script>
```

## 3.Vue生命周期

![Vue生命周期](E:\笔记\JavaWebimg\Vue生命周期.png)

### 1.流程图

![Vue生命周期流程图](E:\笔记\JavaWebimg\Vue生命周期流程图.png)

### 2.mounted

![mounted](E:\笔记\JavaWebimg\mounted.png)

```html
<div id="app">
    <input v-model="count">
    <button v-on:click="show()">你点我试试</button>
    <div v-if="count == 1">1</div>
    <div v-else-if="count == 2">2</div>
    <div v-else>3</div>
    <div v-show="count == 2">你看不见我</div>
    <div v-for="(addr,i) in addrs">
        {{i}}--{{addr}}
    </div>
</div>
<script src="js/vue.js"></script>
<script>
    new Vue({
        el:"#app",
        data(){
            return{
                count:2,
                addrs:["北京","上海","深圳"]
            }
        },
        methods:{
            show(){
                alert("我被电了")
            }
        },
        mounted(){
            alert("页面渲染完成")
        }
    });
```

# 21.Element

![Element](E:\笔记\JavaWebimg\Element.png)

## 1.Element快速入门

![Element快速入门](E:\笔记\JavaWebimg\Element快速入门.png)

```html
<script src="js/vue.js"></script>
<script src="element-ui/lib/index.js"></script>
<link rel="stylesheet" href="element-ui/lib/theme-chalk/index.css">
```

## 2.element布局

![element布局](E:\笔记\JavaWebimg\element布局.png)

 
