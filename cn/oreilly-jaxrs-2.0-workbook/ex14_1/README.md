# JAX-RS and EJB


<!-- toc -->


This project is an example of using JAX-RS, EJB, and JPA all together in one application through a JAX-RS
portable way.


## System Requirements:

- Maven 3.0.4 or higher


## Building the project:

1. Start a JBoss 7.1.1 instance in the background
2. In root directory  **mvn clean install**

This will build a WAR, deploy it on JBoss, and then run the testsuite.







## Source Code


### Hierarchy
```
ex14_1
|-- pom.xml
`-- src
    |-- main
    |   |-- java
    |   |   `-- com
    |   |       `-- restfully
    |   |           `-- shop
    |   |               |-- domain
    |   |               |   |-- Customer.java
    |   |               |   |-- Customers.java
    |   |               |   |-- LineItem.java
    |   |               |   |-- Order.java
    |   |               |   |-- Orders.java
    |   |               |   |-- Product.java
    |   |               |   `-- Products.java
    |   |               |-- persistence
    |   |               |   |-- CustomerEntity.java
    |   |               |   |-- LineItemEntity.java
    |   |               |   |-- OrderEntity.java
    |   |               |   `-- ProductEntity.java
    |   |               `-- services
    |   |                   |-- CustomerResource.java
    |   |                   |-- CustomerResourceBean.java
    |   |                   |-- EJBExceptionMapper.java
    |   |                   |-- EntityNotFoundExceptionMapper.java
    |   |                   |-- OrderResource.java
    |   |                   |-- OrderResourceBean.java
    |   |                   |-- ProductResource.java
    |   |                   |-- ProductResourceBean.java
    |   |                   |-- ShoppingApplication.java
    |   |                   |-- StoreResource.java
    |   |                   `-- StoreResourceBean.java
    |   |-- resources
    |   |   `-- META-INF
    |   |       `-- persistence.xml
    |   `-- webapp
    |       `-- WEB-INF
    |           `-- web.xml
    `-- test
        `-- java
            `-- com
                `-- restfully
                    `-- shop
                        `-- test
                            `-- ShoppingTest.java
```


### Details


*pom.xml*

!CODEFILE "./pom.xml"


*src/main/resources/META-INF/persistence.xml*

!CODEFILE "./src/main/resources/META-INF/persistence.xml"


*src/main/webapp/WEB-INF/web.xml*

!CODEFILE "./src/main/webapp/WEB-INF/web.xml"


*src/main/java/com/restfully/shop/domain/Customer.java*

!CODEFILE "./src/main/java/com/restfully/shop/domain/Customer.java"


*src/main/java/com/restfully/shop/domain/Customers.java*

!CODEFILE "./src/main/java/com/restfully/shop/domain/Customers.java"



*src/main/java/com/restfully/shop/domain/LineItem.java*

!CODEFILE "./src/main/java/com/restfully/shop/domain/LineItem.java"


*src/main/java/com/restfully/shop/domain/Order.java*

!CODEFILE "./src/main/java/com/restfully/shop/domain/Order.java"


*src/main/java/com/restfully/shop/domain/Orders.java*

!CODEFILE "./src/main/java/com/restfully/shop/domain/Orders.java"


*src/main/java/com/restfully/shop/domain/Product.java*

!CODEFILE "./src/main/java/com/restfully/shop/domain/Product.java"


*src/main/java/com/restfully/shop/domain/Products.java*

!CODEFILE "./src/main/java/com/restfully/shop/domain/Products.java"


*src/main/java/com/restfully/shop/persistence/CustomerEntity.java*

!CODEFILE "./src/main/java/com/restfully/shop/persistence/CustomerEntity.java"


*src/main/java/com/restfully/shop/persistence/LineItemEntity.java*

!CODEFILE "./src/main/java/com/restfully/shop/persistence/LineItemEntity.java"


*src/main/java/com/restfully/shop/persistence/OrderEntity.java*

!CODEFILE "./src/main/java/com/restfully/shop/persistence/OrderEntity.java"


*src/main/java/com/restfully/shop/persistence/ProductEntity.java*

!CODEFILE "./src/main/java/com/restfully/shop/persistence/ProductEntity.java"


*src/main/java/com/restfully/shop/services/CustomerResource.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/CustomerResource.java"


*src/main/java/com/restfully/shop/services/CustomerResourceBean.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/CustomerResourceBean.java"


*src/main/java/com/restfully/shop/services/EJBExceptionMapper.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/EJBExceptionMapper.java"



*src/main/java/com/restfully/shop/services/EntityNotFoundExceptionMapper.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/EntityNotFoundExceptionMapper.java"



*src/main/java/com/restfully/shop/services/OrderResource.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/OrderResource.java"


*src/main/java/com/restfully/shop/services/OrderResourceBean.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/OrderResourceBean.java"


*src/main/java/com/restfully/shop/services/ProductResource.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/ProductResource.java"


*src/main/java/com/restfully/shop/services/ProductResourceBean.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/ProductResourceBean.java"


*src/main/java/com/restfully/shop/services/StoreResource.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/StoreResource.java"


*src/main/java/com/restfully/shop/services/StoreResourceBean.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/StoreResourceBean.java"


*src/main/java/com/restfully/shop/services/ShoppingApplication.java*

!CODEFILE "./src/main/java/com/restfully/shop/services/ShoppingApplication.java"


*src/test/java/com/restfully/shop/test/ShoppingTest.java*

!CODEFILE "./src/test/java/com/restfully/shop/test/ShoppingTest.java"