
# in28Minutes-first-webapp

A tiny JSP/Servlet + JSTL todo app packaged as a WAR.

## Prerequisites
- Java 7 or newer (the `pom.xml` targets 1.7; if you use a newer JDK, update `<source>/<target>` to `1.8` or higher)
- Maven 3.x

## Run locally (embedded Tomcat 7 Maven plugin)
```bash
mvn clean package
mvn org.apache.tomcat.maven:tomcat7-maven-plugin:2.2:run
```
Then open http://localhost:8080/

Login with:
- user: `in28Minutes`
- password: `dummy`

## Build a WAR
```bash
mvn clean package
```
Output: `target/in28Minutes-first-webapp-0.0.1-SNAPSHOT.war`

## Deploy notes
- This project uses JSPs under `WEB-INF/views`, JSTL 1.2, and WebJars for Bootstrap/jQuery.
- There is a `LoginRequiredFilter` that forwards all `*.do` URLs to `/login.do` unless a session attribute `name` is present.
- Update Java version in `pom.xml` if your toolchain requires it.
