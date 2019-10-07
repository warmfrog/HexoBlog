
---
layout: post
title: javaweb_tomcat 
tags: [javaweb,tomcat,jsp]
---


## tomcat 篇

* FAQ https://wiki.apache.org/tomcat/FAQ
* WIKI https://wiki.apache.org/tomcat/
* tomcat9.0 home page http://tomcat.apache.org/tomcat-9.0-doc/index.html

## tomcat 安装路径

    C:\Program Files\Apache Software Foundation\Tomcat 9.0

### 环境变量设置

* CATALINA_HOME      "C:\Program Files\Apache Software Foundation\Tomcat 9.0"
* CLASS_PATH         %CATALINA_HOME%\lib;

## 目录

* /bin
* /conf
* /logs
* /webapps

## 启动tomcat 服务器

    startup

## jsp 篇

### jsp 指令

* jsp 代码写在 <% %> 中

#### page 指令

    <%@ page language="java contentType="text/html; charset=GB18030" pageEncoding="GB18030" %>
* language
* extends 设置jsp页面继承的java类
* import 导入java包
    <%@ import="java.util.*" %>
* pageEncoding
    <%@ page pageEncoding="GB18030" %>
* contentType
    <%@ page contentType="text/html; charset=UTF-8" %>
* session
    <%@ page session="false" %>
* buffer 设置out缓冲区大小，默认8kb， 单位kb
    <%@ page buffer="128kb" %>
* autoFlush 页面缓存满时是否刷新，默认 true
    <%@ page autoFlush="true" %>
* isErrorPage
    <%@ page isErrorPage="true" %>
* errorPage
    <%@ page errorPage="error.jsp" %>

#### include 指令

    <%@ include file="path" %>

* 被包含页面 <%@ page pageEncoding="GB18030" %>
* 包含页面   <%@ page language="java" contentType="text/html;charset=GB18030" pageEncoding="GB18030" %>

#### taglib 指令

    <%@ taglib prefix="tagPrefix" url="tagURL" %>

* prefix 制定标签前缀
* uri 标签库存放位置

    <%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>

### jsp 脚本标识

* 表达式 <% =表达式  %>
* 声明标识 <%! 声明的代码%>. 用于定义全局方法和变量，用于在整个jsp使用.

#### 代码片段

    <% java代码或者是片段 %>

#### jsp 注释

* 隐藏注释
    <%-- --%>
* 动态注释
    <%-- <%=new Date()%>-->

### jsp 动作标识

* <jsp:include> 包含文件标识
    <jsp:include page="url" flush="false|true" />
    <jsp:include page="url" flush="false|true"> 子动作标识用于传递参数<jsp:param>
    </jsp:include>

动态页面会被jsp编译器编译执行

* <jsp:forward>请求转发标识
    <jsp:forward page="url"/>
    <jsp:forward page="url>
      子动作标识<jsp:param>
      </jsp:forward>

* <jsp:param>传递参数标识
    <jsp:forward page="modify.jsp">
        <jsp:param name="userId" value="7"/>
    </jsp:forward>

## jsp 内置对象

### request

* <a href=delete.jsp?Id=1">删除</a>
* <% request.getParameter("id") %>
* request.setAttribute(String name, Object object);  请求转发时，将数据保存到request中

### response

* 重定向网页 response.sendRedirect(String path);

#### 处理 HTTP 表头

* 禁用缓存
    response.setHeader("Cache-Control","no-store");
    response.setDateHeader("Expires",0);

* 设置页面自动刷新

    response.setHeader("refresh", "10");

* 定时跳转网页

    response.setHeader("refresh", "5;URL=login.jsp");

#### 设置输出缓冲

* flushBuffer()
* getBufferSize()
* setBufferSize(int size)
* reset()
* isCommitted()

### session

#### 创建及获取客户的对话

* session.setAttribute(String name, Object obj);
* session.getAttribute(String name);

#### 移除制定的绑定对象

* session.removeAttribute("username");

#### 销毁 session

* session.invalidate();

#### 超时会话管理

* getLastAccessedTime()
* getMaxInactiveInterval()
* setMaxInactiveInterval()

### application对象

application 对象用户保存所有应用程序中的共有数据。服务器启东时自动创建，服务器停止时销毁。

#### 访问应用程序初始化参数

应用程序初始化参数在 web.xml文件中配置。通过<context-param> 配置

    <context-param>
        <param-name>url</param-name>
        <param-value>jdbc:mysql://localhost/db_database</param-value>
    </context-param>
    </web-app>

    application.getInitParameter(String name);
    application.getInitParameter("url");

* getAttributeName()

    <%
    Enumeration enema= application.getInitParameterNames();
    while(enema.hasMoreElements()){
        String name=(String)enema.nextElements();
        String value = application.getInitParameter(name);
        out.println(name+": ");
        out.println(value);
    }
    %>

#### 管理应用环境属性

* getAttributeNames()
* getAttribute(String name)
* setAttribute(String key, Object obj)
* removeAttribute(String name)

### out 对象

用于在web浏览器上输出信息，并且管理应用服务器上的输出缓冲区。

* 向客户端输出数据
    out.print("");
    out.println("");

#### 管理数据缓冲

* clear()
* clearBuffer()
* flush()
* isAutoFlush()
* getBufferSize()

### 其他内置对象

#### pageContext

通过pageContext 可以获取request,response,session,applicaition,exception 等对象。创建和初始化由容器完成。

* forward(java.lang.String relativeUrlpath)
* getAttribute(String name)
* getAttributeNamesInScope(int scope)
* getException()
* getRequest()
* getResponse()
* getSession()
* getOut()
* getApplication()
* setAttribute()
* removeAttribute()

#### 读取web.xml配置信息的config对象

* getServletContext()
* getServletName()
* getInitParameter()
* getInitParameterNames()

#### 应答或请求的page对象

page 对象代表jsp本身

* getClass()
* hashCode()
* toString()
* equals(Object o)

#### 获取异常信息的exception对象

getMessage()
getLocalizedmessage()
toString()
fillInStackTrace()




