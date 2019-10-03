# Spring
Spring related questions 

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





