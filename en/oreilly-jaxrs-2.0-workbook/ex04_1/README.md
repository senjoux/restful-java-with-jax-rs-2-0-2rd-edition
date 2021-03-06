# Custom HTTP Method Annotations


<!-- toc -->


This project is a simple example showing usage how to create your own HTTP method annotation.


## System Requirements:


- Maven 3.0.4 or higher


## Building the project:

1. In root directory **mvn clean install**


This will build a WAR and run it with embedded Jetty.


## Source Code


### Hierarchy
```
ex04_1
|-- pom.xml
`-- src
    |-- main
    |   |-- java
    |   |   |-- com
    |   |   |   `-- restfully
    |   |   |       `-- shop
    |   |   |           |-- domain
    |   |   |           |   `-- Customer.java
    |   |   |           `-- services
    |   |   |               |-- CustomerResource.java
    |   |   |               `-- ShoppingApplication.java
    |   |   `-- org
    |   |       `-- ietf
    |   |           `-- annotations
    |   |               `-- PATCH.java
    |   `-- webapp
    |       `-- WEB-INF
    |           `-- web.xml
    `-- test
        `-- java
            `-- com
                `-- restfully
                    `-- shop
                        `-- test
                            `-- PatchTest.java
```


### Details



*pom.xml*

!CODEFILE "./pom.xml"


*src/main/webapp/WEB-INF/web.xml*

!CODEFILE "./src/main/webapp/WEB-INF/web.xml"


*src/main/java/com/restfully/shop/domain/Customer.java*

!CODEFILE "./src/main/java/com/restfully/shop/domain/Customer.java"


*src/main/java/com/restfully/shop/services/CustomerResource.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/CustomerResource.java"


*src/main/java/com/restfully/shop/services/ShoppingApplication.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/ShoppingApplication.java"


*src/main/java/org/ietf/annotations/PATCH.java*

!CODEFILE "./src/main/java/org/ietf/annotations/PATCH.java"


*src/test/java/com/restfully/shop/test/PatchTest.java*

!CODEFILE "./src/test/java/com/restfully/shop/test/PatchTest.java"