# WriterInterceptor


<!-- toc -->


This project implements a WriterInterceptor that generates a Content-MD5 header hash of the message body.

## System Requirements:

- Maven 3.0.4 or higher


## Building the project:

1. In root directory **mvn clean install**

This will build a WAR and run it with embedded Jetty.





## Source Code


### Hierarchy
```
ex12_2
|-- pom.xml
`-- src
    |-- main
    |   |-- java
    |   |   `-- com
    |   |       `-- restfully
    |   |           `-- shop
    |   |               |-- domain
    |   |               |   `-- Customer.java
    |   |               |-- features
    |   |               |   `-- ContentMD5Writer.java
    |   |               `-- services
    |   |                   |-- CustomerResource.java
    |   |                   `-- ShoppingApplication.java
    |   `-- webapp
    |       `-- WEB-INF
    |           `-- web.xml
    `-- test
        `-- java
            `-- com
                `-- restfully
                    `-- shop
                        `-- test
                            `-- CustomerResourceTest.java
```


### Details


*pom.xml*

!CODEFILE "./pom.xml"


*src/main/webapp/WEB-INF/web.xml*

!CODEFILE "./src/main/webapp/WEB-INF/web.xml"


*src/main/java/com/restfully/shop/domain/Customer.java*

!CODEFILE "./src/main/java/com/restfully/shop/domain/Customer.java"


*src/main/java/com/restfully/shop/features/ContentMD5Writer.java*

!CODEFILE "./src/main/java/com/restfully/shop/features/ContentMD5Writer.java"


*src/main/java/com/restfully/shop/services/CustomerResource.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/CustomerResource.java"


*src/main/java/com/restfully/shop/services/ShoppingApplication.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/ShoppingApplication.java"


*src/test/java/com/restfully/shop/test/CustomerResourceTest.java*

!CODEFILE "./src/test/java/com/restfully/shop/test/CustomerResourceTest.java"