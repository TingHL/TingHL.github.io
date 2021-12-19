---
title: Spring Framework Documentation
date: 2021-08-15 16:31:51
tags:
- Spring
description: Spring官网手册笔记
---

# 控制反转 IoC

控制反转（IoC，Inversion of Control )，也被称为依赖注入（DI，dependency injection）。

基础类：`org.springframework.beans`和`org.springframework.context`

BeanFactory接口 --  public interface ListableBeanFactory extends BeanFactory --  子接口 ApplicationContext  interface ApplicationContext extends EnvironmentCapable, ListableBeanFactory, HierarchicalBeanFactory,
		MessageSource, ApplicationEventPublisher, ResourcePatternResolver



ApplicationContext是BeanFactory的superset



Spring, In Spring, the objects that form the backbone of your application and that are managed by the Spring IoC container are called beans. .

A bean is an object that is instantiated, assembled, and managed by a Spring IoC container.





org.springframework.context.ApplicationContext 接口代表了IoC容器，负责实例化、配置和装配beans.

在stand-alone应用中，一般使用[`ClassPathXmlApplicationContext`](https://docs.spring.io/spring-framework/docs/5.3.9/javadoc-api/org/springframework/context/support/ClassPathXmlApplicationContext.html) or [`FileSystemXmlApplicationContext`](https://docs.spring.io/spring-framework/docs/5.3.9/javadoc-api/org/springframework/context/support/FileSystemXmlApplicationContext.html)

支持XML、Java Annotation等方式，可以通过少量 XML方式来说明支持注解方式。



![container magic](Spring-Framework-Documentation/container-magic.png)
