# 1.SSM整合

![SSM](.\SSMimg\SSM.png)

## 1.1 config层

### 1.1.1 SpringConfig

```java
@Configuration
@ComponentScan({"com.whh.controller","com.whh.service"})
@PropertySource("classpath:jdbc.properties")
@Import({JdbcConfig.class,MyBatisConfig.class})
public class SpringConfig {
}
```

### 1.1.2 SpringMvcConfig

```java
@Configuration
@ComponentScan("com.whh.controller")
@EnableWebMvc
@EnableTransactionManagement
public class SpringMvcConfig {
}
```

### 1.1.3 ServletConfig

```java
public class ServletConfig extends AbstractAnnotationConfigDispatcherServletInitializer {

    @Override
    protected Class<?>[] getRootConfigClasses() {
        return new Class[]{SpringConfig.class};
    }

    @Override
    protected Class<?>[] getServletConfigClasses() {
        return new Class[]{SpringMvcConfig.class};
    }

    @Override
    protected String[] getServletMappings() {
        return new String[]{"/"};
    }
}
```

### 1.1.4 MyBatisConfig

```java
public class MyBatisConfig {
    @Bean
    public SqlSessionFactoryBean sqlSessionFactoryBean(DataSource dataSource){
        SqlSessionFactoryBean sqlSessionFactoryBean = new SqlSessionFactoryBean();
        sqlSessionFactoryBean.setDataSource(dataSource);
        sqlSessionFactoryBean.setTypeAliasesPackage("com.whh.domain");
        return sqlSessionFactoryBean;
    }

    @Bean
    public MapperScannerConfigurer mapperScannerConfigurer(){
        MapperScannerConfigurer mapperScannerConfigurer = new MapperScannerConfigurer();
        mapperScannerConfigurer.setBasePackage("com.whh.dao");
        return mapperScannerConfigurer;
    }
}
```

### 1.1.5 JdbcConfig

```java
@Configuration
public class JdbcConfig {

    @Value("${jdbc.driver}")
    private String driver;
    @Value("${jdbc.url}")
    private String url;
    @Value("${jdbc.username}")
    private String username;
    @Value("${jdbc.password}")
    private String password;

    @Bean
    public DataSource dataSource(){
        DruidDataSource da = new DruidDataSource();
        da.setDriverClassName(driver);
        da.setUrl(url);
        da.setUsername(username);
        da.setPassword(password);
        return da;
    }

    public PlatformTransactionManager platformTransactionManager(DataSource dataSource){
        DataSourceTransactionManager ds = new DataSourceTransactionManager();
        ds.setDataSource(dataSource);
        return ds;
    }
}
```

### 1.1.6 SpringMvcSupport



# 2.异常处理

![异常处理器](.\SSMimg\异常处理器.png)

![异常处理器解决方法](.\SSMimg\异常处理器解决方法.png)

```java
@RestControllerAdvice
public class ProjectExceptionAdvice {
    @ExceptionHandler(Exception.class)
    public Result exception(Exception ex){
        System.out.println("报错了！！！！！");
        return new Result(null,"0","报错了！！！");
    }
}
```

## 2.1 RestContrllerAdvice

![RestContrllerAdvice](.\SSMimg\RestContrllerAdvice.png)

## 2.2 ExceptionHandler

![ExceptionHandler](.\SSMimg\ExceptionHandler.png)

# 3.项目异常

## 3.1 项目异常分类

![项目异常分类](.\SSMimg\项目异常分类.png)

## 3.2 项目异常处理

![项目异常处理](.\SSMimg\项目异常处理.png)

## 3.3 拦截处理异常

![拦截处理异常](.\SSMimg\拦截处理异常.png)

# 4.拦截器(interceptor)

![拦截器概念](.\SSMimg\拦截器概念.png)

![拦截器概念2](.\SSMimg\拦截器概念2.png)

## 4.1 拦截器与过滤器区别

![拦截器与过滤器区别](.\SSMimg\拦截器与过滤器区别.png)

## 4.2 拦截器HandlerInterceptor

### 4.2.1 创建HandlerInterceptor

![拦截器HandlerInterceptor](.\SSMimg\拦截器HandlerInterceptor.png)

### 4.2.2 定义配置类

![定义配置类](.\SSMimg\定义配置类.png)

### 4.2.3 添加拦截器

![添加拦截器](.\SSMimg\添加拦截器.png)

### 4.2.4 使用简化开发

![使用简化开发](.\SSMimg\使用简化开发.png)

## 4.3 拦截器执行流程

![拦截器执行流程](.\SSMimg\拦截器执行流程.png)

## 4.4 拦截器参数

### 4.4.1 前置处理

![前置处理](.\SSMimg\前置处理.png)

### 4.4.2 后置处理

![后置处理](.\SSMimg\后置处理.png)

### 4.4.3 完成后处理

![完成后处理](.\SSMimg\完成后处理.png)

## 4.5 多拦截器执行顺序

![多拦截器执行顺序](.\SSMimg\多拦截器执行顺序.png)