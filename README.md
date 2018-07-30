# dynamic-datasource-spring-boot-starter
动态切换多数据源组件
 通过注解方式的转换数据源@DynamicDataSource
 
## 快速开始
~~~
 maven 直接引入
<dependency>
    <groupId>com.github.xphsc</groupId>
    <artifactId>dynamic-datasource-spring-boot-starter</artifactId>
    <version>1.0.1</version>
</dependency>
~~~
## 开发建议
~~~
建议@DynamicDataSource注解在dao,service层 方法级别大于类级别

多数据源配置
spring:
    datasource:
            datasource-name: default
            url: jdbc:mysql://localhost:3306/dynamic_datasource?useUnicode=true&characterEncoding=utf-8&useSSL=false
            username: root
            password: root
    datasources:
         -  datasource-name: slave
            url: jdbc:mysql://localhost:3306/dynamic_datasource1?useUnicode=true&characterEncoding=utf-8&useSSL=false
            username: root
            password: root
         -  datasource-name: master
            url: jdbc:mysql://localhost:3306/dynamic_datasource2?useUnicode=true&characterEncoding=utf-8&useSSL=false
            username: root
            password: root
~~~

#### [更新日志 - GitHub](https://github.com/xphsc/dynamic-datasource-spring-boot-starter/wiki/changelog)

