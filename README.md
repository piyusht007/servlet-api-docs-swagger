# Servlet API documentation using swagger

This project is an extension to the servlet [example] provided as part of [swagger-samples]. 

The [example] documents the Servlet available in the same project whereas this extension documents the Servlet available on a different JAR in the classpath.

This project has some tweaks for jetty and integration test: 
* For `jetty`, it is now using `jetty:deploy-war` maven goal. 
* It also generates/writes the API spec file as part of `integration test`.

## Build Steps

To generate the API spec file (**servlet-api-docs-swagger/servlet-sample-api-docs/servlet-sample-openapi.json**), execute the following from `root` folder: 
```java
mvn clean install
```

To just run the jetty and access the api spec URL available at: `localhost:8080/api/swagger.json`, execute the following from `servlet-sample-api-docs` folder:
```java
mvn jetty:run
```
Make sure that before running the above command you've built the `servlet-sample` JAR using `mvn install`. 



---
[swagger-samples]: https://github.com/swagger-api/swagger-samples
[example]: https://github.com/swagger-api/swagger-samples/tree/master/java/java-servlet