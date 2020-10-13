# Spring
Spring related questions 

Spring MVC sample application:

Spring form Tags:

```

Form 

Input 

Checkbox

Checkboxes

Radiobutton

Radiobuttons

Password 

Select

Option

Options 

Textarea

Hidden

Errors

```

Annotations in controller:

```

@Controller
@Autowired
@RequestMapping -> (value="/deleteemp/{id}",method = RequestMethod.GET)

```

RequestMethod:

RequestMethod.GE - delete
RequestMethod.POST - update

emp pojo class:

```
private int id;  
private String name;  
private float salary;  
private String designation;  

```

dao class:

JdbcTemplate:

save 
update
delete
getEmployeeId

JdbcTemplate template;  
 
```

public void setTemplate(JdbcTemplate template) {  
    this.template = template;  
} 


String sql="insert into Emp99(name,salary,designation) values('"+p.getName()+"',"+p.getSalary()+",'"+p.getDesignation()+"')";
String sql="update Emp99 set name='"+p.getName()",designation='"+p.getDesignation()+"' where id="+p.getId()+"";
String sql="delete from Emp99 where id="+id+"";
String sql="select * from Emp99 where id=?";

template.update(sql);

```

Spring MVC sample application:

Spring Servlet.xml :


adding jsp in web-inf:

```

<bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
<property name="prefix" value="/WEB-INF/jsp/"></property>
<property name="suffix" value=".jsp"></property>
</bean>

``` 

adding dao:

```

<bean id="ds" class="org.springframework.jdbc.datasource.DriverManagerDataSource">  
<property name="driverClassName" value="com.mysql.jdbc.Driver"></property>  
<property name="url" value="jdbc:mysql://localhost:3306/springDB"></property>  
<property name="username" value="root"></property>  
<property name="password" value=""></property>  
</bean>  

``` 

adding jdbc template:

<bean id="jt" class="org.springframework.jdbc.core.JdbcTemplate">
<property name="dataSource" ref="ds"></property>
</bean>

adding dao:

<bean id="dao" class="com.javatpoint.dao.EmpDao">
<property name="template" ref="jt"></property>
</bean>
</beans>

web.xml:

add dispactcher server

```

<web-app xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://java.sun.com/xml/ns/javaee" xsi:schemaLocation="http://java.sun.com/xml/ns/javaee http://java.sun.com/xml/ns/javaee/web-app_3_0.xsd" id="WebApp_ID" version="3.0">
  <display-name>SpringMVC</display-name>
   <servlet>  
    <servlet-name>spring</servlet-name>  
    <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>  
    <load-on-startup>1</load-on-startup>    
</servlet>  
<servlet-mapping>  
    <servlet-name>spring</servlet-name>  
    <url-pattern>/</url-pattern>  
</servlet-mapping>  
</web-app>

```
package names:

beans
controller
dao

jsp in web-Inf

create jsp folder under add all JSP:

pom.xml:

adding jars 

spring web mvc
tomcat server
jstl
mysql
SpringMVCPagination


Spring Servlet.xml :


adding jsp in web-inf:

```
<bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
<property name="prefix" value="/WEB-INF/jsp/"></property>
<property name="suffix" value=".jsp"></property>
</bean>
```

adding dao:

```

<bean id="ds" class="org.springframework.jdbc.datasource.DriverManagerDataSource">  
<property name="driverClassName" value="com.mysql.jdbc.Driver"></property>  
<property name="url" value="jdbc:mysql://localhost:3306/springDB"></property>  
<property name="username" value="root"></property>  
<property name="password" value=""></property>  
</bean>  
```

adding jdbc template:

```
<bean id="jt" class="org.springframework.jdbc.core.JdbcTemplate">
<property name="dataSource" ref="ds"></property>
</bean>
```
adding dao:
```
<bean id="dao" class="com.javatpoint.dao.EmpDao">
<property name="template" ref="jt"></property>
</bean>
</beans>
```
web.xml:

add dispactcher server

```
<web-app xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://java.sun.com/xml/ns/javaee" xsi:schemaLocation="http://java.sun.com/xml/ns/javaee http://java.sun.com/xml/ns/javaee/web-app_3_0.xsd" id="WebApp_ID" version="3.0">
  <display-name>SpringMVC</display-name>
   <servlet>  
    <servlet-name>spring</servlet-name>  
    <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>  
    <load-on-startup>1</load-on-startup>    
</servlet>  
<servlet-mapping>  
    <servlet-name>spring</servlet-name>  
    <url-pattern>/</url-pattern>  
</servlet-mapping>  
</web-app>
```
package names:

beans
controller
dao

jsp in web-Inf

create jsp folder under add all JSP:

pom.xml:

adding jars 

spring web mvc
tomcat server
jstl
mysql
SpringMVCPagination


Software 

Spring tool suite 

File-new-Spring starter project 

Spring Boot Basics:

spring with rest

richardson maturiy model
rpc service
resources
verbs

hateoas

crud operation:

rest:

postman:

get
put
post
delete  

Spring boot 

default by singletion
Default by autowire id

@component in pojo
@qualifier by name
@autowire in class where we are using
 
ReatTemplate rt = new RestTemplate

Person per = rt.getforobject
        ("Http:localhost:8080/person/1");

Resttemplate will have all methods of rest

spring data respositories

-spring data:
repository
crudrepository
pagningandsorting repositroy

spring jpa repository:

jparepository

spring data rest 

annotations:
```
@repository
@complement
@springbootapplication
@complementscan({"com.client"})
@xmlrootelement

public interface manufacture extends jpaRepository<manufacturer, Long>
{
List<manufacture> findbyfoundeddatabefore(Date date)
List<manufacture> findbyactivetrue
List<manufacture> findbyactive false
List<manufacture> getallthatsellAcoustics
}
```
@RepositoryRestResources(path="companies")
http:localhost:8080/api/companies

to view in xml

@XmlRootElement

public class person{
}

runs as- spring boot app

to convert into war:



convert jar to war:

pox.xml:

packinging to war

run as-> maven build

Change port in application.properties

Server.port = 8080








