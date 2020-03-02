## 拉取8.5.x源码
git clone xxx
git checkout 8.5.x

## 新建目录 catalina-home
- 将webapps目录和conf目录剪切至catalina-home目录下
- 并在catalina-home目录下添加lib、work和logs目录

## 新建pom.xml
添加依赖

## Edit Configurations
Main class:org.apache.catalina.startup.Bootstrap
VM options:-Dcatalina.home="D:/IdeaProjects/tomcat/catalina-home"

## 运行报错
- 添加 CookieFilter.java
- JSP 无法解析  
```
ContextConfig.java 添加:
context.addServletContainerInitializer(new JasperInitializer(), null);
```